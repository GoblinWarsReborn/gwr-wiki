# Game Design Document
## Goblin Wars Reborn

**Versão:** 1.0  
**Data:** Janeiro 2026  
**Status:** Em Desenvolvimento

---

## 1. VISÃO GERAL DO JOGO

### 1.1 Conceito Principal
Goblin Wars Reborn é um jogo NFT Play-to-Earn baseado em blockchain que combina elementos de RPG, estratégia e economia descentralizada. Os jogadores coletam, criam e gerenciam Goblins NFT únicos, cada um com atributos genéticos distintos, participando de missões, crafting, combate e uma economia player-driven.

### 1.2 Gênero
- RPG/Strategy
- Play-to-Earn
- NFT-Based Game
- Blockchain Game

### 1.3 Plataformas
- **Fase 1:** Web Browser
- **Fase 2:** Android e iOS
- **Fase 3:** A ser definido

### 1.4 Público-Alvo
- Jogadores de NFT e Blockchain
- Entusiastas de criptomoedas
- Jogadores de RPG e estratégia
- Investidores em Play-to-Earn

### 1.5 Principais Diferenciais
- Sistema genético complexo com 7.776 variações únicas
- Economia interdependente baseada em especialização
- Sistema de crafting profundo
- Integração blockchain com múltiplos tokens
- Sistema de breeding com herança genética

---

## 2. MECÂNICAS DE JOGO

### 2.1 Sistema de Atributos

O jogo possui 6 atributos principais, divididos em físicos e mentais:

#### 2.1.1 Atributos Físicos
- **Força (FOR):** Determina capacidade de usar armas pesadas e realizar mineração
- **Agilidade (AGI):** Necessária para usar armas leves e armaduras ágeis
- **Vigor (VIG):** Requerido para armaduras pesadas e trabalhos de fundição

#### 2.1.2 Atributos Mentais
- **Inteligência (INT):** Essencial para magia e crafting de armaduras
- **Carisma (CHA):** Necessário para instrumentos musicais (bardos)
- **Percepção (PER):** Requerida para armas de longo alcance

#### 2.1.3 Papel dos Atributos
- Atributos não impactam diretamente o combate
- Definem quais equipamentos o Goblin pode utilizar
- Determinam quais habilidades podem ser aprendidas
- Criam especialização e interdependência entre jogadores

### 2.2 Sistema Genético e Raças

#### 2.2.1 Partes do Corpo
Cada Goblin possui 5 partes do corpo que influenciam atributos:
- Pele
- Cabelo
- Orelha
- Olhos
- Boca

**Variações Únicas:** 7.776 combinações possíveis por raça

#### 2.2.2 Raças de Goblins

##### Forest Goblin
- **Tema:** Protetores da natureza e dos animais
- **Aparência:** Verde padrão, cabelos vermelhos
- **Modificadores:** +INT +AGI -VIG -PER
- **Arquétipo:** Mago ágil

##### Desert Goblin
- **Tema:** Nômades do deserto
- **Aparência:** Amarelado, cabelos marrons, pele ressecada, piercings
- **Modificadores:** +PER +AGI -CHA -FOR
- **Arquétipo:** Arqueiro ágil

##### Cave Goblin
- **Tema:** Isolados e perturbados das cavernas
- **Aparência:** Brancos albinos, olhos fundos, aparência animalesca
- **Modificadores:** +VIG +CHA -AGI -PER
- **Arquétipo:** Tank carismático

##### Mountain Goblin
- **Tema:** Fortes e brutais das montanhas
- **Aparência:** Vermelhos, olhos raivosos e brutos
- **Modificadores:** +FOR +VIG -INT -CHA
- **Modificadores:** Guerreiro resistente

##### Dark Goblin
- **Tema:** Obscuros e trevosos
- **Aparência:** Pele escura, olhos vermelhos
- **Modificadores:** +FOR +CHA -AGI -INT
- **Arquétipo:** Lutador carismático

##### Sea Goblin
- **Tema:** Aventureiros e piratas dos mares
- **Aparência:** Pele azul, cabelos com dreads
- **Modificadores:** +FOR +CHA -AGI -INT
- **Arquétipo:** Pirata carismático

#### 2.2.3 Sistema de Herança Genética

O breeding segue as seguintes probabilidades:
- **39%** - Característica do pai
- **39%** - Característica da mãe
- **5%** - Característica recessiva do avô paterno
- **5%** - Característica recessiva da avó paterna
- **5%** - Característica recessiva do avô materno
- **5%** - Característica recessiva da avó materna
- **2%** - Mutação aleatória

**Nota:** As partes do corpo podem fornecer vantagens/desvantagens adicionais (a ser implementado).

### 2.3 Sistema de Combate

#### 2.3.1 Mecânica de Combate
- Atributos servem como **requisitos** para equipamentos, não afetam dano diretamente
- Combate é determinado por **armas e armaduras**
- Sistema baseado em equipamentos, não em stats

#### 2.3.2 Relação Equipamento-Atributo

| Tipo de Equipamento | Atributo Requerido |
|---------------------|-------------------|
| Machados | Força |
| Adagas | Agilidade |
| Armaduras Pesadas | Vigor |
| Cajados Mágicos | Inteligência |
| Arcos e Bestas | Percepção |
| Arpas/Guitarras | Carisma |

#### 2.3.3 Modalidades de Combate
- **PVE:** Missões contra inimigos controlados pelo jogo (Fase 1)
- **PVP:** Combate entre jogadores (Fase 2)
- **Combate Interativo:** Sistema animado (Fase 2)

### 2.4 Sistema de Crafting

#### 2.4.1 Conceito Central
O crafting é o núcleo do gameplay, criando uma economia interdependente onde nenhum jogador é autossuficiente.

#### 2.4.2 Habilidades de Crafting
- Cada Goblin pode aprender um **número limitado de habilidades**
- Habilidades requerem **atributos mínimos**
- Exemplo: Mineração requer FOR ≥ 3

#### 2.4.3 Cadeia de Produção

**Exemplo de Interdependência:**
1. Goblin com alta FOR minera pepitas
2. Goblin com alto VIG funde pepitas em barras
3. Goblin com alta INT forja armaduras

#### 2.4.4 Regras de Equipamentos
- **Soul-Bound:** Equipamentos vinculam-se ao Goblin após primeira equipagem
- **NFT Separado:** Equipamentos podem ser tokens separados (implementação futura)
- **Upgradeável:** Equipamentos podem ser melhorados via:
  - Encantamentos
  - Reforço
  - Joias e gemas encantadas
  - Afiação
- **Dificuldade Progressiva:** Quanto melhor o item, mais difícil melhorá-lo
- **Fundibilidade:** Itens são fundíveis; equipamentos são não fundíveis

### 2.5 Sistema de Missões e Trabalhos

#### 2.5.1 Missões Diárias
- Sistema de progressão diária com recompensas
- Requer número específico de Goblins
- Tempo de conclusão variável
- Barra de progresso com recompensa final (tesouro)

#### 2.5.2 Trabalhos
- Agrupados por categoria
- Requerem materiais e ferramentas específicas
- Sistema de quantidade (múltiplas unidades)
- Tempo de execução variável

---

## 3. ECONOMIA E TOKENOMICS

### 3.1 Estrutura de Tokens

#### 3.1.1 Token de Governança
**Goblin Hero Soul (GOB)**
- **Supply:** 300.000.000 (fixo)
- **Função:** Governança e staking
- **Disponível:** PancakeSwap, Uniswap, Gate.io

#### 3.1.2 Token de Utilidade
**Goblin Rush Gold Bar (GRGB)**
- **Supply:** Infinito
- **Função:** Moeda in-game
- **Obtenção:** Farming, missões, crafting

#### 3.1.3 NFTs
- **Goblin NFT:** Personagens únicos
- **Equipment NFT:** Equipamentos (implementação futura)

### 3.2 Token Allocation (GOB)

| Categoria | Percentual | Vesting |
|-----------|-----------|---------|
| Team | 20% | 2 anos |
| Partners | 10% | 2 anos |
| Advisors | 10% | 2 anos |
| DEX Liquidity | 1% | - |
| Marketing | 10% | - |
| Farming Out-of-Game | TBD | - |
| Farming In-Game | TBD | - |
| AirDrop | TBD | - |
| Staking | TBD | - |

### 3.3 Modelo de Sustentabilidade

#### 3.3.1 Fontes de Receita
1. **Taxas de Marketplace**
   - Comissão sobre vendas de Goblins
   - Comissão sobre vendas de equipamentos
   - Comissão sobre vendas de itens

2. **Venda de Terrenos**
   - Terrenos virtuais no metaverso (Fase 2+)

3. **Venda de GOB**
   - ICO/IDO
   - Vesting progressivo

### 3.4 Sistema de Cloud Wallet

- Carteira gerenciada pelo sistema
- Integração com Metamask
- Opções de resgate para carteiras externas
- Acesso rápido via interface do jogo

---

## 4. PROGRESSÃO E GAMEPLAY LOOPS

### 4.1 Loop Primário
```
Obter Goblins → Equipar → Missões → Farmear Recursos → 
Crafting → Melhorar Equipamentos → Missões Avançadas
```

### 4.2 Loop Secundário
```
Breeding → Goblins com Atributos Específicos → 
Aprender Habilidades → Especialização → Economia Player-Driven
```

### 4.3 Loop Terciário
```
Acumular GRGB → Converter para GOB → Staking → 
Recompensas → Reinvestir
```

---

## 5. INTERFACE E EXPERIÊNCIA DO USUÁRIO

### 5.1 Menu Principal (Persistente)

#### 5.1.1 Itens de Navegação
- Home
- Meu Exército (Lista de Goblins)
- Missões
- Trabalhos
- Itens
- Histórico
- Marketplace

#### 5.1.2 Display de Tokens
- **Gold:** Popup para forjar GWB
- **GOB:** Popup com opções de resgate e compra (PancakeSwap, Uniswap, Gate.io)
- **GWB:** Popup com opções de resgate e compra

#### 5.1.3 Conta do Usuário
- Nome da Conta
  - Cloud Wallet (Popup)
  - Configurações
    - Nome
    - Email
    - Endereço Metamask (não editável)
  - Sair

### 5.2 Páginas Principais

#### 5.2.1 Home - Landing Page
**Elementos:**
- Apresentação e descrição do projeto
- Botão de Login via Metamask
- Link para Whitepaper

#### 5.2.2 App - Dashboard Principal
**Elementos:**
- Nome da conta
- Display de GWSX e GWGB (clicável para resgate)
- Barra de progresso diária com tesouro final
- Lista de missões disponíveis
  - Imagem da missão
  - Nome
  - Goblins necessários
  - Tempo requerido
- Lista de ações em progresso
  - Barra de progresso com countdown
  - Fotos dos Goblins envolvidos
  - Nome da ação
- Lista de Goblins
  - Foto
  - Nome
  - Código
  - Nível de equipamento

#### 5.2.3 Página do Goblin
**Informações:**
- Foto
- Dados completos
- Nível de equipamento
- Status (disponível/ocupado)
- Ações em progresso
- Árvore genealógica (pais e filhos)
- Habilidades
- Histórico de negociações
- Equipamentos (equipar/desequipar)

**Ações Disponíveis:**
- Treinar habilidades
- Ver trabalhos disponíveis
- Cruzar (breeding)
  - Seleção de parceiro
  - Avisos e validações
  - Confirmação

#### 5.2.4 Página de Missão
**Elementos:**
- Imagem
- Descrição detalhada
- Seletor de Goblins
- Tempo de conclusão
- Botão de iniciar

#### 5.2.5 Página de Trabalho
**Elementos:**
- Imagem
- Descrição
- Seletor de Goblins
- Materiais necessários
- Ferramentas necessárias
- Recompensas previstas
- Quantidade a ser produzida
- Tempo de execução
- Botão de iniciar

#### 5.2.6 Inventário
**Organização:**
- Agrupamento por categoria
- Imagem dos itens
- Quantidade disponível

#### 5.2.7 Página do Item
**Informações:**
- Imagem
- Descrição
- Listagem no marketplace (itens similares)
- Ação de vender
  - Campo de preço
  - Campo de quantidade
  - Informação de preço médio
  - Botão de publicar
- Opções futuras:
  - Compra rápida
  - Venda rápida
  
**Para Equipamentos:**
- Lista completa de atributos e stats

#### 5.2.8 Histórico
**Elementos:**
- Lista cronológica de ações
- Data/hora do evento
- Mensagem descritiva com links

#### 5.2.9 Marketplace
**Seções:**

**Busca de Goblins:**
- Filtros por atributos
- Filtros por habilidades
- Lista com:
  - Imagem
  - Nome
  - Código
  - Nível de equipamento
  - Preço
- Link para página do Goblin (somente visualização + preço)

**Busca de Matéria-Prima:**
- Filtro por palavra-chave
- Filtro por tipo
- Link para página do item (somente visualização + preço)

**Busca de Equipamentos:**
- Filtro por palavra-chave
- Filtro por tipo
- Filtro por atributos
- Link para página do equipamento (somente visualização + preço)

---

## 6. ROADMAP DE DESENVOLVIMENTO

### 6.1 Fase 1 - Fundação (Q1-Q2 2026)

#### Completado ✓
- Conceito do Projeto
- Web browser game
- Integração Metamask
- Sistema PVE básico

#### Em Desenvolvimento
- Mecanismo completo do jogo
- Design dos Goblins
- Design da interface
- Landing Page
- Whitepaper release
- Social Mídia

**Meta:** Lançamento do MVP com funcionalidades core

### 6.2 Fase 2 - Expansão (Q3-Q4 2026)

#### Planejado
- Staking de token de governança
- Cloud Wallet implementation
- Combate interativo com animações
- Sistema PVP
- Venda de terrenos (metaverse)
- Engine de jogo animada
- App Android
- App iOS

#### Marketing
- Instagram/Facebook Ads
- Press Release Articles
- Parcerias com influenciadores

**Meta:** Expansão multiplataforma e crescimento da base de usuários

### 6.3 Fase 3 - Metaverso (2027+)

#### A Definir
- Expansão do metaverso
- Novas features de gameplay
- Integrações cross-chain
- Eventos e torneios
- Guilds e sistemas sociais

---

## 7. TECNOLOGIAS E PLATAFORMAS

### 7.1 Blockchain
- **Smart Contracts:** A definir (Ethereum/BSC/Polygon)
- **Wallet Integration:** Metamask
- **NFT Standard:** ERC-721 ou similar

### 7.2 Frontend
- Web browser (HTML5/JavaScript)
- Mobile (iOS/Android - Fase 2)

### 7.3 Backend
- Sistema de cloud wallet
- Banco de dados para histórico e cache
- API para marketplace

### 7.4 Game Engine
- Web-based game engine
- Animation engine (Fase 2)

---

## 8. CONSIDERAÇÕES FINAIS

### 8.1 Riscos e Mitigações
- **Risco:** Complexidade do sistema genético
  - **Mitigação:** Implementação gradual e testes extensivos

- **Risco:** Balanceamento econômico
  - **Mitigação:** Simulações e ajustes dinâmicos

- **Risco:** Adoção de usuários
  - **Mitigação:** Marketing agressivo e incentivos early adopter

### 8.2 Métricas de Sucesso
- Número de jogadores ativos diários (DAU)
- Volume de transações no marketplace
- Valor total bloqueado (TVL) em staking
- Taxa de retenção de jogadores
- Volume de breeding e crafting

### 8.3 Próximos Passos
1. Finalizar design dos Goblins
2. Completar mecânicas de jogo
3. Desenvolver whitepaper detalhado
4. Preparar materiais de marketing
5. Lançamento do MVP

---

**Documento Vivo:** Este GDD será atualizado conforme o desenvolvimento progride e novas features são definidas.

**Versão:** 1.0 | **Última Atualização:** Janeiro 2026