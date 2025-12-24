# Pardal - Regional Intelligence Platform

## 📰 Visão Geral

**Pardal** é uma plataforma editorial de inteligência regional inspirada em publicações como *The News* e *The Brief*. O projeto representa um sistema de newsletter editorial projetado para leitura profunda, clareza editorial e experiência de consumo livre de distrações.

## 🎯 Propósito

Transformar o Pardal em um mecanismo de newsletter editorial focado em:

- Consumo profundo de conteúdo
- Claridade editorial
- Experiência de leitura sem distrações
- Alta relação sinal-ruído
- Design responsivo explícito (mobile, tablet, desktop)

## 📐 Arquitetura do Sistema

### Frontend
- **Framework**: React (compatível com Google AI Studio Apps)
- **Arquitetura**: Atomic Design (Atoms → Molecules → Organisms → Pages)
- **Gerenciamento de Estado**: Context + Hooks (sem estado global complexo)
- **Estilo**: Sistema de tokens de design editorial

### Backend (Conceitual)
- **Firebase**: Authentication, Firestore, Storage
- **Coleções**: Articles, Sections, Authors, Sponsored Content
- **Segurança**: Regras de acesso editorial e permissões granulares

## 📁 Estrutura de Pastas

```
/components
  /atoms       – Elementos de responsabilidade única
  /molecules   – Combinações de átomos
  /organisms   – Seções autocontidas de página
  /pages       – Montagem final de componentes
/hooks         – Lógica reutilizável
/services      – Interfaces para dados externos
/types         – Interfaces e Enums do domínio
/constants     – Tokens de design e configuração
```

## 🖼️ Sistema Visual

### Tipografia
- **Serif Editorial**: Crimson Pro (manchetes, narrativas longas)
- **Sans-Serif Funcional**: Inter (metadados, UI)
- **Escala Tipográfica**: Sistema modular fluido

### Paleta de Cores
- **Modo Claro**: Fundo off-white, texto cinza escuro
- **Modo Escuro**: Fundo cinza escuro, texto off-white
- **Acentos**: Azul suave (confiança), vermelho editorial (urgência)

### Responsividade

#### Mobile (320px - 767px)
- Layout em coluna única (100% largura)
- Tipografia fluida e otimizada para leitura

#### Tablet (Edição - 1024px)
- Grade assimétrica de 2 colunas
- Layout "Golden Ratio" (66% narrativa / 34% pulse)
- Navegação persistente mas discreta

#### Desktop (1025px+)
- Grade sofisticada de 12 colunas
- "The Great Margin" – 8 de 12 colunas para texto
- Navegação utilitária permanente
- Descoberta multi-direcional

## 🔗 Acesso ao Código Fonte Completo

### Google AI Studio
O código-fonte completo desta aplicação está disponível no Google AI Studio:

🔗 **[Abrir no Google AI Studio](https://aistudio.google.com/apps/drive/1HCswQBaOYAcpXJQyeN65kxENsivlPQd-)**

### Arquivos Principais
- `App.tsx` – Componente React principal com toda lógica da aplicação
- `index.tsx` – Entry point da aplicação React
- `index.html` – Template HTML base com configuração de viewport
- `metadata.json` – Metadados do Google AI Studio e configuração

## 📱 Como Usar

1. **Acesse o Google AI Studio**: Clique no link acima
2. **Visualize o Preview**: Veja a aplicação rodando
3. **Explore o Código**: Navegue pelos arquivos na aba "Code"
4. **Faça uma Cópia**: Use "Copy app" para criar sua própria versão

## 🚀 Fases de Desenvolvimento

### Fase 1 - Compreensão do Produto
✅ Definição de audiência e posicionamento editorial
✅ Fluxos de leitura principai
✅ Critérios de sucesso para experiência de leitura

### Fase 2 - Homepage Ideal (Mental Wireframe)
✅ Hierarquia de conteúdo
✅ Fluxo de leitura por viewport
✅ Uso de espaço em branco
✅ Elementos de atenção vs silenciosos

### Fase 3 - Sistema Visual & Editorial
✅ Sistema tipográfico
✅ Paleta de cores alinhada à marca
✅ Design tokens
✅ Estratégia de modo claro/escuro
✅ Modo A+ de acessibilidade
✅ Princípios de movimento

### Fase 4 - Estratégia Responsiva
✅ Atomic Design (Atoms → Molecules → Organisms → Pages)
✅ Mobile-first com progressive enhancement
✅ Navegação adaptativa
✅ Estratégia de escalabilidade

### Fase 5 - Dados & Conteúdo
✅ Estrutura de artigos regionais
✅ Mock data completo com artigos regionais
✅ Estratégia de carregamento
✅ Queries finitas otimizadas

### Fase 6 - Desenvolvimento & Refinamento
✅ Refinamento de componentes
✅ Refinamento de segurança e performance
✅ Iterações baseadas em feedback
✅ Estratégia de testes A/B
✅ Métricas de engajamento e conversão

### Fase 7 - Documentação & Plano de Execução
✅ Visão geral do sistema
✅ Resumo da arquitetura
✅ Roadmap de execução faseado
✅ Mapeamento de métricas práticas

## 💡 Princípios de Design

### Editorial-First
- A experiência de leitura é a UX primária
- Acessibilidade e legibilidade são recursos de primeira classe
- Clareza editorial sobre ruído visual

### Composição sobre Herança
- Componentes pequenos e combináveis
- Separação clara de responsabilidades
- Fluxo explícito de dados

### Responsividade Intencional
- Design baseado em postura de leitura
- Nunca "responsive por acidente"
- Cada viewport tem propósito editorial

## 🎨 Recursos Adicionais

- **Inspirações**: The News, The Brief
- **Frameworks**: React, Google AI Studio Apps
- **Backend**: Firebase (Auth, Firestore, Storage)

## 🎯 Público-Alvo

- Leitores intelectualmente curiosos
- Profissionais buscando contexto sobre manchetes
- Usuários experimentando fadiga de informação
- Quem valoriza jornalismo de alta qualidade

## 🔒 Segurança

- Autenticação via Firebase
- Permissões granulares por função (author, editor)
- Integridade de esquema com validação obrigatória
- Queries finitas otimizadas

## 📊 Escalabilidade

- Sem joins (dados desnormalizados)
- Indexação por publicidade e status
- Performance útil mesmo com 10,000+ artigos

---

## 🆕 Atualização 2025 - Arquitetura Atomic Design

### Nova Estrutura de Componentes

A aplicação foi reestruturada seguindo os princípios do **Atomic Design**, com uma organização clara e modular:

#### Atoms (Elementos Básicos)
- `Button`, `Input`, `Label`, `Icon`
- Componentes mínimos e reutilizáveis
- Sem lógica de negócio

#### Molecules (Combinações Simples)
- `ArticleCard`, `CitySelector`, `FilterBar`
- Combinam atoms para criar funcionalidades específicas
- Exportadas via `Molecules.tsx`

#### Organisms (Seções Complexas)
- `Header`, `ArticleGrid`, `EditionViewer`
- Seções autocontidas da aplicação
- Gerenciam estado local quando necessário
- Exportadas via `Organisms.tsx`

#### Pages (Views Completas)
- `ThresholdPage`, `EditionPage`, `ArticlePage`, `LedgerPage`, `GovernancePage`
- Views completas com toda lógica de apresentação
- Exportadas via `Pages.tsx`

### Arquivos Principais

```
App.tsx           – Componente raiz e gerenciamento de estado global
constants.ts      – Tokens de design e configuração
Molecules.tsx     – Export centralizado de molecules
Organisms.tsx     – Export centralizado de organisms
Pages.tsx         – Export centralizado de pages
Themes.tsx        – Sistema de temas e design tokens
UI.tsx            – Componentes UI básicos
Views.tsx         – Sistema de navegação entre views
```

### Sistema de Navegação

A aplicação utiliza um sistema de **5 views** principais:

1. **Threshold** (Entrada editorial): Seleção de cidade
2. **Edition** (Edição regional): Lista de artigos
3. **Article** (Leitura profunda): Artigo completo
4. **Ledger** (Arquivo histórico): Edições passadas
5. **Governance** (Gestão editorial): Painel administrativo

### Dados Mockados - Sistema PATRIÓNIOS

O app agora usa um sistema de dados mockados completo baseado em **Patrimônios Culturais Brasileiros**:

- **3 Regiões**: Norte (Manaus), Nordeste (Salvador), Sul (Porto Alegre)
- **15 Artigos** por região (total: 45 artigos)
- **Categorias**: Cultural, Histórico, Ambiental, Turístico, Gastronômico
- **Metadados**: Autor, data, categoria, estimativa de leitura

### Interfaces TypeScript

```typescript
interface City {
  id: string;
  name: string;
  region: string;
}

interface View {
  type: 'threshold' | 'edition' | 'article' | 'ledger' | 'governance';
  data?: any;
}

interface Filter {
  category?: string;
  author?: string;
  dateRange?: { start: Date; end: Date };
}

interface Article {
  id: string;
  title: string;
  author: string;
  date: string;
  category: string;
  city: string;
  summary: string;
  content: string;
  readTime: string;
}

interface Edition {
  id: string;
  city: string;
  date: string;
  articles: Article[];
}
```

### Próximos Passos

Para continuar o desenvolvimento:

1. **Backend Real**: Integração com Firebase/Firestore
2. **Autenticação**: Sistema de login e permissões
3. **Editor CMS**: Interface para criação de conteúdo
4. **Notificações**: Sistema de alertas e newsletters
5. **Analytics**: Métricas de engajamento e leitura

---

Para acessar o código fonte completo e atualizado, visite:
🔗 **[Google AI Studio - Pardal App](https://aistudio.google.com/apps/drive/1HCswQBaOYAcpXJQyeN65kxENsivlPQd-)**
