# Guia de Raças e Genes de Goblins

## Índice
1. [Visão Geral](#visão-geral)
2. [Raças de Goblins](#raças-de-goblins)
3. [Sistema de Atributos](#sistema-de-atributos)
4. [Sistema de Genes](#sistema-de-genes)
5. [Herança Genética](#herança-genética)
6. [Raridades](#raridades)

---

## Visão Geral

O sistema de goblins é baseado em 6 raças diferentes, cada uma com características únicas que influenciam os atributos do goblin. Os atributos base de todos os goblins começam em 6 pontos e são modificados com base nas características raciais de cada parte do corpo.

### Atributos Base
Todos os goblins começam com os seguintes atributos:
- **Strength (Força)**: 6
- **Agility (Agilidade)**: 6
- **Vigor (Vigor)**: 6
- **Intelligence (Inteligência)**: 6
- **Charism (Carisma)**: 6
- **Perception (Percepção)**: 6

---

## Raças de Goblins

### 1. Forest (Floresta) - ID: 0
**Código Hexadecimal**: `0x31`

#### Bônus da Raça Principal
- Intelligence +1
- Perception +1
- Strength -1
- Agility -1

#### Bônus por Característica
| Característica | Atributo Positivo | Atributo Negativo | Feature |
|----------------|-------------------|-------------------|---------|
| **Skin** (Pele) | Charism +1 | Perception -1 | Magic Aptitude |
| **Hair** (Cabelo) | Intelligence +1 | Vigor -1 | Nature Defender |
| **Ear** (Orelha) | Strength +1 | Agility -1 | High Senses |
| **Eye** (Olho) | Perception +1 | Strength -1 | Vegan |
| **Mount** (Boca) | Agility +1 | Intelligence -1 | Survivalist |
| **Nose** (Nariz) | Perception +1 | Strength -1 | Keen Smell |

**Perfil**: Goblins da floresta são inteligentes e perceptivos, mas fisicamente mais fracos. Excelentes em magia e conexão com a natureza.

---

### 2. Mountain (Montanha) - ID: 1
**Código Hexadecimal**: `0x34`

#### Bônus da Raça Principal
- Vigor +1
- Perception +1
- Charism -1
- Intelligence -1

#### Bônus por Característica
| Característica | Atributo Positivo | Atributo Negativo | Feature |
|----------------|-------------------|-------------------|---------|
| **Skin** (Pele) | Vigor +1 | Charism -1 | Hypoalgia |
| **Hair** (Cabelo) | Strength +1 | Perception -1 | Greed |
| **Ear** (Orelha) | Agility +1 | Perception -1 | Born Artisan |
| **Eye** (Olho) | Vigor +1 | Intelligence -1 | Tired Vision |
| **Mount** (Boca) | Perception +1 | Agility -1 | Born Negotiator |
| **Nose** (Nariz) | Strength +1 | Agility -1 | Dusty |

**Perfil**: Goblins da montanha são resistentes e perceptivos, nascidos artesãos e negociadores. Menos carismáticos e inteligentes.

---

### 3. Desert (Deserto) - ID: 2
**Código Hexadecimal**: `0x32`

#### Bônus da Raça Principal
- Agility +1
- Intelligence +1
- Vigor -1
- Perception -1

#### Bônus por Característica
| Característica | Atributo Positivo | Atributo Negativo | Feature |
|----------------|-------------------|-------------------|---------|
| **Skin** (Pele) | Vigor +1 | Intelligence -1 | Improved Reflections |
| **Hair** (Cabelo) | Perception +1 | Charism -1 | Reckless |
| **Ear** (Orelha) | Charism +1 | Strength -1 | Perfect Balance |
| **Eye** (Olho) | Perception +1 | Vigor -1 | Shyness |
| **Mount** (Boca) | Agility +1 | Perception -1 | Soft Joints |
| **Nose** (Nariz) | Vigor +1 | Charism -1 | Heat Resistance |

**Perfil**: Goblins do deserto são ágeis e inteligentes, com equilíbrio perfeito. Tendem a ser imprudentes e tímidos.

---

### 4. Sea (Mar) - ID: 3
**Código Hexadecimal**: `0x36`

#### Bônus da Raça Principal
- Charism +1
- Perception +1
- Strength -1
- Vigor -1

#### Bônus por Característica
| Característica | Atributo Positivo | Atributo Negativo | Feature |
|----------------|-------------------|-------------------|---------|
| **Skin** (Pele) | Charism +1 | Strength -1 | Empathy |
| **Hair** (Cabelo) | Charism +1 | Intelligence -1 | Low Cardio |
| **Ear** (Orelha) | Strength +1 | Agility -1 | Amphibian |
| **Eye** (Olho) | Vigor +1 | Intelligence -1 | Disastrous |
| **Mount** (Boca) | Strength +1 | Vigor -1 | Melodious Voice |
| **Nose** (Nariz) | Perception +1 | Intelligence -1 | Salt Tracker |

**Perfil**: Goblins do mar são extremamente carismáticos e perceptivos, com habilidades anfíbias. Fisicamente mais fracos.

---

### 5. Cave (Caverna) - ID: 4
**Código Hexadecimal**: `0x33`

#### Bônus da Raça Principal
- Strength +1
- Vigor +1
- Charism -1
- Perception -1

#### Bônus por Característica
| Característica | Atributo Positivo | Atributo Negativo | Feature |
|----------------|-------------------|-------------------|---------|
| **Skin** (Pele) | Agility +1 | Perception -1 | Rigidity |
| **Hair** (Cabelo) | Strength +1, Charism +1 | Vigor -1 | Dyslexia |
| **Ear** (Orelha) | Intelligence +1 | Perception -1 | Sonar |
| **Eye** (Olho) | Agility +1 | Intelligence -1 | Myopic |
| **Mount** (Boca) | Vigor +1 | Charism -1 | Iron Stomach |
| **Nose** (Nariz) | Perception +1 | Vigor -1 | Echo Location |

**Perfil**: Goblins da caverna são fortes e resistentes, com estômago de ferro. Usam sonar em vez de visão, resultando em baixa percepção visual.

---

### 6. Dark (Escuridão) - ID: 5
**Código Hexadecimal**: `0x35`

#### Bônus da Raça Principal
- Agility +1
- Intelligence +1
- Strength -1
- Vigor -1

#### Bônus por Característica
| Característica | Atributo Positivo | Atributo Negativo | Feature |
|----------------|-------------------|-------------------|---------|
| **Skin** (Pele) | Intelligence +1 | Perception -1 | Occultist |
| **Hair** (Cabelo) | Perception +1 | Vigor -1 | Intolerant |
| **Ear** (Orelha) | Intelligence +1 | Agility -1 | Born Chemist |
| **Eye** (Olho) | Charism +1 | Agility -1 | Depression |
| **Mount** (Boca) | Perception +1 | Agility -1 | Elitist |
| **Nose** (Nariz) | Charism +1 | Vigor -1 | Mysterious Aura |

**Perfil**: Goblins das trevas são inteligentes e ágeis, com aptidão para ocultismo e química. Tendem a ser elitistas e intolerantes.

---

## Sistema de Atributos

### Valores Máximos e Mínimos

Com o sistema de bônus balanceado, os atributos podem variar:

- **Valor Mínimo**: 1 (garantido por validação)
- **Valor Máximo Teórico**: 11-12
- **Faixa Prática**: 5-8 pontos

⚠️ **Importante**: O sistema aplica validação automática para garantir que nenhum atributo fique abaixo de 1 ou acima de 15.

### Descrição dos Atributos

1. **Strength (Força)**
   - Influencia ataques físicos e capacidade de mineração
   - Importante para: Attack, Mining

2. **Agility (Agilidade)**
   - Influencia velocidade e capacidade de esquiva
   - Importante para: Stealth, Hunting

3. **Vigor (Vigor)**
   - Influencia resistência e pontos de vida
   - Importante para: Resistance, Mining

4. **Intelligence (Inteligência)**
   - Influencia habilidades mágicas e crafting
   - Importante para: Magic, Blacksmith, Tailoring

5. **Charism (Carisma)**
   - Influencia interações sociais
   - Importante para: Social

6. **Perception (Percepção)**
   - Influencia consciência e detecção
   - Importante para: Hunting, Stealth

### Como os Atributos são Calculados

Os atributos finais de um goblin são calculados da seguinte forma:

1. **Atributos Base**: Todos começam com 6 em cada atributo
2. **Bônus de Raça**: Aplicado com base na raça dominante
3. **Bônus por Característica**: Cada parte do corpo (Skin, Hair, Ear, Eye, Mount, Nose) pode ter uma raça diferente
4. **Total**: Soma de todos os bônus e penalidades
5. **Limites**: Nenhum atributo pode ser menor que 1 ou maior que 15

**Exemplo de Cálculo:**
```
Goblin da Floresta com:
- Race: Forest
- Skin: Forest  
- Hair: Mountain
- Ear: Desert
- Eye: Forest
- Mount: Cave
- Nose: Sea

Cálculo de Strength:
Base: 6
Race (Forest): -1
Hair (Mountain): +1
Mouth (Cave): não afeta
Nose (Sea): não afeta
= 6 pontos
```

---

## Sistema de Genes

### Estrutura Genética

Cada goblin possui um código genético armazenado como BigInteger de 31 bytes, onde cada característica é representada por 3 genes:

- **DD** (Dominant-Dominant): Gene dominante, peso 1.0
- **R1** (Recessive 1): Gene recessivo 1, peso 0.5
- **R2** (Recessive 2): Gene recessivo 2, peso 0.25

### Características Genéticas

Cada goblin possui genes para as seguintes características:

1. **Genre** (Gênero): Masculino (0x6d) ou Feminino (0x66)
2. **Skin** (Pele): 3 genes (DD, R1, R2)
3. **Hair** (Cabelo): 3 genes (DD, R1, R2)
4. **Eyes** (Olhos): 3 genes (DD, R1, R2)
5. **Ear** (Orelhas): 3 genes (DD, R1, R2)
6. **Mouth** (Boca): 3 genes (DD, R1, R2)
7. **Nose** (Nariz): 3 genes (DD, R1, R2)
8. **Skin Color** (Cor da Pele): 3 genes (DD, R1, R2)
9. **Hair Color** (Cor do Cabelo): 3 genes (DD, R1, R2)
10. **Pupil Color** (Cor da Pupila): 3 genes (DD, R1, R2)
11. **Eye Color** (Cor do Olho): 3 genes (DD, R1, R2)
12. **Race** (Raça): Determinada pela predominância genética
13. **Rarity** (Raridade): Valor de 0-255

### Posições dos Genes no Array de Bytes

| Posição | Característica | Detalhes |
|---------|---------------|----------|
| 0 | Genre | Gênero do goblin |
| 1-3 | Skin | DD, R1, R2 |
| 4-6 | Hair | DD, R1, R2 |
| 7-9 | Eyes | DD, R1, R2 |
| 10-12 | Ear | DD, R1, R2 |
| 13-15 | Mouth | DD, R1, R2 |
| 16-18 | Nose | DD, R1, R2 |
| 19-21 | Skin Color | DD, R1, R2 |
| 22-24 | Hair Color | DD, R1, R2 |
| 25-27 | Pupil Color | DD, R1, R2 |
| 28-30 | Eye Color | DD, R1, R2 |
| 29 | Race | Raça dominante |
| 30 | Rarity | Valor de raridade |

---

## Herança Genética

### Sistema de Breeding (Reprodução)

Quando dois goblins reproduzem, os genes do filho são determinados através do seguinte processo:

#### Probabilidade de Herança

Para cada característica (Skin, Hair, Eyes, etc.):

**Gene Dominante (DD):**
- 60% de chance de herdar do pai ou mãe (6 opções de cada genitor)
- 40% de chance de herdar genes recessivos dos pais (4 opções R1/R2)
- 2% de chance de mutação aleatória (quando roll = 50 ou 51)

**Genes Recessivos (R1 e R2):**
- Escolhidos aleatoriamente dos genes disponíveis (DD, R1, R2) dos pais
- 2% de chance de mutação aleatória para cada gene

#### Algoritmo de Mistura de Genes

```csharp
// Para cada característica, cria pool de genes:
Pool DD: [P1.DD, P1.DD, P1.DD, P2.DD, P2.DD, P2.DD, P1.R1, P2.R1, P1.R2, P2.R2]
Pool R1: [P1.DD, P1.R1, P1.R2]
Pool R2: [P2.DD, P2.R1, P2.R2]

// Embaralha e seleciona
// 2% de chance de gene completamente aleatório
```

### Determinação da Raça

A raça final do goblin é determinada por um sistema de pontuação:

1. Cada característica contribui pontos para sua raça:
   - Gene DD: 1.0 ponto
   - Gene R1: 0.5 pontos
   - Gene R2: 0.25 pontos

2. A raça com maior pontuação total vence

3. Em caso de empate, a raça é escolhida aleatoriamente entre as empatadas

**Exemplo:**
```
Skin: DD=Forest (1.0), R1=Mountain (0.5), R2=Desert (0.25)
Hair: DD=Forest (1.0), R1=Forest (0.5), R2=Forest (0.25)
Eyes: DD=Desert (1.0), R1=Desert (0.5), R2=Mountain (0.25)

Pontuação:
Forest: 1.0 + 1.0 + 0.5 + 0.25 = 2.75
Desert: 0.25 + 1.0 + 0.5 = 1.75
Mountain: 0.5 + 0.25 = 0.75

Raça Final: Forest
```

### Requisitos para Breeding

1. **Gêneros Diferentes**: Um deve ser macho, outro fêmea
2. **Não Podem Ser Irmãos**: Compartilhar mesmo pai ou mesma mãe
3. **Não Podem Ser Parentes Diretos**: Pai/filho ou mãe/filho
4. **Fora de Cooldown**: Ambos devem estar disponíveis
5. **Custo em GOBI**: Varia com a raridade e número de filhos

### Custos de Breeding

#### Por Raridade da Caixa Resultante

| Raridade da Caixa | Custo Base | Custo por Filho (Pai 1) | Custo por Filho (Pai 2) |
|-------------------|------------|------------------------|------------------------|
| Common | 350 GOBI | +100 GOBI | +100 GOBI |
| Uncommon | 700 GOBI | +200 GOBI | +200 GOBI |
| Rare | 2000 GOBI | +500 GOBI | +500 GOBI |

**Fórmula:**
```
Custo Total = Custo Base + (Filhos Pai 1 × Custo por Filho) + (Filhos Pai 2 × Custo por Filho)
```

**Exemplo:**
```
Pai 1 (Uncommon) com 2 filhos + Mãe (Rare) com 1 filho = Uncommon Box
Custo = 700 + (2 × 200) + (1 × 200) = 700 + 400 + 200 = 1300 GOBI
```

### Cooldown Após Breeding

- **Pais**: 5 dias de cooldown
- **Filho**: 5 dias de cooldown inicial

---

## Raridades

### Sistema de Raridade

As raridades determinam a qualidade geral do goblin e são representadas por um valor numérico de 0-255:

| Raridade | Enum ID | Faixa de Valor | Descrição |
|----------|---------|----------------|-----------|
| Common | 0 | 0-127 | Goblins comuns |
| Uncommon | 1 | 128-209 | Goblins incomuns |
| Rare | 2 | 210-254 | Goblins raros |
| Epic | 3 | 255 | Goblins épicos |
| Legendary | 4 | 255+ | Goblins lendários |

### Raridade por Tipo de Gobox

Quando um goblin nasce de uma Gobox, sua raridade é determinada aleatoriamente dentro da faixa:

| Tipo de Gobox | Faixa de Raridade |
|---------------|-------------------|
| GoboxCommon | 0-254 (aleatório) |
| GoboxUncommon | 128-254 (128 + aleatório até 126) |
| GoboxRare | 210-254 (210 + aleatório até 44) |

### Herança de Raridade no Breeding

A raridade do filho é determinada pela média das raridades dos pais:

```csharp
Média = (Raridade Pai 1 + Raridade Pai 2) / 2

Se Média <= 127: Gobox Common
Se Média > 127 e <= 209: Gobox Uncommon  
Se Média > 209: Gobox Rare
```

O filho então recebe um valor de raridade aleatório dentro da faixa da Gobox resultante.

### Sistema de Fusion

Goblins da mesma raridade podem ser fundidos para aumentar a raridade:

| Raridade Atual | Custo de Fusion | Próxima Raridade |
|----------------|----------------|------------------|
| Common → Uncommon | 200 GOBI | Uncommon |
| Uncommon → Rare | 500 GOBI | Rare |
| Rare → Epic | 1000 GOBI | Epic |
| Epic → Legendary | 3000 GOBI | Legendary |
| Legendary | N/A | Não pode fundir |

**Requisitos:**
- Dois goblins da mesma raridade
- Custo em GOBI
- Um goblin é sacrificado (status = Fused)
- Goblin sobrevivente ganha 1 hora de cooldown

---

## Genes Possíveis por Característica

Cada característica física pode ter qualquer uma das 6 raças como gene:

### Lista de Genes Possíveis

Para todas as características (Skin, Hair, Eyes, Ear, Mouth, Nose):

| Gene ID | Nome | Hex Code |
|---------|------|----------|
| 0 | Forest | 0x31 |
| 1 | Mountain | 0x34 |
| 2 | Desert | 0x32 |
| 3 | Sea | 0x36 |
| 4 | Cave | 0x33 |
| 5 | Dark | 0x35 |

### Cores

As cores são determinadas pela raça dominante da característica "Color" correspondente:
- **Hair Color**: Determinado pelos genes HairColorDD, HairColorR1, HairColorR2
- **Skin Color**: Determinado pelos genes SkinColorDD, SkinColorR1, SkinColorR2
- **Pupil Color**: Determinado pelos genes PupilColorDD, PupilColorR1, PupilColorR2
- **Eye Color**: Determinado pelos genes EyeColorDD, EyeColorR1, EyeColorR2

Cada raça possui paletas de cores específicas definidas no `RaceColorService`.

---

## Resumo: Como Criar o Goblin Perfeito

### Para Força e Resistência (Tank/Miner)
**Raças Recomendadas:**
- Race: Cave ou Mountain
- Skin: Mountain ou Cave
- Hair: Mountain ou Cave
- Eye: Mountain
- Mount: Cave

**Atributos Focados:** Strength, Vigor

---

### Para Agilidade e Furtividade (Rogue)
**Raças Recomendadas:**
- Race: Desert ou Dark
- Skin: Cave
- Ear: Mountain ou Desert
- Eye: Cave
- Mount: Desert

**Atributos Focados:** Agility, Perception

---

### Para Magia e Inteligência (Mage)
**Raças Recomendadas:**
- Race: Forest ou Dark
- Skin: Dark
- Hair: Forest ou Dark
- Ear: Cave ou Dark

**Atributos Focados:** Intelligence, Perception

---

### Para Social e Carisma (Bard/Merchant)
**Raças Recomendadas:**
- Race: Sea
- Skin: Forest ou Sea
- Hair: Cave ou Sea
- Ear: Desert
- Eye: Dark
- Mount: Sea

**Atributos Focados:** Charism, Perception

---

## Notas Técnicas

### Representação Hexadecimal

- **Gênero Masculino**: 0x6d ('m')
- **Gênero Feminino**: 0x66 ('f')
- **Forest**: 0x31 ('1')
- **Desert**: 0x32 ('2')
- **Cave**: 0x33 ('3')
- **Mountain**: 0x34 ('4')
- **Dark**: 0x35 ('5')
- **Sea**: 0x36 ('6')

### Exemplo de Código Genético Completo

```
Byte Array (31 bytes):
[0]  = 0x6d (Male)
[1]  = 0x31 (Skin DD: Forest)
[2]  = 0x32 (Skin R1: Desert)
[3]  = 0x34 (Skin R2: Mountain)
[4]  = 0x31 (Hair DD: Forest)
... (continua para todas características)
[29] = 0x31 (Race: Forest)
[30] = 0x85 (Rarity: 133 = Uncommon)
```

Este código genético é convertido em BigInteger para armazenamento e pode ser convertido de volta para leitura das características individuais.

---

## Changelog

- **Versão 1.2**: Ajuste de atributos base
  - Reduzidos atributos base de 7 para 6 pontos
  - Recalculados valores máximos (11-12) e faixa prática (5-8)
  - Sistema permanece balanceado com maior diferenciação entre builds
- **Versão 1.1**: Balanceamento do sistema de atributos
  - Adicionado bônus de Nose (Nariz) para todas as 6 raças
  - Corrigido Cave Hair: agora possui penalidade em Vigor (-1)
  - Adicionados limites de valores (mín: 1, máx: 15)
  - Documentados valores máximos e mínimos esperados
- **Versão 1.0**: Documentação inicial baseada no código-fonte do sistema de Goblins Wars
