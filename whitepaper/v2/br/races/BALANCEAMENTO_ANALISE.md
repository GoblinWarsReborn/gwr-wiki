# Análise de Balanceamento - Sistema de Atributos Goblins

## Situação Atual

### Características que concedem bônus:
- **Race** (Raça Principal)
- **Skin** (Pele)
- **Hair** (Cabelo)
- **Ear** (Orelha)
- **Eye** (Olho)
- **Mount/Mouth** (Boca)
- **Nose** (Nariz) - ⚠️ **FALTANDO BÔNUS**

### Atributos Base
Todos os goblins começam com **7 pontos** em cada atributo:
- Strength (Força)
- Agility (Agilidade)
- Vigor (Vigor)
- Intelligence (Inteligência)
- Charism (Carisma)
- Perception (Percepção)

---

## Análise de Bônus/Penalidades Atuais (SEM Nose)

### Por Raça:

#### Forest (Floresta)
- Race: INT +1, PER +1, STR -1, AGI -1
- Skin: CHA +1, PER -1
- Hair: INT +1, VIG -1
- Ear: STR +1, AGI -1
- Eye: PER +1, STR -1
- Mount: AGI +1, INT -1

**Totais se todas partes forem Forest:**
- STR: 7 -1 +0 +0 +1 -1 +0 = **6**
- AGI: 7 -1 +0 +0 -1 +0 +1 = **6**
- VIG: 7 +0 +0 -1 +0 +0 +0 = **6**
- INT: 7 +1 +0 +1 +0 +0 -1 = **8**
- CHA: 7 +0 +1 +0 +0 +0 +0 = **8**
- PER: 7 +1 -1 +0 +0 +1 +0 = **8**

#### Mountain (Montanha)
- Race: VIG +1, PER +1, CHA -1, INT -1
- Skin: VIG +1, CHA -1
- Hair: STR +1, PER -1
- Ear: AGI +1, PER -1
- Eye: VIG +1, INT -1
- Mount: PER +1, AGI -1

**Totais se todas partes forem Mountain:**
- STR: 7 +0 +0 +1 +0 +0 +0 = **8**
- AGI: 7 +0 +0 +0 +1 +0 -1 = **7**
- VIG: 7 +1 +1 +0 +0 +1 +0 = **10** ⚠️
- INT: 7 -1 +0 +0 +0 -1 +0 = **5**
- CHA: 7 -1 -1 +0 +0 +0 +0 = **5**
- PER: 7 +1 +0 -1 -1 +0 +1 = **7**

#### Desert (Deserto)
- Race: AGI +1, INT +1, VIG -1, PER -1
- Skin: VIG +1, INT -1
- Hair: PER +1, CHA -1
- Ear: CHA +1, STR -1
- Eye: PER +1, VIG -1
- Mount: AGI +1, PER -1

**Totais se todas partes forem Desert:**
- STR: 7 +0 +0 +0 -1 +0 +0 = **6**
- AGI: 7 +1 +0 +0 +0 +0 +1 = **9**
- VIG: 7 -1 +1 +0 +0 -1 +0 = **6**
- INT: 7 +1 -1 +0 +0 +0 +0 = **7**
- CHA: 7 +0 +0 -1 +1 +0 +0 = **7**
- PER: 7 -1 +0 +1 +0 +1 -1 = **7**

#### Sea (Mar)
- Race: CHA +1, PER +1, STR -1, VIG -1
- Skin: CHA +1, STR -1
- Hair: CHA +1, INT -1
- Ear: STR +1, AGI -1
- Eye: VIG +1, INT -1
- Mount: STR +1, VIG -1

**Totais se todas partes forem Sea:**
- STR: 7 -1 -1 +0 +1 +0 +1 = **7**
- AGI: 7 +0 +0 +0 -1 +0 +0 = **6**
- VIG: 7 -1 +0 +0 +0 +1 -1 = **6**
- INT: 7 +0 +0 -1 +0 -1 +0 = **5**
- CHA: 7 +1 +1 +1 +0 +0 +0 = **10** ⚠️
- PER: 7 +1 +0 +0 +0 +0 +0 = **8**

#### Cave (Caverna)
- Race: STR +1, VIG +1, CHA -1, PER -1
- Skin: AGI +1, PER -1
- Hair: STR +1, CHA +1 (SEM NEGATIVO!) ⚠️
- Ear: INT +1, PER -1
- Eye: AGI +1, INT -1
- Mount: VIG +1, CHA -1

**Totais se todas partes forem Cave:**
- STR: 7 +1 +0 +1 +0 +0 +0 = **9**
- AGI: 7 +0 +1 +0 +0 +1 +0 = **9**
- VIG: 7 +1 +0 +0 +0 +0 +1 = **9**
- INT: 7 +0 +0 +0 +1 -1 +0 = **7**
- CHA: 7 -1 +0 +1 +0 +0 -1 = **6**
- PER: 7 -1 -1 +0 -1 +0 +0 = **4**

#### Dark (Escuridão)
- Race: AGI +1, INT +1, STR -1, VIG -1
- Skin: INT +1, PER -1
- Hair: PER +1, VIG -1
- Ear: INT +1, AGI -1
- Eye: CHA +1, AGI -1
- Mount: PER +1, AGI -1

**Totais se todas partes forem Dark:**
- STR: 7 -1 +0 +0 +0 +0 +0 = **6**
- AGI: 7 +1 +0 +0 -1 -1 -1 = **5**
- VIG: 7 -1 +0 -1 +0 +0 +0 = **5**
- INT: 7 +1 +1 +0 +1 +0 +0 = **10** ⚠️
- CHA: 7 +0 +0 +0 +0 +1 +0 = **8**
- PER: 7 +0 -1 +1 +0 +0 +1 = **8**

---

## Problemas Identificados

### 1. **Desbalanceamento Extremo**
- Mountain VIG pode chegar a **10** (base 7 + 3)
- Sea CHA pode chegar a **10** (base 7 + 3)
- Dark INT pode chegar a **10** (base 7 + 3)
- Enquanto outros atributos ficam em 4-5

### 2. **Cave Hair está quebrado**
- Cave Hair dá STR +1 e CHA +1 SEM NEGATIVO
- Todas as outras características têm um trade-off (positivo e negativo)

### 3. **Falta de balanceamento nas penalidades**
- Algumas raças acumulam muitas penalidades no mesmo atributo
- Cave Perception pode cair para 4

### 4. **Nose não tem bônus**
- Isso adiciona 6 novas oportunidades de modificação de atributos

---

## Cálculo de Valores Máximos e Mínimos Possíveis

### Cenário ATUAL (sem Nose)

Para cada atributo, o **máximo teórico** seria escolher todas as partes do corpo que dão bônus para aquele atributo:

#### Strength (Força)
- Base: 7
- Melhor Race: Cave (+1)
- Melhor Skin: nenhum (+0)
- Melhor Hair: Mountain (+1) ou Cave (+1)
- Melhor Ear: Forest (+1)
- Melhor Eye: nenhum (+0)
- Melhor Mount: Sea (+1)
- **Máximo: 7 + 1 + 1 + 1 + 1 = 11**

#### Agility (Agilidade)
- Base: 7
- Melhor Race: Desert (+1) ou Dark (+1)
- Melhor Skin: Cave (+1)
- Melhor Hair: nenhum (+0)
- Melhor Ear: Mountain (+1)
- Melhor Eye: Cave (+1)
- Melhor Mount: Forest (+1) ou Desert (+1)
- **Máximo: 7 + 1 + 1 + 1 + 1 + 1 = 12**

#### Vigor (Vigor)
- Base: 7
- Melhor Race: Mountain (+1) ou Cave (+1)
- Melhor Skin: Mountain (+1) ou Desert (+1)
- Melhor Hair: nenhum (+0)
- Melhor Ear: nenhum (+0)
- Melhor Eye: Mountain (+1) ou Sea (+1)
- Melhor Mount: Cave (+1)
- **Máximo: 7 + 1 + 1 + 1 + 1 = 11**

#### Intelligence (Inteligência)
- Base: 7
- Melhor Race: Forest (+1) ou Desert (+1) ou Dark (+1)
- Melhor Skin: Dark (+1)
- Melhor Hair: Forest (+1)
- Melhor Ear: Cave (+1) ou Dark (+1)
- Melhor Eye: nenhum (+0)
- Melhor Mount: nenhum (+0)
- **Máximo: 7 + 1 + 1 + 1 + 1 = 11**

#### Charism (Carisma)
- Base: 7
- Melhor Race: Sea (+1)
- Melhor Skin: Forest (+1) ou Sea (+1)
- Melhor Hair: Cave (+1) ou Sea (+1)
- Melhor Ear: Desert (+1)
- Melhor Eye: Dark (+1)
- Melhor Mount: nenhum (+0)
- **Máximo: 7 + 1 + 1 + 1 + 1 + 1 = 12**

#### Perception (Percepção)
- Base: 7
- Melhor Race: Forest (+1) ou Mountain (+1) ou Sea (+1)
- Melhor Skin: nenhum (+0)
- Melhor Hair: Desert (+1) ou Dark (+1)
- Melhor Ear: nenhum (+0)
- Melhor Eye: Forest (+1) ou Desert (+1)
- Melhor Mount: Mountain (+1) ou Dark (+1)
- **Máximo: 7 + 1 + 1 + 1 + 1 = 11**

### Resumo Máximos ATUAIS (sem Nose):
- **Strength**: 11
- **Agility**: 12 ⚠️ (maior)
- **Vigor**: 11
- **Intelligence**: 11
- **Charism**: 12 ⚠️ (maior)
- **Perception**: 11

### Mínimos Teóricos (pior combinação):
Escolhendo sempre as piores opções:

- **Strength**: 7 - 1 (race) - 1 (skin Sea) - 1 (ear Desert) - 1 (eye Forest) = **3**
- **Agility**: 7 - 1 (race) - 1 (ear Sea) - 1 (mount Mountain) - 1 (eye Dark) - 1 (ear Dark) = **2**
- **Vigor**: 7 - 1 (race) - 1 (hair Forest) - 1 (eye Desert) - 1 (mount Sea) = **3**
- **Intelligence**: 7 - 1 (race) - 1 (skin Desert) - 1 (eye Mountain) - 1 (mount Forest) - 1 (hair Sea) - 1 (eye Sea) = **1** ⚠️
- **Charism**: 7 - 1 (race) - 1 (skin Mountain) - 1 (mount Cave) - 1 (hair Desert) = **3**
- **Perception**: 7 - 1 (race) - 1 (skin Cave) - 1 (hair Mountain) - 1 (ear Mountain) - 1 (mount Desert) - 1 (skin Dark) - 1 (skin Forest) = **-1** ❌ (PROBLEMA!)

**ATENÇÃO**: É possível criar goblins com Perception abaixo de 1, o que viola a regra!

---

## Sugestões de Balanceamento

### Opção 1: Balanceamento Conservador (Recomendado)

#### Corrigir Cave Hair
- **Atual**: STR +1, CHA +1 (sem negativo)
- **Novo**: STR +1, CHA +1, **VIG -1**
- Feature: Dyslexia

#### Adicionar Nose com bônus moderados

Nose deve complementar o "tema" de cada raça sem criar novos máximos extremos:

| Raça | Nose Bônus | Feature |
|------|------------|---------|
| **Forest** | PER +1, STR -1 | Keen Smell (olfato aguçado) |
| **Mountain** | STR +1, AGI -1 | Dusty (fareja minérios) |
| **Desert** | VIG +1, CHA -1 | Heat Resistance |
| **Sea** | PER +1, INT -1 | Salt Tracker |
| **Cave** | PER +1, VIG -1 | Echo Location |
| **Dark** | CHA +1, VIG -1 | Mysterious Aura |

**Novos Máximos com Nose:**
- Strength: 11 + 1 (Mountain Nose) = **12**
- Agility: 12 (sem mudança) = **12**
- Vigor: 11 + 1 (Desert Nose) = **12**
- Intelligence: 11 (sem mudança) = **11**
- Charism: 12 + 1 (Dark Nose) = **13** ⚠️
- Perception: 11 + 1 (Forest/Sea/Cave Nose) = **12**

---

### Opção 2: Balanceamento Agressivo (Mais Equilibrado)

#### Mudanças necessárias:

1. **Corrigir Cave Hair**: STR +1, CHA +1, **VIG -1**

2. **Reduzir alguns bônus duplos**:
   - Sea: Reduzir um dos CHA +1 para evitar stackar muito

3. **Adicionar Nose balanceado**:

| Raça | Nose Bônus | Justificativa |
|------|------------|---------------|
| **Forest** | VIG +1, CHA -1 | Compensa baixo VIG |
| **Mountain** | INT +1, VIG -1 | Compensa baixo INT |
| **Desert** | STR +1, AGI -1 | Compensa baixo STR |
| **Sea** | AGI +1, CHA -1 | Compensa baixo AGI, reduz excesso CHA |
| **Cave** | PER +1, STR -1 | Compensa baixíssimo PER |
| **Dark** | VIG +1, INT -1 | Compensa baixo VIG, reduz excesso INT |

**Resultado Final Opção 2:**
- Range de atributos: **3 a 11** (mais balanceado)
- Sem nenhum atributo chegando a 12 ou 13
- Cada raça tem pontos fortes e fracos bem definidos

---

## Comparação de Opções

| Aspecto | Opção 1 (Conservador) | Opção 2 (Agressivo) |
|---------|----------------------|---------------------|
| **Máximo possível** | 13 | 11 |
| **Mínimo possível** | 1 | 3 |
| **Range total** | 12 pontos | 8 pontos |
| **Especialização** | Muito alta | Moderada |
| **Balanceamento** | Médio | Alto |
| **Mantém atual** | Sim | Requer mudanças |

---

## Recomendação Final

Recomendo a **Opção 1 (Conservador)** com ajustes menores:

### Mudanças Necessárias:

1. ✅ **Corrigir Cave Hair**: Adicionar VIG -1
2. ✅ **Adicionar Nose** conforme tabela Opção 1
3. ✅ **Limitar soma de penalidades**: Nenhum atributo pode receber mais de -4 total
4. ✅ **Validação no código**: Garantir que nenhum atributo seja < 1

### Valores Finais Recomendados:
- **Mínimo**: 1 (com validação hard-coded)
- **Máximo teórico**: 12-13
- **Médio prático**: 6-9

Isso mantém o espírito de especialização (goblins muito fortes em certas áreas) enquanto previne builds completamente quebradas.

---

## Implementação no Código

```csharp
// Validação após calcular todos os bônus
public static int ClampAttribute(int value)
{
    return Math.Max(1, Math.Min(15, value)); // Min 1, Max 15 (futuro-proof)
}

// Aplicar após calcular STR, AGI, VIG, INT, CHA, PER
goblin.Strength = ClampAttribute(calculatedStrength);
goblin.Agility = ClampAttribute(calculatedAgility);
// ... etc
```
