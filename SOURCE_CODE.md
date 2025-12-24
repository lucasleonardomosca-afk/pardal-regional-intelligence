# Código-Fonte do Pardal - Regional Intelligence

## 🔗 Localização do Código Completo

O código-fonte completo da aplicação Pardal está disponível no Google AI Studio:

**URL**: [https://aistudio.google.com/apps/drive/1HCswQBaOYAcpXJQyeN65kxENsivlPQd-](https://aistudio.google.com/apps/drive/1HCswQBaOYAcpXJQyeN65kxENsivlPQd-)

## 📝 Estrutura da Aplicação

### Arquivos Principais

#### 1. App.tsx (Componente React Principal)

Contém toda a lógica da aplicação:
- Gerenciamento de estado (view, activeArticle, etc.)
- Mock data completo com artigos regionais
- Componentes:
  - **Header** (Pardal branding)
  - **Threshold** (entrada editorial)
  - **HomePage** (grid de artigos)
  - **ArticlePage** (visualização completa)
  - **Footer**

**Principais funcionalidades**:
```typescript
- useState para gerenciamento de view (homepage | article)
- useState para artigo ativo
- Scroll restoration para navegação fluida
- Listener de eventos para scroll
```

#### 2. index.tsx

- Entry point da aplicação React
- Renderização do componente App

**Código**:
```typescript
import React from 'react';
import ReactDOM from 'react-dom/client';
import App from './App';

const root = ReactDOM.createRoot(
  document.getElementById('root') as HTMLElement
);
root.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
);
```

#### 3. index.html

- Template HTML base
- Carregamento de fontes (Crimson Pro, Inter)
- Configuração de viewport e meta tags

**Features**:
```html
- Fontes: Crimson Pro (editorial), Inter (UI)
- Meta viewport para responsividade
- Otimizações de performance
```

#### 4. metadata.json

- Metadados do Google AI Studio
- Configurações de aplicação

## 📦 Pasta documentation/

A pasta `documentation/` contém toda a documentação do projeto dividida em fases:

### PHASE_1.md - Compreensão do Produto & Editorial
Definição da audiência, posicionamento editorial e fluxos de leitura.

### PHASE_2.md - Homepage Ideal (Mental Wireframe)
Estrutura conceitual da homepage com hierarquia de conteúdo por viewport.

### PHASE_3.md - Sistema Visual & Editorial  
Sistema tipográfico, paleta de cores, tokens de design e modo A+.

### PHASE_4.md - Estratégia Responsiva
Definições explícitas de breakpoints e adaptações por dispositivo.

### PHASE_5.md - Arquitetura Frontend
Estrutura de componentes, gerenciamento de estado e padrões de código.

### PHASE_6.md - Modelo de Backend & Dados
Design conceitual do backend Firebase e coleções Firestore.

## 🎨 Design System

### Tipografia

```css
/* Serif Editorial (Manchetes e narrativas) */
font-family: 'Crimson Pro', serif;

/* Sans-Serif Funcional (Metadados e UI) */
font-family: 'Inter', sans-serif;
```

### Escala Tipográfica

```typescript
const TYPOGRAPHY_SCALE = {
  display: '4rem',    // 64px - Títulos hero
  h1: '3rem',         // 48px - Manchetes principais
  h2: '2rem',         // 32px - Subseções
  h3: '1.5rem',       // 24px - Títulos de artigos
  body: '1.125rem',   // 18px - Corpo de texto
  small: '0.875rem'   // 14px - Metadados
};
```

### Paleta de Cores

```typescript
const COLORS = {
  light: {
    background: '#FAFAF9',
    text: '#262626',
    accent: '#2563EB',
    urgent: '#DC2626'
  },
  dark: {
    background: '#171717',
    text: '#FAFAFA',
    accent: '#3B82F6',
    urgent: '#EF4444'
  }
};
```

### Breakpoints

```typescript
const BREAKPOINTS = {
  mobile: '< 640px',
  tablet: '641px - 1024px',
  desktop: '1025px - 1440px',
  xl: '> 1440px'
};
```

## 📊 Mock Data Structure

### Article Interface

```typescript
interface Article {
  id: string;
  slug: string;
  title: string;
  lead: string;
  author: string;
  date: string;
  format: ArticleFormat[];
  category: string;
  pillar: string;
}

type ArticleFormat = {
  type: 'heading' | 'paragraph' | 'quote';
  content: string;
};
```

### Categorias Regionais

1. **São João da Boa Vista**: Plano habitacional 2030
2. **Mococa**: Festival cultural e preservação do patrimônio
3. **São José do Rio Pardo**: Polos de tecnologia agrícola
4. **Casa Branca**: Terminal de cargas para escoamento de grãos

## 🚀 Como Executar

### No Google AI Studio

1. Acesse o link: https://aistudio.google.com/apps/drive/1HCswQBaOYAcpXJQyeN65kxENsivlPQd-
2. Clique em "Preview" para visualizar
3. Clique em "Code" para ver o código
4. Use "Copy app" para criar sua versão

### Localmente (Futuro)

Quando exportado do AI Studio:

```bash
# Instalar dependências
npm install

# Executar em desenvolvimento
npm start

# Build para produção
npm run build
```

## 📖 Referências

- [Documentação Completa - GitHub](https://github.com/lucasleonardomosca-afk/pardal-regional-intelligence)
- [Código Fonte - Google AI Studio](https://aistudio.google.com/apps/drive/1HCswQBaOYAcpXJQyeN65kxENsivlPQd-)
- [Inspiração: The News](https://thenewsletter.beehiiv.com/)
- [Inspiração: The Brief](https://thebrief-newsletter.beehiiv.com/)

## 🔧 Stack Tecnológico

- **Frontend**: React, TypeScript
- **Styling**: CSS-in-JS (inline styles no AI Studio)
- **State Management**: React Hooks (useState, useEffect)
- **Backend (Futuro)**: Firebase (Auth, Firestore, Storage)
- **Hospedagem**: Google AI Studio Apps

## 📝 Notas de Implementação

### Estado da Aplicação

A aplicação usa gerenciamento de estado simples com React Hooks:

```typescript
const [view, setView] = useState<'homepage' | 'article'>('homepage');
const [activeArticle, setActiveArticle] = useState<Article | null>(null);
const [scrollY, setScrollY] = useState(0);
```

### Navegação

Navegação baseada em estado com scroll restoration:

```typescript
const handleArticleClick = (article: Article) => {
  setActiveArticle(article);
  setView('article');
  window.scrollTo(0, 0);
};

const handleBackToHomepage = () => {
  setView('homepage');
  setActiveArticle(null);
  window.scrollTo(0, lastScrollY);
};
```

### Responsividade

CSS inline com media queries para adaptação responsiva:

```css
/* Mobile: Coluna única */
@media (max-width: 640px) {
  grid-template-columns: 1fr;
}

/* Tablet: 2 colunas */  
@media (min-width: 641px) and (max-width: 1024px) {
  grid-template-columns: repeat(2, 1fr);
}

/* Desktop: 3 colunas */
@media (min-width: 1025px) {
  grid-template-columns: repeat(3, 1fr);
}
```


## 🏗️ Nova Arquitetura Atualizada (2025)

### Estrutura de Componentes Atomic Design

O código foi completamente refatorado seguindo o padrão Atomic Design:

#### 🔹 Atoms (Componentes Básicos)
- **SerifHeading**: Títulos em fonte serif editorial
- **Text**: Textos em fonte sans-serif
- **Divider**: Separadores visuais
- **Link**: Links com estilo editorial

#### 🔸 Molecules (Combinações)
- **ArticleCard**: Cartão de artigo com imagem, título, lead e metadados
- **NewsletterHeader**: Cabeçalho com branding Pardal
- **BriefingCard**: Cartão compacto para briefings rápidos
- **CategoryBadge**: Badge de categoria com cor
- **PairingBadge**: Badge de pareamento de categoria

#### 🔷 Organisms (Seções Completas)
- **Molecules.tsx**: Arquivo com todos os molecules
- **Organisms.tsx**: Arquivo com todos os organisms
- **Pages.tsx**: Páginas completas (EditionPage, ArticlePage, LedgerPage)

### 📋 Novos Arquivos no Projeto

```
pardal-regional-intelligence/
├── App.tsx                 # Componente principal
├── constants.ts           # Constantes e configurações
├── index.html             # Template HTML
├── index.tsx              # Entry point
├── Molecules.tsx          # Molecules (ArticleCard, etc.)
├── Organisms.tsx          # Organisms (seções completas)
├── Pages.tsx              # Pages (EditionPage, ArticlePage)
├── Themes.tsx             # Sistema de temas
├── UI.tsx                 # Atoms (SerifHeading, Text, etc.)
├── Views.tsx              # Gerenciamento de views
└── metadata.json         # Metadados do AI Studio
```

### 🎨 Sistema de Temas (Themes.tsx)

Implementa temas claro, escuro e modo A+ (acessibilidade):

```typescript
- light: Fundo off-white (#FAFAF9), texto escuro
- dark: Fundo escuro (#171717), texto claro  
- a11y: Modo A+ com contraste aumentado e tipografia 20% maior
```

### 📊 Interface Article Atualizada

```typescript
export type City = 'São João' | 'Mococa' | 'Rio Pardo' | 'Casa Branca' | 'Regional' | 'Global';
export type View = 'threshold' | 'edition' | 'article' | 'ledger' | 'governance';
export type Filter = 'Power' | 'The Harvest' | 'Enterprise' | 'Urbanity' | 'The Pulse' | 'Constitution';

interface Source {
  name: string;
  url: string;
}

interface Patron {
  id: string;
  name: string;
  role: string;
  tagline: string;
}

interface Briefupdate {
  slug: string;
  title: string;
  impact: string;
}

interface Article {
  id: string;
  slug: string;
  title: string;
  lead: string;
  city: City;
  pillar: Filter;
  format: ArticleFormat[];
  context: string[];
  sources: Source[];
  update: boolean;
  pairedId?: string;
  volumeId: string;
}

interface Edition {
  id: string;
  releaseDate: string;
  viewsAfterH: string;
  bigstory: string[];
  articleIds: string[];
  volumeId: string;
}
```

### 🔀 Fluxo de Navegação

Sistema baseado em Views:

1. **Threshold**: Entrada editorial (hero com frase de boas-vindas)
2. **Edition**: Homepage com grade de artigos
3. **Article**: Visualização completa do artigo
4. **Ledger**: Registro/histórico de edições
5. **Governance**: Governança e categorias

### 🎯 Mock Data PATRIÓNIOS

Nova estrutura de dados regionais:

- **Cooperativa Agro-Mantiqueira** (Volume Patron)
- **Laticiciano Regional** (Pareamento)
- Artigos com fontes, contexto e updates
- Sistema de briefings por categoria

### 🛠️ Utilitários e Helpers

```typescript
// constants.ts
- PATRIÓNIOS: Array de patrocinadores
- ARTICLES: Mock data completo de artigos
- Helpers de filtragem e busca
```
---

**👁️ Para visualizar o código completo, acesse o [Google AI Studio](https://aistudio.google.com/apps/drive/1HCswQBaOYAcpXJQyeN65kxENsivlPQd-)**
