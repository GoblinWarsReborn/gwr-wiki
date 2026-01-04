# Mobile - Especificação de Telas

## 1. Tela Inicial

![Tela Principal](images/01-tela-principal.png)

### Elementos da Tela
- **Goblins do Time**: Os 3 goblins do time selecionado, exibindo nome e nível
- **Botão Principal**: "Continuar história"
- **Menu Inferior**:
  1. Arena
  2. Inventário
  3. Mina
  4. Meu Time

---

## 2. Continuar História

![Mapa](images/02-mapa.png)

### Navegação
- **Botão**: "Voltar" no topo
- **Mapa de Navegação Livre**: 
  - Linhas pontilhadas indicam caminhos não percorridos
  - Linhas sólidas indicam caminhos já percorridos
  - Círculos com escudo marcam pontos de combate
  - O mapa não fica completamente visível na tela, apenas a parte navegada

### Interação com Inimigos

![Mapa - Inimigo Selecionado](images/03-mapa-inimigo.png)

Ao clicar no escudo:
1. Zoom-in no escudo selecionado
2. Metade inferior exibe lista dos monstros oponentes com seus níveis
3. Botão "Lutar" na parte inferior direita

---

## 3. Arena

![Arena](images/04-arena.png)

### Elementos da Tela
- **Liga Atual**: Exibe a liga na qual está (ex: Liga de Bronze 3)
- **Oponentes**: 3 opções de time para lutar, dispostos em 3 colunas
- **Posição no Ranking**: Exibe a posição do team no placar
- **Botões**:
  - "Ver placar da liga" - Lista todas as posições da liga
  - "Voltar" na parte inferior esquerda

---

## 4. Combate

![Combate](images/11-combate.png)

### Layout da Batalha
- **Visão Isométrica**: 
  - 3 goblins na parte de baixo olhando para parte superior esquerda
  - 3 goblins oponentes olhando para a parte inferior direita
- **Topo da Tela**: 
  - Nome do time e status do oponente
  - Nome do time e status do jogador
  - Botão "Automático" no centro
- **Informações dos Goblins**:
  - Atributos e vida exibidos em cada goblin
- **Menu de Combate**: 
  - Parte inferior com opções de ataque
  - Estilo similar ao Axie Infinity

---

## 5. Inventário

![Inventário](images/05-inventario.png)

### Organização
- **Grade de Itens**: Lista em 4 colunas
- **Filtro**: Combo para filtrar por tipo de item
- **Interação**: Clicar no item abre a tela de detalhes

### Tela do Item

![Detalhes do Item](images/06-item.png)

**Elementos**:
1. Imagem do Item
2. Quantidade disponível
3. Menu superior direito:
   - Opção "Destruir"

---

## 6. Mina

![Mina](images/07-mina.png)

### Funcionalidade
- **Propósito**: Área onde goblins que não estão em times podem extrair itens e moedas
- **Navegação**: Livre navegação, tela não exibe a mina inteira simultaneamente
- **Mecânica**:
  - Quando o goblin estiver cheio, ele para de trabalhar
  - Jogador deve clicar no goblin para colher itens e moedas mineradas

---

## 7. Meu Time

![Meu Time](images/08-time.png)

### Tabulação
Duas abas principais: "Meu Time" e "Meus Goblins"

#### Aba: Meu Time
- **Lista do Time**: 3 goblins selecionados com botão de remover
- **Interação**: Clicar em um goblin abre a tela de detalhes
- **Espaços Vazios**: Ao clicar, exibe lista de goblins disponíveis

#### Lista de Goblins Disponíveis

![Goblins Disponíveis](images/09-goblins-disponiveis.png)

- Lista completa de goblins
- Goblins indisponíveis aparecem em cinza
- Exibe tempo restante para ficarem disponíveis

---

## 8. Tela do Goblin

![Detalhes do Goblin](images/10-goblin.png)

### Layout
- **Visualização**: Imagem animada do goblin à direita
- **Slots de Equipamento**:
  - Capacete
  - Ombros
  - Mão direita
  - Mão esquerda
  - Arma reserva
  - Peito
  - Braços
  - Pernas

### Funcionalidades
- **Equipamentos**: Clicar em um slot exibe lista de equipamentos disponíveis no inventário
- **Status**: Exibe todos os atributos do goblin:
  - Força
  - Agilidade
  - Vigor
  - Inteligência
  - Carisma
- **Navegação**: Botão "Voltar"