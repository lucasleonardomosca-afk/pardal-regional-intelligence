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

## 🏗️ Arquitetura do Sistema

### Frontend
- **Framework**: React (compatível com Google AI Studio Apps)
- **Arquitetura**: Atomic Design (Atoms → Molecules → Organisms → Pages)
- **Gerenciamento de Estado**: Context + Hooks (sem estado global complexo)
- **Estilo**: Sistema de tokens de design editorial

### Backend (Conceitual)
- **Firebase**: Authentication, Firestore, Storage
- **Coleções**: Articles, Sections, Authors, Sponsored Content
- **Segurança**: Regras de acesso editorial e permissões granulares

### Estrutura de Pastas
```
/components
  /atoms       - Elementos de responsabilidade única
  /molecules   - Combinações de átomos
  /organisms   - Seções autocontidas de página
/pages         - Montagem final de componentes
/hooks         - Lógica reutilizável
/services      - Interfaces para dados externos
/types         - Interfaces e Enums do domínio
/constants     - Tokens de design e configuração
```

## 🎨 Sistema Visual

### Tipografia
- **Serif Editorial**: Crimson Pro (manchetes, narrativas longas)
- **Sans-Serif Funcional**: Inter (metadados, UI)
- **Escala Tipográfica**: Sistema modular fluido

### Paleta de Cores
- **Modo Claro**: Fundo off-white, texto cinza escuro
- **Modo Escuro**: Fundo cinza escuro, texto off-white
- **Acentos**: Azul suave (confiança), vermelho editorial (urgência)

### Modo A+ (Acessibilidade)
- Aumento de 20% na escala tipográfica
- Line-height expandido para 2.0
- Contraste alto
- Layout de coluna única

## 📱 Estratégia Responsiva

### Mobile (< 640px)
- Fluxo vertical de coluna única
- Navegação "Ghost Header"
- Alvos de toque grandes (mín. 44px)
- 100% linear

### Tablet (641px - 1024px)
- Grade assimétrica de 2 colunas
- Layout "Golden Ratio" (66% narrativa / 34% pulse)
- Navegação persistente mas discreta

### Desktop (1025px+)
- Grade sofisticada de 12 colunas
- "The Great Margin" - 8 de 12 colunas para texto
- Navegação utilitária permanente
- Descoberta multi-direcional

## 📂 Acesso ao Código Fonte Completo

### Google AI Studio
O código-fonte completo desta aplicação está disponível no Google AI Studio:

🔗 **[Abrir no Google AI Studio](https://aistudio.google.com/apps/drive/1HCswQBaOYAcpXJQyeN65kxENsivlPQd-)**

### Arquivos Principais
- `App.tsx` - Componente React principal com toda lógica da aplicação
- `index.tsx` - Entry point da aplicação React
- `index.html` - Template HTML base com configuração de viewport
- `metadata.json` - Metadados do Google AI Studio e configuração

## 🚀 Como Usar

1. **Acesse o Google AI Studio**: Clique no link acima
2. **Visualize o Preview**: Veja a aplicação rodando
3. **Explore o Código**: Navegue pelos arquivos na aba "Code"
4. **Faça uma Cópia**: Use "Copy app" para criar sua própria versão

## 📋 Fases de Desenvolvimento

### Fase 1 - Compreensão do Produto
✅ Definição da audiência e posicionamento editorial
✅ Fluxos de leitura principais
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
✅ Filosofia mobile-first
✅ Definições de breakpoints
✅ Regras de densidade de conteúdo
✅ Adaptações de navegação

### Fase 5 - Arquitetura Frontend
✅ Estrutura modular de componentes
✅ Estratégia de gerenciamento de estado
✅ Filosofia de dados e serviços
✅ Tratamento de erros e renderização segura
✅ Modelo de roteamento

### Fase 6 - Modelo de Backend & Dados
✅ Design backend baseado em Firebase
✅ Coleções Firestore
✅ Regras de segurança conceituais
✅ Estratégia de escalabilidade

### Fase 7 - Documentação & Plano de Execução
✅ Visão geral do sistema
✅ Resumo da arquitetura
✅ Roadmap de execução faseado
✅ Mapeamento de melhores práticas

## 🎓 Princípios de Design

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
- Nunca "responsivo por acidente"
- Cada viewport tem propósito editorial

## 📚 Recursos Adicionais

- **Inspiração**: The News, The Brief
- **Framework**: React, Google AI Studio Apps
- **Backend**: Firebase (Auth, Firestore, Storage)

## 👥 Público-Alvo

- Leitores intelectualmente curiosos
- Profissionais buscando contexto sobre manchetes
- Usuários experimentando fadiga de informação
- Quem valoriza jornalismo de alta qualidade

## 🔐 Segurança

- Autenticação via Firebase
- Permissões granulares por função (author, editor)
- Integridade de esquema com validação obrigatória
- Queries finitas otimizadas

## 📊 Escalabilidade

- Sem joins (dados desnormalizados)
- Indexação por publishDate e status
- Performance O(1) mesmo com 10,000+ artigos

---

**Desenvolvido com foco em excelência editorial e experiência de leitura de classe mundial.**
