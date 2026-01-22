# Sistema de Cristais - Goblins Wars

## Índice
1. [Visão Geral](#visão-geral)
2. [Como Funciona](#como-funciona)
3. [Regras de Formação](#regras-de-formação)
4. [Lista Completa de Cristais](#lista-completa-de-cristais)
5. [Sistema de Pontos](#sistema-de-pontos)
6. [Probabilidades](#probabilidades)
7. [Exemplos Práticos](#exemplos-práticos)
8. [Implementação](#implementação)
9. [Tabelas de Referência](#tabelas-de-referência)

---

## Visão Geral

O Sistema de Cristais é um mecanismo que gera cristais especiais baseados em **regras específicas e hierárquicas** de combinações genéticas.

### Princípio Fundamental

> **Sistema de Cristais Independentes por Raridade**
> 
> Cada raça pode gerar MÚLTIPLOS cristais por goblin. O sistema verifica TODAS as regras e atribui TODOS os cristais cujas regras sejam satisfeitas. Um goblin pode ter vários cristais da mesma raça (em tiers diferentes).

### Conceitos Básicos

- **60 cristais únicos**: 6 raças × 10 cristais (4 Uncommon + 3 Rare + 2 Epic + 1 Legendary)
- **Regras baseadas em partes**: Cada cristal requer genes completos ou específicos em características
- **Hierarquia de complexidade**: Legendary = 30 genes, Epic = 7-9 genes, Rare = 5-6 genes, Uncommon = 3 genes
- **Verificação completa**: Sistema verifica TODAS as regras e atribui TODOS os cristais aplicáveis
- **10 características avaliadas**: 6 físicas (Skin, Hair, Eyes, Ear, Mouth, Nose) + 4 cores (SkinColor, HairColor, PupilColor, EyeColor)
- **Múltiplos cristais por raça**: Um goblin pode ter vários cristais da mesma raça (até 10 por raça)
- **Raridade final**: Soma dos pontos de todos os cristais
- **Sem tier Common**: Sistema começa em Uncommon

---

## Como Funciona

### Processo de Formação

1. **Para cada raça** (Forest, Mountain, Desert, Sea, Cave, Dark):
   - Verificar regra **Legendary** (1 cristal) → Se satisfeita, atribui
   - Verificar regras **Epic** (2 cristais: E-01 e E-02) → Se satisfeita, atribui
   - Verificar regras **Rare** (3 cristais: R-01, R-02, R-03) → Se satisfeita, atribui
   - Verificar regras **Uncommon** (4 cristais: U-01, U-02, U-03, U-04) → Se satisfeita, atribui
   - Um goblin pode receber MÚLTIPLOS cristais da mesma raça (em tiers diferentes)

2. **Resultado**: Goblin recebe 0-60 cristais (até 10 por raça)

3. **Raridade do Goblin**: Soma dos pontos de todos os cristais formados

### Exemplo Simplificado

```
Goblin X tem genes Forest:
✓ Regra Legendary Forest NÃO satisfeita (30 genes puros)
✓ Regras Epic Forest NÃO satisfeitas (E-01: 9 genes, E-02: 7 DD)
✓ Regra Rare R-02 Forest SATISFEITA (5 DD da mesma raça)
→ Recebe: Esmeralda Trapiche (Rare R-02) - 12 pontos
✓ Regra Uncommon U-02 Forest SATISFEITA (3 DD da mesma raça)
→ Recebe: Jade Nefrita (Uncommon U-02) - 4 pontos
→ Total Forest: 2 cristais = 16 pontos

Goblin X tem genes Mountain:
✓ ... verifica todas as regras...
✓ Regra Uncommon U-02 Mountain SATISFEITA (3 DD da mesma raça)
→ Recebe: Ágata Listrada (Uncommon U-02) - 4 pontos
→ Total Mountain: 1 cristal = 4 pontos

Total: 3 cristais (Esmeralda Trapiche + Jade Nefrita + Ágata Listrada) = 20 pontos = Rare Goblin
```

---

## Regras de Formação

Cada cristal possui uma **regra específica e única**. As regras são verificadas de cima para baixo (Legendary → Epic → Rare → Uncommon).

### Legenda de Termos

- **DD**: Gene Dominante-Dominante (posição mais forte)
- **R1**: Gene Recessivo 1 (posição intermediária)
- **R2**: Gene Recessivo 2 (posição mais fraca)
- **Físicas**: Skin, Hair, Eyes, Ear, Mouth, Nose (6 características)
- **Cores**: SkinColor, HairColor, PupilColor, EyeColor (4 características)
- **Pureza**: Todas as posições (DD, R1, R2) da mesma raça em uma característica

---

### Forest (Floresta) - 10 Cristais

| Tier | ID | Nome | Pontos | Regra Específica |
|------|----|----|--------|------------------|
| **Legendary** | F-L | Esmeralda da Floresta Ancestral | 50 | **30 genes Forest** (DD + R1 + R2 em todas as 10 características) |
| **Epic** | F-E01 | Esmeralda Imperial | 22 | **3 características completas** Forest (9 genes: 3 DD + 3 R1 + 3 R2) |
| **Epic** | F-E02 | Esmeralda Colombiana | 22 | **7 DD** Forest em qualquer característica |
| **Rare** | F-R01 | Esmeralda Real | 12 | **2 características completas** Forest (6 genes: 2 DD + 2 R1 + 2 R2) |
| **Rare** | F-R02 | Esmeralda Trapiche | 12 | **5 DD** Forest em qualquer característica |
| **Rare** | F-R03 | Jade Imperial | 12 | **5 R1** Forest em qualquer característica |
| **Uncommon** | F-U01 | Jade Musgoso | 4 | **1 característica completa** Forest (3 genes: DD + R1 + R2) |
| **Uncommon** | F-U02 | Jade Nefrita | 4 | **3 DD** Forest em qualquer característica |
| **Uncommon** | F-U03 | Peridoto Selvagem | 4 | **3 R1** Forest em qualquer característica |
| **Uncommon** | F-U04 | Peridoto Dourado | 4 | **3 R2** Forest em qualquer característica |

---

### Mountain (Montanha) - 10 Cristais

| Tier | ID | Nome | Pontos | Regra Específica |
|------|----|----|--------|------------------|
| **Legendary** | M-L | Quartzo do Coração da Montanha | 50 | **30 genes Mountain** (DD + R1 + R2 em todas as 10 características) |
| **Epic** | M-E01 | Topázio Imperial | 22 | **3 características completas** Mountain (9 genes: 3 DD + 3 R1 + 3 R2) |
| **Epic** | M-E02 | Topázio Precious | 22 | **7 DD** Mountain em qualquer característica |
| **Rare** | M-R01 | Quartzo Rutilado | 12 | **2 características completas** Mountain (6 genes: 2 DD + 2 R1 + 2 R2) |
| **Rare** | M-R02 | Quartzo Fumê Imperial | 12 | **5 DD** Mountain em qualquer característica |
| **Rare** | M-R03 | Topázio Marrom | 12 | **5 R1** Mountain em qualquer característica |
| **Uncommon** | M-U01 | Ágata Rochosa | 4 | **1 característica completa** Mountain (3 genes: DD + R1 + R2) |
| **Uncommon** | M-U02 | Ágata Listrada | 4 | **3 DD** Mountain em qualquer característica |
| **Uncommon** | M-U03 | Quartzo Fumê | 4 | **3 R1** Mountain em qualquer característica |
| **Uncommon** | M-U04 | Jaspe Marrom | 4 | **3 R2** Mountain em qualquer característica |

---

### Desert (Deserto) - 13 Cristais

| Tier | ID | Nome | Pontos | Regra Específica |
|------|----|----|------0 Cristais

| Tier | ID | Nome | Pontos | Regra Específica |
|------|----|----|--------|------------------|
| **Legendary** | D-L | Topázio do Sol Eterno | 50 | **30 genes Desert** (DD + R1 + R2 em todas as 10 características) |
| **Epic** | D-E01 | Topázio Fogo do Deserto | 22 | **3 características completas** Desert (9 genes: 3 DD + 3 R1 + 3 R2) |
| **Epic** | D-E02 | Topázio Azul Imperial | 22 | **7 DD** Desert em qualquer característica |
| **Rare** | D-R01 | Topázio Dourado | 12 | **2 características completas** Desert (6 genes: 2 DD + 2 R1 + 2 R2) |
| **Rare** | D-R02 | Topázio Sherry | 12 | **5 DD** Desert em qualquer característica |
| **Rare** | D-R03 | Citrino Madeira | 12 | **5 R1** Desert em qualquer característica |
| **Uncommon** | D-U01 | Âmbar Solar | 4 | **1 característica completa** Desert (3 genes: DD + R1 + R2) |
| **Uncommon** | D-U02 | Citrino das Dunas | 4 | **3 DD** Desert em qualquer característica |
| **Uncommon** | D-U03 | Opala de Fogo | 4 | **3 R1** Desert em qualquer característica |
| **Uncommon** | D-U04 | Cornalina | 4 | **3 R2** Desert em qualquer característica

### Sea (Mar) - 13 Cristais

| Tier | ID | Nome | Pontos | Regra Específica |
|------|----|----0 Cristais

| Tier | ID | Nome | Pontos | Regra Específica |
|------|----|----|--------|------------------|
| **Legendary** | S-L | Água-marinha do Leviatã | 50 | **30 genes Sea** (DD + R1 + R2 em todas as 10 características) |
| **Epic** | S-E01 | Safira Oceânica | 22 | **3 características completas** Sea (9 genes: 3 DD + 3 R1 + 3 R2) |
| **Epic** | S-E02 | Água-marinha Santa Maria | 22 | **7 DD** Sea em qualquer característica |
| **Rare** | S-R01 | Água-marinha Celeste | 12 | **2 características completas** Sea (6 genes: 2 DD + 2 R1 + 2 R2) |
| **Rare** | S-R02 | Safira Azul | 12 | **5 DD** Sea em qualquer característica |
| **Rare** | S-R03 | Água-marinha Espirito Santo | 12 | **5 R1** Sea em qualquer característica |
| **Uncommon** | S-U01 | Turmalina Paraíba | 4 | **1 característica completa** Sea (3 genes: DD + R1 + R2) |
| **Uncommon** | S-U02 | Turquesa das Ondas | 4 | **3 DD** Sea em qualquer característica |
| **Uncommon** | S-U03 | Apatita Azul | 4 | **3 R1** Sea em qualquer característica |
| **Uncommon** | S-U04 | Larimar | 4 | **3 R2** Sea em qualquer característica

### Cave (Caverna) - 13 Cristais

| Tier | ID | Nome | Pontos | Regra Específica |
|------|----|----|----0 Cristais

| Tier | ID | Nome | Pontos | Regra Específica |
|------|----|----|--------|------------------|
| **Legendary** | C-L | Ametista do Abismo Profundo | 50 | **30 genes Cave** (DD + R1 + R2 em todas as 10 características) |
| **Epic** | C-E01 | Ametista Siberiana | 22 | **3 características completas** Cave (9 genes: 3 DD + 3 R1 + 3 R2) |
| **Epic** | C-E02 | Ametista Rose de France | 22 | **7 DD** Cave em qualquer característica |
| **Rare** | C-R01 | Ametista Geodo | 12 | **2 características completas** Cave (6 genes: 2 DD + 2 R1 + 2 R2) |
| **Rare** | C-R02 | Ametista Uruguaia | 12 | **5 DD** Cave em qualquer característica |
| **Rare** | C-R03 | Ametrina | 12 | **5 R1** Cave em qualquer característica |
| **Uncommon** | C-U01 | Ametista das Cavernas | 4 | **1 característica completa** Cave (3 genes: DD + R1 + R2) |
| **Uncommon** | C-U02 | Fluorita Roxa | 4 | **3 DD** Cave em qualquer característica |
| **Uncommon** | C-U03 | Lepidolita | 4 | **3 R1** Cave em qualquer característica |
| **Uncommon** | C-U04 | Charoita | 4 | **3 R2** Cave em qualquer característica

### Dark (Trevas) - 13 Cristais

| Tier | ID | Nome | Pontos | Regra Específica |
|------|----|----|---0 Cristais

| Tier | ID | Nome | Pontos | Regra Específica |
|------|----|----|--------|------------------|
| **Legendary** | K-L | Rubi Negro do Void | 50 | **30 genes Dark** (DD + R1 + R2 em todas as 10 características) |
| **Epic** | K-E01 | Rubi Estrela | 22 | **3 características completas** Dark (9 genes: 3 DD + 3 R1 + 3 R2) |
| **Epic** | K-E02 | Rubi Sangue de Pombo | 22 | **7 DD** Dark em qualquer característica |
| **Rare** | K-R01 | Rubi Negro | 12 | **2 características completas** Dark (6 genes: 2 DD + 2 R1 + 2 R2) |
| **Rare** | K-R02 | Granada Rodolita | 12 | **5 DD** Dark em qualquer característica |
| **Rare** | K-R03 | Espinélio Vermelho | 12 | **5 R1** Dark em qualquer característica |
| **Uncommon** | K-U01 | Ônix das Trevas | 4 | **1 característica completa** Dark (3 genes: DD + R1 + R2) |
| **Uncommon** | K-U02 | Granada Sombria | 4 | **3 DD** Dark em qualquer característica |
| **Uncommon** | K-U03 | Obsidiana Mogno | 4 | **3 R1** Dark em qualquer característica |
| **Uncommon** | K-U04 | Turmalina Negra | 4 | **3 R2** Dark em qualquer característica
### Características das Regras

#### Por Complexidade

**Legendary** (40 pontos) - 1 por raça
- Todas as raças: Pureza total (30 genes da mesma raça = 100% puro)
- Probabilidade: ~0.00000000001% (1 em 10 trilhões)
- Requisitos: 10 características com DD+R1+R2 da mesma raça

**Epic** (18 pontos) - 2 por raça
- Requisitos: 650 pontos) - 1 por raça
- Pureza total: 30 genes da mesma raça (DD + R1 + R2 em todas as 10 características)
- Probabilidade: ~0.000000000047% (1 em 2.15 trilhões)
- Goblin 100% puro de uma única raça

**Epic** (22 pontos) - 2 por raça
- E-01: 3 características completas (9 genes: 3 DD + 3 R1 + 3 R2)
- E-02: 7 DD em qualquer característica
- Probabilidade: ~0.01% a 0.1%
- Alta concentração genética

**Rare** (12 pontos) - 3 por raça
- R-01: 2 características completas (6 genes: 2 DD + 2 R1 + 2 R2)
- R-02: 5 DD em qualquer característica
- R-03: 5 R1 em qualquer característica
- Probabilidade: ~1% a 5%
- Concentração moderada-alta

**Uncommon** (4 pontos) - 4 por raça
- U-01: 1 característica completa (3 genes: DD + R1 + R2)
- U-02: 3 DD em qualquer característica
- U-03: 3 R160 Cristais Únicos

- **6 raças** × **10 cristais** = **60 cristais**
- Cada raça: **1 Legendary + 2 Epic + 3 Rare + 4 Uncommon**
- Cada cristal tem **regra específica baseada em partes genéticas**
- **Pontos fixos** por tier: Uncommon (4), Rare (12), Epic (22), Legendary (5
- Cada raça: **1 Legendary + 2 Epic + 4 Rare + 6 Uncommon**
- Cada cristal tem **regra específica e não0 Cristais

| Tier | ID | Nome | Pontos | Pedra | Descrição |
|------|----|----|--------|-------|-----------|
| Legendary | F-L | Esmeralda da Floresta Ancestral | 50 | Esmeralda Trapiche | Raríssima esmeralda com padrão hexagonal natural perfeito |
| Epic | F-E01 | Esmeralda Imperial | 22 | Esmeralda Imperial | Esmeralda perfeita sem inclusões, pureza excepcional |
| Epic | F-E02 | Esmeralda Colombiana | 22 | Esmeralda Muzo | Esmeralda verde intenso da melhor qualidade |
| Rare | F-R01 | Esmeralda Real | 12 | Esmeralda AAA | Esmeralda verde profundo brilhante de alta qualidade |
| Rare | F-R02 | Esmeralda Trapiche | 12 | Esmeralda Trapiche | Esmeralda com inclusões radiais naturais |
| Rare | F-R03 | Jade Imperial | 12 | Jade Imperial | Jade verde-esmeralda translúcido de qualidade imperial |
| Uncommon | F-U01 | Jade Musgoso | 4 | Jade Nefrita | Jade verde com padrões naturais de musgo |
| Uncommon | F-U02 | Jade Nefrita | 4 | Jade Nefrita | Jade verde-claro opaco tradicional |
| Uncommon | F-U03 | Peridoto Selvagem | 4 | Peridoto | Peridoto verde-oliva brilhante |
| Uncommon | F-U04 | Peridoto Dourado | 4 | Peridoto Dourado | Peridoto com tons dourados qualidade imperial |
| Uncommon | F-U01 | Jade Musgoso | 5 | Jade Nefrita | Jade verde com padrões naturais de musgo |
| Uncommon | F-U02 | Jade Nefrita | 5 | Jade Nefrita | Jade verde-claro opaco tradicional |
| Uncommon | F-U03 | Peridoto Selvagem | 5 | Peridoto | Peridoto verde-oliva brilhante |
| Uncommon | F-U04 | Peridoto Dourado | 5 | Peridoto Dourado | Peridoto com tons dourados |
| Uncommon | F-U05 | Turmalina Verde | 5 | Turmalina Verde | Turmalina verde translúcida |
| Uncommon | F-U06 | Crisoberilo | 5 | Crisoberilo | Cristal amarelo-esverdeado brilhante |

---

### Mountain (Cinza/Marrom - Quartzos e Topázios) - 13 Cristais

| Tier | ID | Nome | Pontos | Pedra | Descrição |
|------|----|----|--------|-------|-----------|0 Cristais

| Tier | ID | Nome | Pontos | Pedra | Descrição |
|------|----|----|--------|-------|-----------|
| Legendary | M-L | Quartzo do Coração da Montanha | 50 | Quartzo Fantasma | Quartzo com múltiplas formações fantasma perfeitas |
| Epic | M-E01 | Topázio Imperial | 22 | Topázio Imperial | Topázio laranja-dourado precioso de alta qualidade |
| Epic | M-E02 | Topázio Precious | 22 | Topázio Amarelo | Topázio amarelo intenso raro |
| Rare | M-R01 | Quartzo Rutilado | 12 | Quartzo Rutilado | Quartzo com inclusões douradas de rutilo |
| Rare | M-R02 | Quartzo Fumê Imperial | 12 | Quartzo Fumê AAA | Quartzo fumê marrom profundo de alta qualidade |
| Rare | M-R03 | Topázio Marrom | 12 | Topázio Marrom | Topázio marrom-dourado natural |
| Uncommon | M-U01 | Ágata Rochosa | 4 | Ágata | Pedra com bandas marrons e cinzas |
| Uncommon | M-U02 | Ágata Listrada | 4 | Ágata Bandada | Ágata com bandas paralelas definidas |
| Uncommon | M-U03 | Quartzo Fumê | 4 | Quartzo Fumê | Cristal translúcido acastanhado |
| Uncommon | M-U04 | Jaspe Marrom | 4 | Jaspe | Jaspe opaco marrom-avermelh
### Desert (Amarelo/Dourado - Topázios e Citrinos) - 13 Cristais

| Tier | ID | Nome | Pontos | Pedra | Descrição |
|------|----|----|--------|-------|-----------|
| Legendary | D-L | Topázio do Sol Eterno | 40 | Topázio Azul Natural | Raríssimo topázio azul natural não tratado |
| Epic | D-E01 | Topázio Fogo do Deserto | 18 | Topázio Ígneo | Topázio laranja-fogo intenso raro |
| Epic | D-E02 | Topázio Azul Imperial | 18 | Topázio 0 Cristais

| Tier | ID | Nome | Pontos | Pedra | Descrição |
|------|----|----|--------|-------|-----------|
| Legendary | D-L | Topázio do Sol Eterno | 50 | Topázio Azul Natural | Raríssimo topázio azul natural não tratado |
| Epic | D-E01 | Topázio Fogo do Deserto | 22 | Topázio Ígneo | Topázio laranja-fogo intenso raro |
| Epic | D-E02 | Topázio Azul Imperial | 22 | Topázio Azul AAA | Topázio azul de qualidade excepcional |
| Rare | D-R01 | Topázio Dourado | 12 | Topázio Dourado | Topázio amarelo-dourado brilhante |
| Rare | D-R02 | Topázio Sherry | 12 | Topázio Sherry | Topázio amarelo-acobreado |
| Rare | D-R03 | Citrino Madeira | 12 | Citrino Madeira | Citrino laranja-avermelhado profundo |
| Uncommon | D-U01 | Âmbar Solar | 4 | Âmbar | Âmbar dourado com inclusões de resina |
| Uncommon | D-U02 | Citrino das Dunas | 4 | Citrino | Citrino amarelo-pálido translúcido |
| Uncommon | D-U03 | Opala de Fogo | 4 | Opala de Fogo | Opala laranja-amarelada com jogo de cores |
| Uncommon | D-U04 | Cornalina | 4 | Cornalina | Calcedônia laranja-avermelhada translúcid
|------|----|----|--------|-------|-----------|
| Legendary | S-L | Água-marinha do Leviatã | 40 | Safira Padparadscha | Lendária safira rosa-alaranjada natural |
| Epic | S-E01 | Safira Oceânica | 18 | Safira Azul AAA | Safira azul profunda de qualidade excepcional |
| Epic | S-E02 | Água-marinha Santa Maria | 18 | Água-0 Cristais

| Tier | ID | Nome | Pontos | Pedra | Descrição |
|------|----|----|--------|-------|-----------|
| Legendary | S-L | Água-marinha do Leviatã | 50 | Safira Padparadscha | Lendária safira rosa-alaranjada natural |
| Epic | S-E01 | Safira Oceânica | 22 | Safira Azul AAA | Safira azul profunda de qualidade excepcional |
| Epic | S-E02 | Água-marinha Santa Maria | 22 | Água-marinha AAA | Água-marinha azul profundo intenso sem tons verdes |
| Rare | S-R01 | Água-marinha Celeste | 12 | Água-marinha | Água-marinha azul-celeste cristalina |
| Rare | S-R02 | Safira Azul | 12 | Safira | Safira azul de alta qualidade |
| Rare | S-R03 | Água-marinha Espirito Santo | 12 | Água-marinha Espirito Santo | Água-marinha azul puro sem tons verdes |
| Uncommon | S-U01 | Turmalina Paraíba | 4 | Turmalina Paraíba | Turmalina azul-neon elétrica |
| Uncommon | S-U02 | Turquesa das Ondas | 4 | Turquesa | Turquesa azul-esverdeada com matriz |
| Uncommon | S-U03 | Apatita Azul | 4 | Apatita Azul | Apatita azul-neon translúcida |
| Uncommon | S-U04 | Larimar | 4 | Larimar | Pectolita azul-celeste com padrões brancos
|------|----|----|--------|-------|-----------|
| Legendary | C-L | Ametista do Abismo Profundo | 40 | Ametista Chevron | Rara ametista com padrão em V perfeito |
| Epic | C-E01 | Ametista Siberiana | 18 | Ametista Siberiana | Ametista roxa-real de qualidade siberiana |
| Epic | C-E02 | Ametista Rose de France | 0 Cristais

| Tier | ID | Nome | Pontos | Pedra | Descrição |
|------|----|----|--------|-------|-----------|
| Legendary | C-L | Ametista do Abismo Profundo | 50 | Ametista Chevron | Rara ametista com padrão em V perfeito |
| Epic | C-E01 | Ametista Siberiana | 22 | Ametista Siberiana | Ametista roxa-real de qualidade siberiana |
| Epic | C-E02 | Ametista Rose de France | 22 | Ametista Rose de France | Ametista lilás-rosada delicada |
| Rare | C-R01 | Ametista Geodo | 12 | Ametista Geodo | Ametista roxa em formação de geodo |
| Rare | C-R02 | Ametista Uruguaia | 12 | Ametista Uruguaia | Ametista roxa profunda do Uruguai |
| Rare | C-R03 | Ametrina | 12 | Ametrina | Cristal com zonas de ametista e citrino |
| Uncommon | C-U01 | Ametista das Cavernas | 4 | Ametista | Ametista roxa com zonamento de cor |
| Uncommon | C-U02 | Fluorita Roxa | 4 | Fluorita | Fluorita roxa translúcida vítrea |
| Uncommon | C-U03 | Lepidolita | 4 | Lepidolita | Mica roxa-lilás com brilho perolado |
| Uncommon | C-U04 | Charoita | 4 | Charoita | Pedra roxa com padrões swirl único
|------|----|----|--------|-------|-----------|
| Legendary | K-L | Rubi Negro do Void | 40 | Rubi Sangue de Dragão | Mítico rubi vermelho-puro intenso perfeito |
| Epic | K-E01 | Rubi Estrela | 18 | Rubi Estrela | Rubi com asterismo (efeito de estrela de 6 pontas) |
| Epic | K-E02 | Rubi Sangue de Pombo | 18 | Rubi Sangue de Pombo | Rubi vermelho-puro com fluorescência azul |
| Rare | K-R01 | Rubi Negro | 10 | Rubi | Rubi vermelho-sangue profundo |
| Rare | K-R02 | Granada Rodolita | 10 | Granada Rodolita | Granada rosa-avermelhada brilhante |
| Rare | K-R03 | Espinélio Vermelho | 10 | Espin0 Cristais

| Tier | ID | Nome | Pontos | Pedra | Descrição |
|------|----|----|--------|-------|-----------|
| Legendary | K-L | Rubi Negro do Void | 50 | Rubi Sangue de Dragão | Mítico rubi vermelho-puro intenso perfeito |
| Epic | K-E01 | Rubi Estrela | 22 | Rubi Estrela | Rubi com asterismo (efeito de estrela de 6 pontas) |
| Epic | K-E02 | Rubi Sangue de Pombo | 22 | Rubi Sangue de Pombo | Rubi vermelho-puro com fluorescência azul |
| Rare | K-R01 | Rubi Negro | 12 | Rubi | Rubi vermelho-sangue profundo |
| Rare | K-R02 | Granada Rodolita | 12 | Granada Rodolita | Granada rosa-avermelhada brilhante |
| Rare | K-R03 | Espinélio Vermelho | 12 | Espinélio | Espinélio vermelho-vivo transparente |
| Uncommon | K-U01 | Ônix das Trevas | 4 | Ônix | Ônix negro com bandas paralelas |
| Uncommon | K-U02 | Granada Sombria | 4 | Granada | Granada vermelho-escura com inclusões |
| Uncommon | K-U03 | Obsidiana Mogno | 4 | Obsidiana Mogno | Obsidiana vermelho-marrom translúcida |
| Uncommon | K-U04 | Turmalina Negra | 4 | Turmalina Negra | Turmalina negra opaca (Schorl)
| **Legendary** | 40 | Extrema | 1 por raça | 6 |
| **Epic** | 18 | Muito Alta | 2 por raça | 12 |
| **Rare** | 10 | Alta | 4 por raça | 24 |
| **Uncommon** | 5 | Moderada | 6 por raça | 36 |
| **TOTAL** | - | - | **13 por raça** | **78** |

### Raridade do Goblin

A raridade final do goblin é determinada pela **soma dos pontos de TODOS os cristais** que ele possui:
50 | Extrema | 1 por raça | 6 |
| **Epic** | 22 | Muito Alta | 2 por raça | 12 |
| **Rare** | 12 | Alta | 3 por raça | 18 |
| **Uncommon** | 4 | Moderada | 4 por raça | 24 |
| **TOTAL** | - | - | **10 por raça** | **60
- 0-10 pontos:   Common      (~50%)
- 11-20 pontos:  Uncommon    (~30%)
- 21-35 pontos:  Rare        (~15%)
- 36-55 pontos:  Epic        (~4%)
- 56+ pontos:    Legendary   (~1%)
```

### Exemplos de Combinações

| Cr4 pontos:    Common      (~50%)
- 5-12 pontos:   Uncommon    (~30%)
- 13-24 pontos:  Rare        (~15%)
- 25-50 pontos:  Epic        (~4%)
- 51 Uncommon | 10 | Common |
| 1× Rare | 10 | Common |
| 3× Uncommon | 15 | Uncommon |
| 1× Rare + 1× Uncommon | 15 | Uncommon |
| 1× Epic | 18 | Uncommon |
| 2× Rare | 20 |4 | Common |
| 2× Uncommon | 8 | Uncommon |
| 1× Rare | 12 | Uncommon |
| 3× Uncommon | 12 | Uncommon |
| 1× Rare + 1× Uncommon | 16 | Rare |
| 1× Epic | 22 | Rare |
| 2× Rare | 24 | Rare |
| 1× Rare + 2× Uncommon | 20 | Rare |
| 1× Epic + 1× Uncommon | 26 | Epic |
| 1× Epic + 1× Rare | 34 | Epic |
| 3× Rare | 36 | Epic |
| 2× Epic | 44 | Epic |
| 1× Legendary | 50 | Epic |
| 1× Epic + 2× Rare | 46 | Epic |
| 1× Legendary + 1× Uncommon | 54 | Legendary |
| 1× Legendary + 1× Rare | 62 | Legendary |
| 1× Legendary + 1× Epic | 72 | Legendary |
| 2× Legendary | 100 pontos
- 1× Legendary + 1× Epic (58 pontos300 pontos (impossível na prática)

**Mínimo para Legendary**: 51 pontos
- 1× Legendary + 1× Uncommon (54 pontos)
- 1× Legendary + 1× Rare (62 pontos)
- 1× Legendary + 1× Epic (72 pontos)
- 2× Legendary (100 pontos)

**Mínimo para Epic**: 25 pontos
- 1× Epic + 1× Uncommon (26 pontos)
- 1× Epic + 1× Rare (34 pontos)
- 3× Rare (36 pontos)
- 2× Epic (44 pontos)
- 1× Legendary (50 pontos)

**Mínimo para Rare**: 13 pontos
- 1× Rare + 1× Uncommon (16 pontos)
- 1× Rare + 2× Uncommon (20 pontos)
- 1× Epic (22 pontos)
- 2× Rare (24 pontos)

**Típico Common**: 0-4 pontos
- 0 cristais (0 pontos)
- 1× Uncommon (4 pontos)

**Típico Uncommon**: 5-12 pontos
- 2× Uncommon (8 pontos)
- 1× Rare (12 pontos)
- 3× Uncommon (12
## Probabilidades

### Metodologia

Considerando geração completamente aleatória:
- **6 raças possíveis** para cada gene (prob. 1/6 ≈ 16.67% cada)
- **3 posições** por característica (DD, R1, R2)
- **10 características** (6 físicas + 4 cores)
- **30 genes totais** por goblin

### Probabilidade por Tier (para UMA raça específica)

#### Cálculos Base

**Probabilidade de N genes DD da mesma raça:**
```
P(n DD) = C(10,n) × (1/6)^n × (5/6)^(10-n)
```

**Probabilidade de genes com distribuição específica:**
```
P(combo) = [prob dos DD] × [prob dos R1] × [prob dos R2]
```

#### Tabela de Probabilidades por Tier

| Tier | Regra Típica | Cálculo Aproximado | Probabilidade | Odds | 1 em |
|------|--------------|-------------------|---------------|------|------|
| **Legendary** | 30 genes puros | (1/6)^30 | 0.00000000000466% | 1:2.15×10¹³ | 21 trilhões |
| **Epic** | 6-7 DD + 4-6 R1 + extras | C(10,7)×(1/6)^7 × fatores R1/R2 | ~0.008% | 1:12,500 | 12.5 mil |
| **Rare** | 4-6 DD + 2-5 R1 | C(10,5)×(1/6)^5 × fatores R1 | ~0.4% | 1:250 | 250 |
| **Uncommon** | 2-4 DD + 1-4 R1 | C(10,3)×(1/6)^3 × fatores R1 | ~15% | 1:6.7 | 7 |

**Observação**: Como há **6 raças** competindo, multiplique por 6 para probabilidade de ALGUM cristal.

---

### Probabilidades Detalhadas por Tier

#### Legendary (Pureza Total - 30 genes)

| Raça | Requisito | Probabilidade | 1 em |
|------|-----------|---------------|------|
| Todas | 10 DD + 10 R1 + 10 R2 (100% puro) | 4.66×10⁻¹⁴ % | 21.5 trilhões |

**Cálculo**: (1/6)^30 = 1 / 2.1542×10¹³

---

#### Epic 30 genes da mesma raça (DD + R1 + R2 em 10 características) | 4.66×10⁻¹⁴ % | 2.1

**Requisitos típicos**: 6-7 DD + 4-6 R1 + distribuição específica + pureza parcial

| Fórmula Base | Valor |
|-E-01**: 3 características completas (9 genes: 3 DD + 3 R1 + 3 R2)
**E-02**: 7 DD da mesma raça em qualquer característica

| Fórmula | Valor |
|---------|-------|
| P(E-01: 3 características completas) | C(10,3) × (1/6)^9 ≈ 0.000012% |
| P(E-02: 7 DD mesma raça) | C(10,7) × (1/6)^7 × (5/6)^3 ≈ 0.0043% |

**Probabilidade por cristal Epic**:
- E-01: ~0.000012% (muito raro - 3 características completas)
- E-02: ~0.0043% (raro - 7 DD)

**Probabilidade total Epic para uma raça** (E-01 OU E-02): ~0.0043%

**Para as 6 raças**: ~0.026% de ter ALGUM Epic

| Em 10,000 Goblins | Qtd Esperada com Epic |
|-------------------|-----------------------|
| Epic de qualquer raça | 2-3 |
| Epic específico (ex: F-E02
#### Rare (4 cristais por raça)
3 cristais por raça)

**R-01**: 2 características completas (6 genes: 2 DD + 2 R1 + 2 R2)
**R-02**: 5 DD da mesma raça em qualquer característica
**R-03**: 5 R1 da mesma raça em qualquer característica

| Fórmula | Valor |
|---------|-------|
| P(R-01: 2 características completas) | C(10,2) × (1/6)^6 ≈ 0.01% |
| P(R-02: 5 DD mesma raça) | C(10,5) × (1/6)^5 × (5/6)^5 ≈ 0.13% |
| P(R-03: 5 R1 mesma raça) | C(10,5) × (1/6)^5 × (5/6)^5 ≈ 0.13% |

**Probabilidade por cristal Rare**:
- R-01: ~0.01% (2 características completas)
- R-02: ~0.13% (5 DD)
- R-03: ~0.13% (5 R1)

**Probabilidade total Rare para uma raça** (R-01 OU R-02 OU R-03): ~0.27%

**Para as 6 raças**: ~1.6% de ter ALGUM Rare

| Em 10,000 Goblins | Qtd Esperada com Rare |
|-------------------|-----------------------|
| Rare de qualq4 cristais por raça)

**U-01**: 1 característica completa (3 genes: DD + R1 + R2)
**U-02**: 3 DD da mesma raça em qualquer característica
**U-03**: 3 R1 da mesma raça em qualquer característica
**U-04**: 3 R2 da mesma raça em qualquer característica

| Fórmula | Valor |
|---------|-------|
| P(U-01: 1 característica completa) | 10 × (1/6)^3 ≈ 0.46% |
| P(U-02: 3 DD mesma raça) | C(10,3) × (1/6)^3 × (5/6)^7 ≈ 3.1% |
| P(U-03: 3 R1 mesma raça) | C(10,3) × (1/6)^3 × (5/6)^7 ≈ 3.1% |
| P(U-04: 3 R2 mesma raça) | C(10,3) × (1/6)^3 × (5/6)^7 ≈ 3.1% |

**Probabilidade por cristal Uncommon**:
- U-01: ~0.46% (1 característica completa)
- U-02/U-03/U-04: ~3.1% cada (3 genes na mesma posição)

**Probabilidade total Uncommon para uma raça** (U-01 OU U-02 OU U-03 OU U-04): ~9.7%

**Para as 6 raças**: ~45% de ter ALGUM Uncommon

| Em 10,000 Goblins | Qtd Esperada com Uncommon |
|-------------------|---------------------------|
| Uncommon de qualquer raça | 4,500 |
| Uncommon específico (ex: F-U02) | 31
| Em 10,000 Goblins | Qtd Esperada com Uncommon |
|---------------55% | 5,500 | Nenhuma raça atingiu requisitos mínimos |
| 1 cristal | ~32% | 3,200 | 1 raça formou cristal |
| 2 cristais | ~11% | 1,100 | 2 raças formaram cristais |
| 3 cristais | ~1.8% | 180 | 3 raças formaram cristais |
| 4 cristais | ~0.2% | 20 | 4 raças formaram cristais |
| 5 cristais | ~0.01% | 1 | 5 raças formaram cristais |
| 6 cristais | ~0.0001% | 0 | Todas as 6 raças formaram cristais |

**Média**: ~0.6 Cristais | Probabilidade | Em 10,000 Goblins | Descrição |
|------------------------|---------------|-------------------|-----------|
| 0 cristais | ~8% | 800 | Nenhuma raça atingiu requisitos mínimos |
| 1 cristal | ~28% | 2,800 | 1 raça formou cristal |
| 2 cristais | ~35% | 3,500 | 2 raças formaram cristais |
| 3 cristais | ~20% | 2,000 | 3 raças formaram cristais |
| 4 cristais | ~7% | 700 | 4 raças formaram cristais |
| 5 cristais | ~1.8% | 180 | 5 raças formaram cristais |
| 6 cristais | ~04 | ~50% | 5,000 | 0-1 Uncommon |
| **Uncommon** | 5-12 | ~30% | 3,000 | 2-3 Uncommon ou 1 Rare |
| **Rare** | 13-24 | ~15% | 1,500 | 1 Rare + Uncommon, 2 Rare, ou 1 Epic |
| **Epic** | 25-50 | ~4% | 400 | 1 Epic + extras, 2+ Rare, ou 1 Legendary |
| **Legendary** | 51+ | ~1% | 100 | Legendary + extras ou múltiplos

### Distribuição da Raridade Final do Goblin

| Raridade | Pontos | Probabilidade | Em 10,000 | Descrição Típica |
|----------|--------|---------------|-----------|------------------|
| **Common** | 0-15 | ~45% | 4,500 | 0-3 Uncommon ou 1 Rare |
| **Uncommon** | 16-35 | ~30% | 3,000 | 4-8 Uncommon, 2-3 Rare, ou 1 Epic |
| **Rare** | 36-75 | ~18% | 1,800 | Múltiplos Rare e Epic |
| **Epic** | 76-150 | ~5% | 500 | Vários Epic e possivelmente Legendary |
| **Legendary** | 151+ | ~2% | 200 | Múltiplos Legendary e Epic |

---
.15T    │ 1:2.15T      │ 1:360B           │
├──────────────┼────────────┼──────────────┼──────────────────┤
│ Epic         │ 0.002%     │ 0.0043%      │ 0.026%           │
│              │ 1:50,000   │ 1:23,000     │ 1:3,800          │
├──────────────┼────────────┼──────────────┼──────────────────┤
│ Rare         │ 0.09%      │ 0.27%        │ 1.6%             │
│              │ 1:1,100    │ 1:370        │ 1:63             │
├──────────────┼────────────┼──────────────┼──────────────────┤
│ Uncommon     │ 2.4%       │ 9.7%         │ 45%              │
│              │ 1:42       │ 1:10.3       │ 1:2.2            │
└──────────────┴────────────┴──────────────┴──────────────────┘

┌─────────────────────────────────────────────────────────────┐
│              DISTRIBUIÇÃO DE RARIDADE DO GOBLIN              │
├──────────────┬────────────┬──────────────┬──────────────────┤
│ Raridade     │ Pontos     │ Probabilidade│ Em 10,000        │
├──────────────┼────────────┼──────────────┼──────────────────┤
│ Common       │ 0-4        │ ████████████████████████████████████████ 50% │ 5,000 │
│ Uncommon     │ 5-12       │ ████████████████████████ 30% │ 3,000 │
│ Rare         │ 13-24      │ ████████████ 15%         │ 1,500 │
│ Epic         │ 25-50      │ ███ 4%                   │ 400   │
│ Legendary    │ 51
┌─────────────────────────────────────────────────────────────┐
│              DISTRIBUIÇÃO DE RARIDADE DO GOBLIN              │
├──────────────┬────────────┬──────────────┬──────────────────┤
│ Raridade     │ Pontos     │ Probabilidade│ Em 10,000        │
├──────────────┼────────────┼──────────────┼──────────────────┤
│ Common       │ 0-10       │ ████████████████████████████████████████ 50% │ 5,000 │
│ Uncommon     │ 11-20      │ ████████████████████████ 30% │ 3,000 │
│ Rare         │ 21-35      │ ████████████ 15%         │ 1,500 │
│ Ep45% de chance** de ter pelo menos 1 cristal Uncommon
- **1.6% de chance** de ter pelo menos 1 cristal Rare
- **0.026% de chance** de ter pelo menos 1 cristal Epic
- **~0% de chance** de ter cristal Legendary (1 em 360 bilhões)

**Para seu goblin:**
- **50% de chance** de ser Common (0-4 pts)
- **30% de chance** de ser Uncommon (5-12 pts)
- **15% de chance** de ser Rare (13-24 pts)
- **4% de chance** de ser Epic (25-50 pts)
- **1% de chance** de ser Legendary (51+ pts)

**Em uma coleção de 1,000 goblins:**
- **~500 serão Common** (sem cristais ou 1 Uncommon)
- **~300 serão Uncommon** (2-3 Uncommon ou 1 Rare)
- **~150 serão Rare** (1-2 Rare + extras)
- **~40 serão Epic** (Epic, múltiplos Rare, ou Legendary)
- **~10 serão Legendary** (Legendary + extras ou múltiplos Epic)
- **~0 Legendary puros** (estatisticamente improvável)

**Cristais mais raros:**
- **Legendary de qualquer raça**: ~0 em 100 milhões de goblins
- **Epic E-01 (3 características completas)**: ~0 em 1 milhão de goblins
- **Epic E-02 (7 DD)**: ~1 em 23,000 goblins
- **Rare R-01 (2 características completas)**: ~1 em 10,000 goblins
- **Rare R-02/R-03 (5 genes)**: ~1 em 770 goblins
- **Uncommon U-01 (1 característica completa)**: ~1 em 220 goblins
- **Uncommon U-02/U-03/U-04 (3 genes)**: ~1 em 32ic)
- **~150 serão Rare** (Epic+extras, 3 Rare, ou combinações altas)
- **~40 serão Epic** (2 Epic, Legendary, ou múltiplos Rare)
- **~10 serão Legendary** (Legendary+Epic ou combinações extremas)
- **~0 Legendary puros** (estatisticamente improvável)

**Cristais mais raros:**
- **Legendary de qualquer raça**: ~0 em 1 milhão de goblins
- **Epic específico (ex: Esmeralda Imperial)**: ~1 em 30,000 goblins
- **Rare específico (ex: Esmeralda Real)**: ~1 em 400 goblins
- **Uncommon específico (ex: Jade Musgoso)**: ~1 em 15 goblins

---

## Exemplos Práticos

### Exemplo 1: Goblin Common (1 cristal Uncommon)

```
Genes do Goblin:

Físicas:
- Skin:  DD=Forest, R1=Mountain, R2=Sea
- Hair:  DD=Desert, R1=Cave, R2=Dark
- Eyes:  DD=Mountain, R1=Forest, R2=Desert
- Ear:   DD=Sea, R1=Dark, R2=Cave
- Mouth: DD=Cave, R1=Mountain, R2=Forest
- Nose:  DD=Dark, R1=Sea, R2=Desert

Cores:
- SkinColor:  DD=Mountain, R1=Desert, R2=Forest
- HairColor:  DD=Sea, R1=Cave, R2=Dark
- PupilColor: DD=Forest, R1=Mountain, R2=Sea
- EyeColor:   DD=Dark, R1=Desert, R2=Cave

Análise por Raça:

FOREST:
✗ Legendary: Precisa 30 genes Forest → Tem apenas 5 genes
✗ Epic (F-E01): Precisa 5 DD físicas → Tem 1 DD física
✗ Epic (F-E02): Precisa 6 DD → Tem 2 DD
✗ Rare (todas): Requisitos não satisfeitos
✗ Uncommon (todas): Não satisfaz nenhuma regra U-01 a U-06

MOUNTAIN:
✗ Legendary/Epic/Rare: Não
✓ Uncommon M-U03: Precisa 3 DD (1 física + 1 cor mín.) + 2 R1
  - DD: Eyes (física), SkinColor (cor), PupilColor (cor) = 3 DD ✓
  - R1: Skin, Mouth = 2 R1 ✓
→ CRISTAL FORMADO: Quartzo Fumê (5 pontos)

SEA:
✗ Todas as regras não satisfeitas

Outras raças: Não satisfazem requisitos

Resultado:
Cristais: 1 (Quartzo Fumê)
Pontos Totais: 5
Raridade: Common Goblin (0-10 = Common)
```

---

### Exemplo 2: Goblin Uncommon (2 cristais)

```
Genes do Goblin:

Físicas:
- Skin:  DD=Sea, R1=Sea, R2=Mountain
- Hair:  DD=Sea, R1=Forest, R2=Sea
- Eyes:  DD=Forest, R1=Sea, R2=Desert
- Ear:   DD=Mountain, R1=Mountain, R2=Sea
- Mouth: DD=Forest, R1=Dark, R2=Cave
- Nose:  DD=Forest, R1=Mountain, R2=Desert

Cores:
- SkinColor:  DD=Sea, R1=Mountain, R2=Desert
- HairColor:  DD=Forest, R1=Sea, R2=Dark
- PupilColor: DD=Mountain, R1=Forest, R2=Sea
- EyeColor:   DD=Mountain, R1=Desert, R2=Cave

Análise por Raça:

FOREST:
✗ Legendary/Epic/Rare: Não satisfeitos
✓ Uncommon F-U03: Precisa 3 DD físicas + 2 R1 cores
  - DD físicas: Eyes, Mouth, Nose = 3 DD ✓
  - R1 cores: HairColor, PupilColor = 2 R1 ✓
→ CRISTAL FORMADO: Peridoto Selvagem (5 pontos)

SEA:
✗ Legendary/Epic/Rare: Não
✓ Uncommon S-U02: Precisa 3 DD + 2 R1
  - DD: Skin, Hair, SkinColor = 3 DD ✓
  - R1: Skin, Eyes, HairColor = 3 R1 (mais que 2) ✓
→ CRISTAL FORMADO: Turquesa das Ondas (5 pontos)

MOUNTAIN:
✗ Legendary/Epic/Rare: Não
✓ Uncommon M-U03: Precisa 3 DD (1 física + 1 cor) + 2 R1
  - DD: Ear (física), PupilColor, EyeColor (cores) = 3 DD ✓
  - R1: Ear, Nose, SkinColor = 3 R1 ✓
→ CRISTAL FORMADO: Quartzo Fumê (5 pontos)

Resultado:
Cristais: 3 (Peridoto + Turquesa + Quartzo)
Pontos Totais: 5 + 5 + 5 = 15 pontos
Raridade: Uncommon Goblin (11-20 = Uncommon)
```

---

### Exemplo 3: Goblin Rare (1 Rare + 2 Uncommon)

```
Genes do Goblin:

Físicas:
- Skin:  DD=Cave, R1=Cave, R2=Cave (PURA)
- Hair:  DD=Cave, R1=Cave, R2=Mountain
- Eyes:  DD=Cave, R1=Dark, R2=Cave
- Ear:   DD=Cave, R1=Cave, R2=Forest
- Mouth: DD=Dark, R1=Cave, R2=Cave
- Nose:  DD=Mountain, R1=Cave, R2=Desert

Cores:
- SkinColor:  DD=Cave, R1=Cave, R2=Dark
- HairColor:  DD=Cave, R1=Mountain, R2=Cave
- PupilColor: DD=Cave, R1=Desert, R2=Sea
- EyeColor:   DD=Mountain, R1=Cave, R2=Dark

Análise por Raça:

CAVE:
✗ Legendary: Precisa 30 genes Cave → Tem ~22 genes
✗ Epic C-E01: Precisa 5 DD físicas + 3 DD cores + 5 R1 + 2 R2
  - DD: 7 total (4 físicas + 3 cores) ✓ mas precisa 5 físicas (tem 4) ✗
✗ Epic C-E02: Precisa 6 DD + 6 R1 (mín. 4 físicas)
  - DD: 7 ✓, R1: 7 ✓, mas R1 físicas: 5 (ok) ✓
  - Quase, mas não tem 6 R1 totais... espera, tem 7 R1! ✓
✗ Epic C-E02: Análise mais cuidadosa mostra que não satisfaz distribuição
✓ Rare C-R01: Precisa 6 DD (3 físicas + 3 cores) + 3 R1 físicas
  - DD Cave: Skin, Hair, Eyes, Ear (físicas) + SkinColor, HairColor, PupilColor (cores) = 7 DD
  - 4 físicas + 3 cores ✓
  - R1 físicas: Skin, Hair, Ear, Mouth, Nose = 5 R1 físicas ✓
→ CRISTAL FORMADO: Ametista Geodo (10 pontos)

MOUNTAIN:
✗ Legendary/Epic/Rare: Não
✓ Uncommon M-U03: Tem Nose (física), EyeColor (cor), SkinColor (cor)... 
  - Espera, Nose é DD Mountain? Não, é DD Mountain apenas em R1
✗ Não satisfaz

DARK:
✗ Rare: Não
✓ Uncommon K-U02: Precisa 3 DD físicas + 2 R1
  - DD físicas: Mouth = 1 (não suficiente)
✗ Não satisfaz

Resultado:
Cristais: 1 (Ametista Geodo)
Pontos Totais: 10
Raridade: Common Goblin (0-10 = Common)
```

---

### Exemplo 4: Goblin Epic (1 Epic + 1 Rare)

```
Genes do Goblin:

Físicas:
- Skin:  DD=Desert, R1=Desert, R2=Desert (PURA)
- Hair:  DD=Desert, R1=Desert, R2=Mountain
- Eyes:  DD=Desert, R1=Desert, R2=Sea
- Ear:   DD=Mountain, R1=Desert, R2=Desert
- Mouth: DD=Desert, R1=Dark, R2=Cave
- Nose:  DD=Desert, R1=Desert, R2=Forest

Cores:
- SkinColor:  DD=Desert, R1=Mountain, R2=Desert
- HairColor:  DD=Desert, R1=Cave, R2=Desert
- PupilColor: DD=Desert, R1=Desert, R2=Sea
- EyeColor:   DD=Desert, R1=Desert, R2=Dark

Análise por Raça:

DESERT:
✗ Legendary: Precisa 30 genes → Tem ~26 genes (não suficiente)
✓ Epic D-E01: Precisa 4 DD físicas + 3 DD cores + 5 R1 + 3 R2
  - DD físicas: Skin, Hair, Eyes, Mouth, Nose = 5 ✓
  - DD cores: SkinColor, HairColor, PupilColor, EyeColor = 4 ✓
  - R1: Skin, Hair, Eyes, Ear, Nose, PupilColor, EyeColor = 7 ✓
  - R2: Skin, Ear, SkinColor, HairColor = 4 ✓
→ CRISTAL FORMADO: Topázio Fogo do Deserto (18 pontos)
→ PARA verificação para Desert

MOUNTAIN:
✗ Epic/Rare: Não
✓ Uncommon M-U04: Precisa 4 DD físicas + 1 R1 cor
  - DD físicas: Ear = 1 (não suficiente)
✗ Não satisfaz

Outras raças: Não satisfazem

Resultado:
Cristais: 1 (Topázio Fogo do Deserto)
Pontos Totais: 18
Raridade: Uncommon Goblin (11-20 = Uncommon)

Nota: 18 pontos está em Uncommon (11-20)
```

---

### Exemplo 5: Goblin Legendary (1 Legendary Puro)

```
Genes do Goblin - PUREZA TOTAL MOUNTAIN:

Físicas:
- Skin:  DD=Mountain, R1=Mountain, R2=Mountain
- Hair:  DD=Mountain, R1=Mountain, R2=Mountain
- Eyes:  DD=Mountain, R1=Mountain, R2=Mountain
- Ear:   DD=Mountain, R1=Mountain, R2=Mountain
- Mouth: DD=Mountain, R1=Mountain, R2=Mountain
- Nose:  DD=Mountain, R1=Mountain, R2=Mountain

Cores:
- SkinColor:  DD=Mountain, R1=Mountain, R2=Mountain
- HairColor:  DD=Mountain, R1=Mountain, R2=Mountain
- PupilColor: DD=Mountain, R1=Mountain, R2=Mountain
- EyeColor:   DD=Mountain, R1=Mountain, R2=Mountain

Análise:

MOUNTAIN:
✓ Legendary: Pureza total → 10 DD + 10 R1 + 10 R2 Mountain
→ CRISTAL FORMADO: Quartzo do Coração da Montanha (40 pontos)
→ PARA verificação (Legendary satisfeito)

Outras raças: 0 genes

Resultado:
Cristais: 1 (Quartzo do Coração da Montanha)
Pontos Totais: 40
Raridade: Epic Goblin (36-55 = Epic)

Nota: Um goblin 100% puro em uma raça resulta em Epic (40 pontos)!
Para Legendary Goblin (56+), precisaria: Legendary + Epic, 2 Legendary, etc.
Isso incentiva diversidade genética moderada!
```

---

## Implementação

### Algoritmo C# Completo

```csharp
public class CrystalSystemV2
{
    public enum Race { Forest, Mountain, Desert, Sea, Cave, Dark }
    public enum Tier { Common = 2, Uncommon = 5, Rare = 10, Epic = 18, Legendary = 40 }
    
    public class Gene
    {
        public Race DD { get; set; }
        public Race R1 { get; set; }
        public Race R2 { get; set; }
    }
    
    public class Goblin
    {
        // Físicas
        public Gene Skin, Hair, Eyes, Ear, Mouth, Nose;
        // Cores
        public Gene SkinColor, HairColor, PupilColor, EyeColor;
        
        public Gene[] AllPhysical => new[] { Skin, Hair, Eyes, Ear, Mouth, Nose };
        public Gene[] AllColors => new[] { SkinColor, HairColor, PupilColor, EyeColor };
        public Gene[] All => AllPhysical.Concat(AllColors).ToArray();
    }
    
    public class Crystal
    {
        public Race Race { get; set; }
        public Tier Tier { get; set; }
        public string Name { get; set; }
        public int Points => (int)Tier;
    }
    
    // Método principal
    public List<Crystal> GenerateCrystals(Goblin goblin)
    {
        List<Crystal> allCrystals = new List<Crystal>();
        
        foreach (Race race in Enum.GetValues(typeof(Race)))
        {
            List<Crystal> raceCrystals = CheckRaceRules(goblin, race);
            allCrystals.AddRange(raceCrystals);
        }
        
        return allCrystals;
    }
    
    // Verifica TODAS as regras para uma raça e retorna TODOS os cristais aplicáveis
    private List<Crystal> CheckRaceRules(Goblin g, Race race)
    {
        List<Crystal> crystals = new List<Crystal>();
        
        // LEGENDARY
        if (CheckLegendary(g, race))
            crystals.Add(new Crystal { Race = race, Tier = Tier.Legendary, Name = GetName(race, Tier.Legendary) });
        
        // EPIC - verifica E-01 e E-02
        if (CheckEpic01(g, race))
            crystals.Add(new Crystal { Race = race, Tier = Tier.Epic, Name = GetName(race, "E-01") });
        if (CheckEpic02(g, race))
            crystals.Add(new Crystal { Race = race, Tier = Tier.Epic, Name = GetName(race, "E-02") });
        
        // RARE - verifica R-01, R-02, R-03
        if (CheckRare01(g, race))
            crystals.Add(new Crystal { Race = race, Tier = Tier.Rare, Name = GetName(race, "R-01") });
        if (CheckRare02(g, race))
            crystals.Add(new Crystal { Race = race, Tier = Tier.Rare, Name = GetName(race, "R-02") });
        if (CheckRare03(g, race))
            crystals.Add(new Crystal { Race = race, Tier = Tier.Rare, Name = GetName(race, "R-03") });
        
        // UNCOMMON - verifica U-01, U-02, U-03, U-04
        if (CheckUncommon01(g, race))
            crystals.Add(new Crystal { Race = race, Tier = Tier.Uncommon, Name = GetName(race, "U-01") });
        if (CheckUncommon02(g, race))
            crystals.Add(new Crystal { Race = race, Tier = Tier.Uncommon, Name = GetName(race, "U-02") });
        if (CheckUncommon03(g, race))
            crystals.Add(new Crystal { Race = race, Tier = Tier.Uncommon, Name = GetName(race, "U-03") });
        if (CheckUncommon04(g, race))
            crystals.Add(new Crystal { Race = race, Tier = Tier.Uncommon, Name = GetName(race, "U-04") });
        
        return crystals;
    }
    
    // Regras LEGENDARY (pureza total)
    private bool CheckLegendary(Goblin g, Race race)
    {
        return g.All.All(gene => 
            gene.DD == race && gene.R1 == race && gene.R2 == race);
    }
    
    // Regras EPIC (específicas por raça)
    private bool CheckEpic(Goblin g, Race race)
    {
        int ddPhys = CountDD(g.AllPhysical, race);
        int ddColor = CountDD(g.AllColors, race);
        int r1Total = CountR1(g.All, race);
        int r2Total = CountR2(g.All, race);
        
        switch (race)
        {
            case Race.Forest:
                return ddPhys >= 8 && ddColor >= 3;
            
            case Race.Mountain:
                return ddPhys >= 8 && r1Total >= 4 && ddColor >= 2;
            
            case Race.Desert:
                return ddPhys >= 4 && ddColor >= 3 && r1Total >= 5 && r2Total >= 3;
            
            case Race.Sea:
                return ddPhys >= 5 && ddColor >= 4 && r1Total >= 3;
            
            case Race.Cave:
                return CountDD(g.All, race) >= 8 && r1Total >= 5 && r2Total >= 2 &&
                       ddPhys + CountR1(g.AllPhysical, race) >= 6;
            
            case Race.Dark:
                return CountDD(g.All, race) >= 7 && r1Total >= 6 && 
                       CountPureCharacteristics(g, race) >= 2;
        }
        
        return false;
    }
    
    // Regras RARE (específicas por raça)
    private bool CheckRare(Goblin g, Race race)
    {
        int ddPhys = CountDD(g.AllPhysical, race);
        int ddColor = CountDD(g.AllColors, race);
        int r1Total = CountR1(g.All, race);
        
        switch (race)
        {
            case Race.Forest:
                return ddPhys >= 3 && ddColor >= 2 && r1Total >= 3;
            
            case Race.Mountain:
                return CountDD(g.All, race) >= 5 && 
                       CountPureCharacteristics(g, race) >= 2;
            
            case Race.Desert:
                return CountDD(g.All, race) >= 6 && CountR1(g.AllColors, race) >= 2;
            
            case Race.Sea:
                return CountDD(g.All, race) >= 5 && r1Total >= 4 && 
                       CountPureCharacteristics(g, race) >= 1;
            
            case Race.Cave:
                return ddPhys >= 3 && ddColor >= 3 && CountR1(g.AllPhysical, race) >= 3;
            
            case Race.Dark:
                return ddPhys >= 3 && r1Total >= 5 && CountR1(g.AllColors, race) >= 2;
        }
        
        return false;
    }
    
    // Regras UNCOMMON (grupos específicos)
    private bool CheckUncommon(Goblin g, Race race)
    {
        switch (race)
        {
            case Race.Forest:
                // 3 DD em Skin+Hair+Eyes + 2 R1
                return HasDD(g.Skin, race) && HasDD(g.Hair, race) && 
                       HasDD(g.Eyes, race) && CountR1(g.All, race) >= 2;
            
            case Race.Mountain:
                // 4 DD em Skin+Ear+Nose+1cor + 1 R1
                return HasDD(g.Skin, race) && HasDD(g.Ear, race) && 
                       HasDD(g.Nose, race) && CountDD(g.AllColors, race) >= 1 && 
                       CountR1(g.All, race) >= 1;
            
            case Race.Desert:
                // 3 DD em Eyes+Mouth+Nose + 3 R1
                return HasDD(g.Eyes, race) && HasDD(g.Mouth, race) && 
                       HasDD(g.Nose, race) && CountR1(g.All, race) >= 3;
            
            case Race.Sea:
                // 4 DD (2 físicas + 2 cores) + 2 R1 físicas
                return CountDD(g.AllPhysical, race) >= 2 && 
                       CountDD(g.AllColors, race) >= 2 && 
                       CountR1(g.AllPhysical, race) >= 2;
            
            case Race.Cave:
                // 3 DD em Skin+Eyes+Ear + 4 R1
                return HasDD(g.Skin, race) && HasDD(g.Eyes, race) && 
                       HasDD(g.Ear, race) && CountR1(g.All, race) >= 4;
            
            case Race.Dark:
                // 4 DD em Hair+Mouth+Nose+1cor + 2 R1
                return HasDD(g.Hair, race) && HasDD(g.Mouth, race) && 
                       HasDD(g.Nose, race) && CountDD(g.AllColors, race) >= 1 && 
                       CountR1(g.All, race) >= 2;
        }
        
        return false;
    }
    
    // Regras COMMON (simples)
    private bool CheckCommon(Goblin g, Race race)
    {
        switch (race)
        {
            case Race.Forest:
                return CountDD(g.AllPhysical, race) >= 2;
            
            case Race.Mountain:
                return CountDD(g.AllPhysical, race) >= 1 && CountDD(g.AllColors, race) >= 1;
            
            case Race.Desert:
                return CountDD(g.AllColors, race) >= 2;
            
            case Race.Sea:
                return CountDD(g.All, race) >= 3;
            
            case Race.Cave:
                return HasDD(g.Eyes, race) && 
                       (HasDD(g.PupilColor, race) || HasDD(g.EyeColor, race));
            
            case Race.Dark:
                return CountDD(g.AllPhysical, race) >= 2 || CountDD(g.All, race) >= 3;
        }
        
        return false;
    }
    
    // Helpers
    private bool HasDD(Gene gene, Race race) => gene.DD == race;
    private int CountDD(Gene[] genes, Race race) => genes.Count(g => g.DD == race);
    private int CountR1(Gene[] genes, Race race) => genes.Count(g => g.R1 == race);
    private int CountR2(Gene[] genes, Race race) => genes.Count(g => g.R2 == race);
    
    private int CountPureCharacteristics(Goblin g, Race race)
    {
        return g.All.Count(gene => 
            gene.DD == race && gene.R1 == race && gene.R2 == race);
    }
    
    private string GetName(Race race, Tier tier)
    {
        var names = new Dictionary<(Race, Tier), string>
        {
            { (Race.Forest, Tier.Common), "Peridoto Selvagem" },
            { (Race.Forest, Tier.Uncommon), "Jade Musgoso" },
            { (Race.Forest, Tier.Rare), "Esmeralda Real" },
            { (Race.Forest, Tier.Epic), "Esmeralda Imperial" },
            { (Race.Forest, Tier.Legendary), "Esmeralda da Floresta Ancestral" },
            // ... adicionar todos os 30 cristais
        };
        return names[(race, tier)];
    }
    
    public string GetGoblinRarity(List<Crystal> crystals)
    {
        int total = crystals.Sum(c => c.Points);
        if (total <= 4) return "Common";
        if (total <= 11) return "Uncommon";
        if (total <= 19) return "Rare";
        if (total <= 35) return "Epic";
        return "Legendary";
    }
}
```

---

## Tabelas de Referência

### Resumo: Múltiplos Cristais por Raça

| Raça | Cristais Possíveis | Distribuição | Máx. Pontos por Raça | Máx. Pontos Total |
|------|-------------------|--------------|----------------------|-------------------|
| Forest | 10 (1L + 2E + 3R + 4U) | 1+2+3+4 | 146 | - |
| Mountain | 10 (1L + 2E + 3R + 4U) | 1+2+3+4 | 146 | - |
| Desert | 10 (1L + 2E + 3R + 4U) | 1+2+3+4 | 146 | - |
| Sea | 10 (1L + 2E + 3R + 4U) | 1+2+3+4 | 146 | - |
| Cave | 10 (1L + 2E + 3R + 4U) | 1+2+3+4 | 146 | - |
| Dark | 10 (1L + 2E + 3R + 4U) | 1+2+3+4 | 146 | - |
| **Total** | **60 únicos** | **6+12+18+24** | **876 máximo** | **876** |

---

### Quick Reference: Thresholds e Pontos

```
GOBLIN RARITY (soma de pontos):
0-15:     Common      (0-3 Uncommon)
16-35:    Uncommon    (4-8 Uncommon, ou 2-3 Rare)
36-75:    Rare        (Múltiplos Rare/Epic)
76-150:   Epic        (Vários Epic e possivelmente Legendary)
151+:     Legendary   (Múltiplos Legendary)

CRYSTAL POINTS:
Uncommon:  4 pontos   (4 por raça = 24 totais, máx. 96 pts)
Rare:      12 pontos  (3 por raça = 18 totais, máx. 216 pts)
Epic:      22 pontos  (2 por raça = 12 totais, máx. 264 pts)
Legendary: 50 pontos  (1 por raça = 6 totais, máx. 300 pts)

ESTRUTURA:
- Sem tier Common (mínimo é Uncommon)
- Total de 60 cristais únicos
- Máximo 60 cristais por goblin (todos os cristais possíveis)
- Máximo teórico: 876 pontos (todos os 60 cristais)
```

---

### Tabela de IDs dos Cristais

| Raça | L | E-01 | E-02 | R-01 | R-02 | R-03 | R-04 | U-01 | U-02 | U-03 | U-04 | U-05 | U-06 |
|------|---|------|------|------|------|------|------|------|------|------|------|------|------|
| **Forest** | F-L | F-E01 | F-E02 | F-R01 | F-R02 | F-R03 | F-R04 | F-U01 | F-U02 | F-U03 | F-U04 | F-U05 | F-U06 |
| **Mountain** | M-L | M-E01 | M-E02 | M-R01 | M-R02 | M-R03 | M-R04 | M-U01 | M-U02 | M-U03 | M-U04 | M-U05 | M-U06 |
| **Desert** | D-L | D-E01 | D-E02 | D-R01 | D-R02 | D-R03 | D-R04 | D-U01 | D-U02 | D-U03 | D-U04 | D-U05 | D-U06 |
| **Sea** | S-L | S-E01 | S-E02 | S-R01 | S-R02 | S-R03 | S-R04 | S-U01 | S-U02 | S-U03 | S-U04 | S-U05 | S-U06 |
| **Cave** | C-L | C-E01 | C-E02 | C-R01 | C-R02 | C-R03 | C-R04 | C-U01 | C-U02 | C-U03 | C-U04 | C-U05 | C-U06 |
| **Dark** | K-L | K-E01 | K-E02 | K-R01 | K-R02 | K-R03 | K-R04 | K-U01 | K-U02 | K-U03 | K-U04 | K-U05 | K-U06 |

---

### Regras Rápidas por Tier

#### Legendary (40 pts) - 6 cristais total
```
Todas as raças: 10 DD + 10 R1 + 10 R2 (pureza 100%)
Extremamente raro: 1 em 21.5 trilhões
```

#### Epic (18 pts) - 12 cristais total
```
Fórmulas típicas:
- 5-7 DD (4-5 físicas + 2-4 cores) + 3-6 R1 + pureza parcial
- Alta concentração + distribuição balanceada
Raro: ~1 em 10,000
```

#### Rare (10 pts) - 24 cristais total
```
Fórmulas típicas:
- 3-6 DD (distribuição variada) + 2-5 R1
- Pureza em 1-2 características
- Grupos específicos com R2
Moderadamente raro: ~1 em 200
```

#### Uncommon (5 pts) - 36 cristais total
```
Fórmulas típicas:
- 2-4 DD (localização específica) + 1-4 R1
- Grupos faciais, corporais ou cromáticos
- Distribuição física/cor
Comum: ~1 em 6
```

---

### FAQ

**P: Um goblin pode ter Peridoto Selvagem (F-U03) E Jade Musgoso (F-U01)?**  
R: SIM! Agora um goblin pode ter MÚLTIPLOS cristais da mesma raça, desde que satisfaça todas as regras.

**P: Um goblin pode ter TODOS os cristais Forest ao mesmo tempo?**  
R: Teoricamente sim, se satisfizer todas as 10 regras de Forest simultaneamente (seria um goblin extremamente raro).

**P: Como o sistema decide quais cristais Forest o goblin recebe?**  
R: O sistema verifica TODAS as regras de todas as raridades:
   1. Legendary (F-L)
   2. Epic (F-E01, F-E02)
   3. Rare (F-R01, F-R02, F-R03)
   4. Uncommon (F-U01, F-U02, F-U03, F-U04)
   
   TODOS os cristais cujas regras forem satisfeitas são atribuídos.

**P: Um goblin com muitos genes Forest sempre recebe Legendary?**  
R: Não. Precisa ter EXATAMENTE 30 genes Forest (100% puro). Qualquer gene de outra raça desqualifica.

**P: Quantos cristais um goblin pode ter?**  
R: Mínimo 0, máximo 60 (todos os cristais de todas as raças - teoricamente impossível na prática).

**P: Qual a combinação mínima para Legendary Goblin?**  
R: 151 pontos. Exemplos:
   - 4× Legendary (50×4 = 200)
   - 3× Legendary + 1× Uncommon (150+4 = 154)
   - 7× Epic (22×7 = 154)
   - 13× Rare (12×13 = 156)
   - Combinações mistas de alta raridade

**P: Um goblin 100% puro é automaticamente Legendary Goblin?**  
R: NÃO! Um goblin 100% puro de uma única raça terá no máximo todos os 10 cristais daquela raça (50+44+36+16 = 146 pontos), que resulta em **Epic Goblin** (76-150).
   Para ser Legendary Goblin (151+), precisa ter cristais de múltiplas raças com alta concentração.

**P: Por que não existem cristais Common?**  
R: Para valorizar todos os cristais. Uncommon é o novo "baseline" acessível.

**P: Como funciona a verificação de múltiplos cristais Epic/Rare da mesma raça?**  
R: TODAS as regras são verificadas independentemente. Se um goblin satisfaz E-01 E E-02 ao mesmo tempo, ele recebe AMBOS os cristais Epic daquela raça (44 pontos só de Epic).

**P: Quantos Uncommon diferentes de Forest existem?**  
R: 6 (F-U01 a F-U06). Mas um goblin só pode ter 1 deles (primeiro que satisfizer).

**P: É possível ter 6× Legendary?**  
R: Matematicamente sim (300 pontos), mas probabilidade é 0% na prática.
   Seria (1/6)^180 = menos que 1 em 10^140. Cada raça precisaria de 100% de pureza simultaneamente.

---

### Combinações Interessantes

#### Para Common Goblin (0-10 pts) - 50%
```
✓ 0× cristais                = 0 pts (comum - 8%)
✓ 1× Uncommon                = 5 pts (comum - 28%)
✓ 2× Uncommon                = 10 pts (comum - 13%)
✓ 1× Rare                    = 10 pts (raro - 1%)
```

#### Para Uncommon Goblin (11-20 pts) - 30%
```
✓ 3× Uncommon                = 15 pts (moderado)
✓ 1× Rare + 1× Uncommon      = 15 pts (raro)
✓ 1× Epic                    = 18 pts (muito raro)
✓ 2× Rare                    = 20 pts (raro)
✓ 4× Uncommon                = 20 pts (incomum)
```

#### Para Rare Goblin (21-35 pts) - 15%
```
✓ 1× Epic + 1× Uncommon      = 23 pts (muito raro)
✓ 5× Uncommon                = 25 pts (extremamente raro)
✓ 1× Epic + 1× Rare          = 28 pts (extremamente raro)
✓ 3× Rare                    = 30 pts (muito raro)
✓ 1× Rare + 3× Uncommon      = 25 pts (raro)
```

#### Para Epic Goblin (36-55 pts) - 4%
```
✓ 2× Epic                    = 36 pts (muito raro)
✓ 1× Legendary               = 40 pts (extremamente raro)
✓ 1× Epic + 2× Rare          = 38 pts (muito raro)
✓ 4× Rare                    = 40 pts (praticamente impossível)
✓ 1× Legendary + 1× Rare     = 50 pts (praticamente impossível)
✓ 3× Epic                    = 54 pts (praticamente impossível)
```

#### Para Legendary Goblin (56+ pts) - 1%
```
✓ 1× Legendary + 1× Epic              = 58 pts (praticamente impossível)
✓ 1× Legendary + 2× Rare              = 60 pts (praticamente impossível)
✓ 4× Epic                             = 72 pts (impossível)
✓ 1× Legendary + 2× Epic              = 76 pts (impossível)
✓ 2× Legendary                        = 80 pts (impossível)
✓ 1× Legendary + 1× Epic + 2× Rare    = 76 pts (impossível)
```

---

### Distribuição Esperada em 10,000 Goblins

| Categoria | Quantidade | % |
|-----------|------------|---|
| **Por Raridade do Goblin** |
| Common (0-10) | 5,000 | 50% |
| Uncommon (11-20) | 3,000 | 30% |
| Rare (21-35) | 1,500 | 15% |
| Epic (36-55) | 400 | 4% |
| Legendary (56+) | 100 | 1% |
| **Por Quantidade de Cristais** |
| 0 cristais | 800 | 8% |
| 1 cristal | 2,800 | 28% |
| 2 cristais | 3,500 | 35% |
| 3 cristais | 2,000 | 20% |
| 4 cristais | 700 | 7% |
| 5 cristais | 180 | 1.8% |
| 6 cristais | 20 | 0.2% |
| **Por Tipo de Cristal** |
| Pelo menos 1 Uncommon | 7,000 | 70% |
| Pelo menos 1 Rare | 300 | 3% |
| Pelo menos 1 Epic | 6 | 0.06% |
| Pelo menos 1 Legendary | ~0 | ~0% |

---

## Changelog

### Versão 4.0 (Atual - Janeiro 2026)
- **REMOVIDA** a limitação de um cristal por raça
- **Múltiplos cristais da mesma raça** agora são possíveis
- Sistema verifica TODAS as regras e atribui TODOS os cristais aplicáveis
- **Máximo teórico**: 60 cristais (todos) = 876 pontos
- **Máximo por raça**: 10 cristais = 146 pontos
- **Novos thresholds de raridade do goblin**:
  * Common: 0-15 pontos (45%)
  * Uncommon: 16-35 pontos (30%)
  * Rare: 36-75 pontos (18%)
  * Epic: 76-150 pontos (5%)
  * Legendary: 151+ pontos (2%)
- **Probabilidades recalculadas** para refletir múltiplos cristais
- **Maior variedade**: Goblins agora podem ter combinações muito mais diversas
- **Sistema mais recompensador**: Genes fortes em uma raça geram múltiplos cristais

### Versão 3.0 (Janeiro 2026)
- **78 cristais únicos** (13 por raça: 1 Legendary + 2 Epic + 4 Rare + 6 Uncommon)
- **Removido tier Common** - Uncommon é o novo baseline
- **Distribuição proporcional à raridade**:
  * 6 Uncommon por raça (36 totais) - mais acessíveis
  * 4 Rare por raça (24 totais) - moderadamente raros
  * 2 Epic por raça (12 totais) - muito raros
  * 1 Legendary por raça (6 totais) - extremamente raros
- **Regras únicas e específicas** para cada um dos 78 cristais
- **Verificação hierárquica**: L → E-01 → E-02 → R-01...R-04 → U-01...U-06
- **Thresholds de raridade do goblin ajustados** (padrão tradicional 50-30-15-4-1):
  * Common: 0-10 pontos (0-2 Uncommon ou 1 Rare) - 50%
  * Uncommon: 11-20 pontos (3-4 Uncommon, 2 Rare, ou Epic) - 30%
  * Rare: 21-35 pontos (Epic+extras, 3 Rare) - 15%
  * Epic: 36-55 pontos (2 Epic, Legendary, múltiplos Rare) - 4%
  * Legendary: 56+ pontos (Legendary+Epic ou múltiplos extremos) - 1%
- **Sistema de IDs**: Cristais identificados por raça + tier + número (ex: F-U03, M-E01)
- **Probabilidades recalculadas** para nova distribuição
- **Balanceamento perfeito**: Todas as 6 raças têm exatamente 13 cristais

### Versão 2.0 (Dezembro 2025)
- Sistema hierárquico com regras específicas
- **30 cristais únicos** (6 raças × 5 tiers)
- **Regras não-repetitivas** para cada cristal
- Verificação **top-down** (Legendary → Common)
- **Um cristal por raça** (nunca 2 da mesma raça)
- Complexidade proporcional à raridade
- Balanceamento perfeito entre raças

### Versão 1.0 (Inicial)
- Sistema de múltiplos cristais por raça
- Problema: goblin podia ter "Esmeralda Menor" + "Jade Musgoso"
- 82 cristais com regras sobrepostas
- Sistema descontinuado

---

## Notas de Design

### Por que 78 cristais?

**Matemática**: 6 raças × 13 cristais = 78 totais

**Distribuição**: Queremos mais variedade nas raridades acessíveis (Uncommon/Rare) e menos nos extremos (Epic/Legendary).

```
Uncommon: 24 cristais (40%) - Acessíveis e variados
Rare:     18 cristais (30%) - Moderadamente raros
Epic:     12 cristais (20%) - Muito valiosos
Legendary: 6 cristais (10%)  - Míticos
```

### Por que remover Common?

1. **Valor mínimo**: Todo cristal deve ter significado
2. **Simplicidade**: 4 tiers são mais claros que 5
3. **Balanceamento**: Uncommon como baseline funciona melhor
4. **Raridade do goblin**: Evita muitos goblins Common (0-4 pts mantém equilíbrio)

### Por que 4 Uncommon por raça?

- **Simplicidade**: Cada Uncommon tem uma regra clara e específica
  - U-01: 1 característica completa (DD + R1 + R2)
  - U-02: 3 DD
  - U-03: 3 R1
  - U-04: 3 R2
- **Acessibilidade**: ~45% dos goblins têm pelo menos 1 Uncommon
- **Simetria**: Regras consistentes entre todas as raças
- **Gameplay**: Jogadores entendem facilmente o sistema

### Por que 3 Rare por raça?

- **Progressão lógica**: 
  - R-01: 2 características completas (6 genes)
  - R-02: 5 DD
  - R-03: 5 R1
- **Gradiente**: Cria escada natural de Uncommon (3 genes) → Rare (5-6 genes) → Epic (7-9 genes)
- **Balanceamento**: Mantém raridade apropriada (~1.6% de chance)

### Por que 2 Epic por raça?

- **Variação**: E-01 focado em características completas (9 genes), E-02 em DD (7 genes)
- **Alta complexidade**: Ambos extremamente difíceis de alcançar
- **Valor**: Mantém Epic como tier verdadeiramente especial

### Decisões de Threshold

Thresholds da raridade do goblin foram ajustados para o **novo sistema mantendo proporção 50-30-15-4-1**:

- **Common (0-4)**: 50% dos goblins - maioria acessível com 0-1 Uncommon
- **Uncommon (5-12)**: 30% dos goblins - segundo tier mais comum, requer 2-3 Uncommon ou 1 Rare
- **Rare (13-24)**: 15% dos goblins - relativamente exclusivo, requer Rare+Uncommon, 2 Rare, ou Epic
- **Epic (25-50)**: 4% dos goblins - muito raro, requer Epic+extras, múltiplos Rare, ou Legendary
- **Legendary (51+)**: 1% dos goblins - extremamente raro, requer Legendary+extras ou múltiplos Epic

**Nota importante**: Um goblin 100% puro (Legendary crystal = 50 pts) é **Epic Goblin** (25-50), não Legendary Goblin. Isso incentiva diversidade genética moderada ao invés de pureza extrema. Para ser Legendary Goblin, é necessário ter cristal Legendary + pelo menos 1 Uncommon (54 pts), ou combinações de múltiplos cristais de alto valor.

**Progressão equilibrada**: O sistema segue uma distribuição clássica de raridade, onde cada tier é aproximadamente metade do anterior após Uncommon:
- Common → Uncommon: 50% → 30% (redução de 40%)
- Uncommon → Rare: 30% → 15% (redução de 50%)
- Rare → Epic: 15% → 4% (redução de 73%)
- Epic → Legendary: 4% → 1% (redução de 75%)
