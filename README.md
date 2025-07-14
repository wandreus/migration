# Estimativa de Migração: ASICS Legacy → VTEX FastStore

## Resumo

Este documento apresenta a estimativa técnica para migração do projeto **asics-br-refactory** (VTEX Legacy) para **VTEX FastStore v2+**. A análise considera a complexidade arquitetural, integrações específicas e particularidades da marca ASICS.

### Estimativa Geral
- **Tempo Total Estimado**: 22-27 semanas
- **Complexidade**: Média-Alta  
- **Risco**: Médio
- **Esforço**: ~896-1.064 horas

### Benefícios do FastStore Template Base
✅ **Autenticação VTEX ID** já integrada  
✅ **Login/Register** com fluxo completo  
✅ **Checkout básico** implementado  
✅ **APIs VTEX** pré-configuradas  
✅ **Componentes core** (Header, Footer, Product)  
✅ **SEO e Performance** otimizados  
✅ **Responsividade** mobile-first

### O que o Template FastStore Inclui:
🏗️ **Arquitetura Completa**: Next.js + TypeScript + React configurados  
🔌 **Integrações VTEX**: GraphQL, Checkout, OMS, PIM já funcionando  
🎨 **Design System**: Componentes base estilizáveis e customizáveis  
📱 **PWA Ready**: Service workers e cache otimizado  
🚀 **Performance**: SSR/SSG, lazy loading, otimizações automáticas  
🔍 **SEO**: Meta tags, structured data, sitemap gerados  
🛒 **E-commerce Core**: PDP, PLP, Cart, Search funcionais  
👤 **Account System**: Login, orders, profile integrados

---

## Metodologia de Estimativa

### Critérios Técnicos
- **Complexidade Arquitetural**: Migração de templates HTML → componentes React
- **Integrações**: APIs externas (RetailRocket, Trustvox, OneASICS)
- **Funcionalidades Específicas**: Recursos únicos da marca ASICS
- **Responsividade**: Adaptação mobile-first
- **Performance**: Otimização SSR/SSG
- **SEO**: Manutenção de estrutura e meta tags

### Escala de Complexidade
- **Simples (1-2 semanas)**: Componentes básicos, páginas estáticas
- **Média (3-5 semanas)**: Funcionalidades com integrações
- **Complexa (6-8 semanas)**: Sistemas críticos com múltiplas integrações
- **Muito Complexa (8+ semanas)**: Funcionalidades únicas/críticas

---

## Estimativas Detalhadas por Categoria

### 🔐 Account (8-10 semanas)

| Funcionalidade | URL | Estimativa | Justificativa Técnica |
|---|---|---|---|
| **Login/Register** | `/login` | 1-2 semanas | ✅ **Template base** - Apenas customização visual ASICS |
| **MyVouchers** | `/account/my-vouchers` | 1-2 semanas | ✅ **Account base** - Adicionar funcionalidade específica |
| **Orders** | `/account#/profile` | 2-3 semanas | ✅ **OMS integrado** - Customizar layout e dados |
| **Wallet (OneASICS)** | `/account/wallet` | 2-3 semanas | Sistema cashback proprietário, integração financeira |
| **Wishlist** | `/account/wishlist` | 1 semana | ✅ **Template base** - Customização visual apenas |

**Complexidade Account Reduzida**: 
- ✅ VTEX ID já integrado no template
- ✅ Autenticação/autorização funcionando
- ✅ APIs VTEX pré-configuradas
- 🔧 Customização visual/UX ASICS
- 🔧 Integração sistema OneASICS (única complexidade)

---

### 🏢 Institucional (6-8 semanas)

| Funcionalidade | URL | Estimativa | Justificativa Técnica |
|---|---|---|---|
| **Central Relacionamento** | `/ajuda/central-relacionamento` | 1-2 semanas | Página estática com formulários de contato |
| **Regulamentos/Políticas** | `/institucional#/regulamentos` | 1-2 semanas | Conteúdo estático, estrutura de navegação |
| **Guia de Medidas** | `/ajuda/guia-medidas` | 2 semanas | Tabelas interativas, cálculos de tamanho |
| **Lojas** | `/ajuda/lojas` | 1-2 semanas | Mapa interativo, integração Google Maps |
| **Páginas de Erro** | `/Sistema/404` | 1 semana | Componentes de erro, redirecionamentos |

**Complexidade Institucional**:
- Migração de conteúdo estático para CMS
- Componentes de formulário padronizados
- Integração com mapas e serviços externos

---

### 🎯 Landing Pages & Campanhas (12-14 semanas)

| Funcionalidade | URL | Estimativa | Justificativa Técnica |
|---|---|---|---|
| **OneASICS** | `/oneasics` | 3 semanas | Sistema cashback, animações, integração wallet |
| **Sustentabilidade** | `/institucional/sustentabilidade` | 2 semanas | Conteúdo rico, animações, timeline interativa |
| **ASICS Bag** | `/asicsbag` | 2-3 semanas | Campanha temporária, QR codes, integração mobile |
| **Black Friday** | `/asics-black-friday` | 2-3 semanas | Countdown, ofertas dinâmicas, alta performance |
| **Sportstyle** | `/asics-sportstyle` | 2 semanas | Landing rica, carrosséis, galeria produtos |
| **CPS Tennis** | `/cps-tennis` | 2 semanas | Conteúdo esportivo específico, vídeos, animações |
| **Lançamentos** | `/lancamento/gel-nimbus-26` | 2-3 semanas | Template reutilizável, CMS para novos produtos |

**Complexidade Landing Pages**:
- Animações e interações complexas
- Performance otimizada para campanhas
- Integração com sistemas de promoção
- Templates reutilizáveis via CMS

---

### 📝 Blog (4-5 semanas)

| Funcionalidade | URL | Estimativa | Justificativa Técnica |
|---|---|---|---|
| **Blog Home** | `/asicsblog` | 2 semanas | Listagem posts, filtros, paginação |
| **Categorias** | `/asicsblog/corrida` | 1-2 semanas | Filtros por categoria, SEO otimizado |
| **Post Individual** | `/asicsblog/corrida/treino-em-dupla` | 1-2 semanas | Renderização markdown, compartilhamento social |

**Complexidade Blog**:
- Sistema de CMS para conteúdo
- SEO otimizado com meta tags dinâmicas
- Integração com redes sociais

---

### 🛍️ E-commerce Core (6-8 semanas)

| Funcionalidade | URL | Estimativa | Justificativa Técnica |
|---|---|---|---|
| **PDP** | `/1013a142-402/p` | 3-4 semanas | ✅ **PDP base** - Customizar galeria, specs, adicionar comparador |
| **PLP/Busca** | `/busca?ft=Nimbus+27` | 2-3 semanas | ✅ **Search base** - Customizar filtros e layout ASICS |
| **Categoria** | `/calcados/corrida` | 1 semana | ✅ **Template pronto** - Apenas ajustes visuais |
| **Departamento** | `/calcados` | 1 semana | ✅ **Template pronto** - Customização mínima |

**Complexidade E-commerce Reduzida**:
- ✅ APIs GraphQL já configuradas
- ✅ Performance otimizada no template
- ✅ Componentes base funcionando
- 🔧 Customização visual ASICS
- 🔧 Integração Trustvox e RetailRocket

---

### 🏪 Sistema Totem (8-10 semanas)

| Funcionalidade | URL | Estimativa | Justificativa Técnica |
|---|---|---|---|
| **Totem Home** | `/totem/loja/rio-sul` | 2 semanas | Interface específica para touchscreen |
| **Totem Menu** | `/totem/loja/rio-sul/menu` | 1-2 semanas | Navegação otimizada para totem |
| **Totem OneASICS** | `/totem/loja/rio-sul/oneasics` | 2 semanas | Integração cashback em loja física |
| **Totem Quiz** | `/totem/loja/rio-sul/quiz` | 1-2 semanas | Sistema de recomendação interativo |
| **Totem Comparador** | `/totem/loja/rio-sul/comparador` | 2 semanas | Comparação produtos em tela grande |
| **Totem NPS/Roleta** | `/totem/loja/rio-sul/nps` | 1-2 semanas | Gamificação e pesquisa satisfação |

**Complexidade Totem**:
- Interface adaptada para dispositivos touchscreen
- Integração com sistemas de loja física
- Otimização para hardware específico
- Sistema offline/online híbrido

---

### 🧩 Componentes Core (4-6 semanas)

| Componente | Estimativa | Justificativa Técnica |
|---|---|---|
| **Header** | 1-2 semanas | ✅ **Template base** - Customizar menu ASICS e CEP |
| **Footer** | 0.5-1 semana | ✅ **Template base** - Apenas links institucionais ASICS |
| **Minicart** | 1-2 semanas | ✅ **Checkout base** - Customizar cupons e visual |
| **Menu Mobile** | 0.5-1 semana | ✅ **Template pronto** - Customização visual |
| **Quickview** | 1 semana | ✅ **Modal base** - Adaptar layout ASICS |
| **Comparador** | 1-2 semanas | 🔧 Funcionalidade específica a implementar |

**Complexidade Componentes Reduzida**:
- ✅ Estado global já implementado
- ✅ APIs VTEX integradas
- ✅ Responsividade configurada
- ✅ Performance otimizada
- 🔧 Customização visual/UX ASICS

---

### 📊 Integrações & Analytics (4-5 semanas)

| Sistema | Estimativa | Justificativa Técnica |
|---|---|---|
| **GA4/GTM/Datalayer** | 2-3 semanas | Migração eventos, enhanced ecommerce, conversions |
| **RetailRocket** | 1-2 semanas | Recomendações produto, tracking comportamental |
| **Trustvox** | 1 semana | Reviews e avaliações, integração API |

**Complexidade Integrações**:
- Migração de eventos jQuery para React
- Manutenção de tracking existente
- Performance sem impacto na UX

---

## Cronograma de Implementação ⚡ Acelerado com Template

### Fase 1: Setup & Customização Base (Semanas 1-6)
- ✅ Setup projeto FastStore (template already configured)
- 🔧 Customização visual ASICS (cores, fontes, layout)
- 🔧 Componentes base adaptados (Header, Footer)
- ✅ Autenticação funcionando (template base)

### Fase 2: E-commerce Core (Semanas 7-14)
- 🔧 PDP customizado (galeria, especificações)
- 🔧 PLP/Search customizado (filtros ASICS)
- 🔧 Minicart personalizado
- ✅ APIs VTEX funcionando

### Fase 3: Funcionalidades Específicas (Semanas 15-20)
- 🔧 Sistema Account customizado
- 🔧 OneASICS (cashback/wallet)
- 🔧 Blog e CMS
- 🔧 Landing pages principais

### Fase 4: Sistemas Avançados (Semanas 21-25)
- 🔧 Sistema Totem completo
- 🔧 Campanhas e hotspots
- 🔧 Integrações externas (RetailRocket, Trustvox)
- 🔧 Analytics e tracking

### Fase 5: Refinamento & Deploy (Semanas 26-27)
- ✅ Performance já otimizada
- 🔧 Ajustes de UX/UI finais
- 🔧 Deploy e monitoramento

---

## Considerações Técnicas Críticas

### Desafios da Migração

1. **Arquitetura Fundamental**
   - Legacy: Templates HTML + jQuery
   - FastStore: React SSR + TypeScript
   - **Impacto**: Reescrita completa do frontend

2. **APIs VTEX**
   - Legacy: VTEX.js (REST limitado)
   - FastStore: GraphQL + REST moderno
   - **Impacto**: Refatoração de todas integrações

3. **Estado da Aplicação**
   - Legacy: Estado DOM + localStorage
   - FastStore: React state + Context API
   - **Impacto**: Redefinição de gerenciamento de dados

4. **Integrações Externas**
   - OneASICS: Sistema proprietário de cashback
   - RetailRocket: Recomendações personalizadas
   - Trustvox: Reviews e avaliações
   - **Impacto**: Adaptação para arquitetura moderna

### Riscos Identificados

1. **Alto**: Sistema OneASICS (integração financeira)
2. **Médio**: Totem (hardware específico)
3. **Médio**: Performance (muitas integrações)
4. **Baixo**: SEO (estrutura bem definida)



## Tabela Resumo: Todas as Páginas/Funcionalidades

| Funcionalidade | URL | Categoria | Estimativa | Complexidade |
|---|---|---|---|---|
| Account - Login | `/login` | Account | 1-2 semanas ⚡ | Baixa (Template) |
| Account - MyVouchers | `/account/my-vouchers` | Account | 1-2 semanas ⚡ | Baixa (Template) |
| Account - Orders | `/account#/profile` | Account | 2-3 semanas ⚡ | Média (Template) |
| Account - Wallet (OneASICS) | `/account/wallet` | Account | 2-3 semanas ⚡ | Média |
| Account - Wishlist | `/account/wishlist` | Account | 1 semana ⚡ | Baixa (Template) |
| Central de Relacionamento | `/ajuda/central-relacionamento` | Institucional | 1-2 semanas | Baixa |
| Institucionais | `/institucional#/regulamentos` | Institucional | 1-2 semanas | Baixa |
| Guia de Medidas | `/ajuda/guia-medidas` | Institucional | 2 semanas | Média |
| OneASICS | `/oneasics` | Landing Page | 3 semanas | Alta |
| Lojas | `/ajuda/lojas` | Institucional | 1-2 semanas | Média |
| Sustentabilidade | `/institucional/sustentabilidade` | Institucional | 2 semanas | Média |
| ASICS Bag | `/asicsbag` | Campanha | 2-3 semanas | Média |
| ASICS Black Friday | `/asics-black-friday` | Campanha | 2-3 semanas | Média |
| Blog - Home | `/asicsblog` | Blog | 2 semanas | Média |
| Blog - Categorias | `/asicsblog/corrida` | Blog | 1-2 semanas | Baixa |
| Blog - Post | `/asicsblog/corrida/treino-em-dupla` | Blog | 1-2 semanas | Baixa |
| ASICS Sportstyle | `/asics-sportstyle` | Landing Page | 2 semanas | Média |
| Busca | `/busca?ft=Nimbus+27` | PLP | 2-3 semanas ⚡ | Média (Template) |
| Categoria | `/calcados/corrida` | PLP | 1 semana ⚡ | Baixa (Template) |
| Departamento | `/calcados` | PLP | 1 semana ⚡ | Baixa (Template) |
| Listas | `/lista/lancamentos` | PLP | 1-2 semanas | Média |
| Páginas de Cadastro | `/cadastro/aes` | Cadastro | 1-2 semanas | Média |
| CPS Tennis | `/cps-tennis` | Landing Page | 2 semanas | Média |
| HotSites | `/hotsite/funcionario` | Campanha | 1-2 semanas | Baixa |
| Cuidados com seu ASICS | `/Institucional/cuidados-com-seu-asics` | Landing Page | 1-2 semanas | Baixa |
| Páginas de Lançamento | `/lancamento/gel-nimbus-26` | Landing Page | 2-3 semanas | Média |
| Metaspeed-plus | `/metaspeed-plus` | Landing Page | 1-2 semanas | Baixa |
| Pesquisas-asics | `/pesquisas-asics` | Landing Page | 1-2 semanas | Baixa |
| Produto Details | `/1013a142-402/p` | PDP | 3-4 semanas ⚡ | Alta (Template) |
| Seja Franqueado | `/sejafranqueado` | Landing Page | 1-2 semanas | Baixa |
| Páginas de erro | `/Sistema/404` | Institucional | 1 semana | Baixa |
| State Of Mind Study 2024 | `/stateofmindstudy2024` | Landing Page | 2 semanas | Média |
| State Of Mind Study - Brasil | `/stateofmindstudy2024/brasil` | Landing Page | 1-2 semanas | Baixa |
| The Desk Break | `/the-desk-break` | Landing Page | 1-2 semanas | Baixa |
| Totem - Home | `/totem/loja/rio-sul` | Totem | 2 semanas | Alta |
| Totem - Menu | `/totem/loja/rio-sul/menu` | Totem | 1-2 semanas | Média |
| Totem - OneASICS | `/totem/loja/rio-sul/oneasics` | Totem | 2 semanas | Alta |
| Totem - Quiz | `/totem/loja/rio-sul/quiz` | Totem | 1-2 semanas | Média |
| Totem - Comparador | `/totem/loja/rio-sul/comparador` | Totem | 2 semanas | Alta |
| Totem - Campanhas | `/totem/loja/rio-sul/campanhas` | Totem | 1-2 semanas | Média |
| Totem - Ver todos os produtos | `/totem/loja/rio-sul/produtos` | Totem | 1 semana | Baixa |
| Totem - NPS | `/totem/loja/rio-sul/nps` | Totem | 1 semana | Baixa |
| Totem - Roleta | `/totem/loja/rio-sul/roleta` | Totem | 1 semana | Baixa |
| Home | `/` | Landing Page | 2-3 semanas ⚡ | Média (Template) |
| Header | Componente | Componente | 1-2 semanas ⚡ | Média (Template) |
| Footer | Componente | Componente | 0.5-1 semana ⚡ | Baixa (Template) |
| Minicart | Componente | Componente | 1-2 semanas ⚡ | Média (Template) |
| Menu | Componente | Componente | 0.5-1 semana ⚡ | Baixa (Template) |
| Quickview | Componente | Componente | 1 semana ⚡ | Baixa (Template) |
| Comparador | Componente | Componente | 1-2 semanas | Média |
| Rastreamento (Datalayer/GA4/GTM) | Sistema | Rastreamento | 2-3 semanas | Alta |
| Retail Rocket | Sistema | Componente | 1-2 semanas | Média |

---

## Conclusão ⚡ Otimizada com Template

A migração do projeto ASICS Legacy para FastStore com **template base** é **altamente factível** e **significativamente simplificada**, demandando **22-27 semanas** de desenvolvimento focado em customização. O template FastStore elimina a necessidade de reescrita completa, transformando o projeto em **customização visual e funcional** sobre uma base sólida.


### Benefícios Esperados Pós-Migração

1. **Performance**: Melhoria significativa em Core Web Vitals
2. **Manutenibilidade**: Código mais limpo e escalável
3. **Developer Experience**: Ferramentas modernas de desenvolvimento
4. **SEO**: Melhor indexação com SSR/SSG
5. **Escalabilidade**: Arquitetura preparada para crescimento
6. **Atualizações**: Sistema de versionamento automático FastStore
