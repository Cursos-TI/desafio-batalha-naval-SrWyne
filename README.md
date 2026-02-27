Batalha Naval - MateCheck

Projeto desenvolvido em linguagem C como desafio de lógica e manipulação de matrizes, inspirado no clássico jogo Batalha Naval.

Sobre o Projeto

O sistema simula diferentes níveis de dificuldade do jogo Batalha Naval utilizando:

Matrizes 10x10 como tabuleiro

Posicionamento automático de navios

Validação de limites

Aplicação de habilidades especiais com áreas de efeito

Exibição visual do tabuleiro no terminal

O programa é dividido em três níveis:

NOVATO

AVENTUREIRO

MESTRE

Estrutura do Tabuleiro

O tabuleiro é representado por uma matriz:

int tabuleiro[10][10];

Linhas: 0 a 9

Colunas: A a J

Cada posição armazena um número representando o conteúdo da célula.

Legenda dos Valores

0 → Água
1 → Área afetada (Octaedro)
2 → Área afetada (Cruz)
3 → Navio
5 → Área afetada (Cone)

Nível NOVATO

O que acontece:

O tabuleiro é inicializado com água (0).

Um navio horizontal de tamanho 3 é posicionado.

Um navio vertical de tamanho 3 é posicionado.

O sistema verifica:

Se o navio ultrapassa o limite do tabuleiro.

Se já existe outro navio na posição.

Objetivo do nível:
Demonstrar posicionamento básico de navios com validação simples.

Nível AVENTUREIRO

O que muda:

O tabuleiro é reinicializado.

Navios horizontais e verticais são posicionados.

São adicionados:

Navio na diagonal principal.

Navio na diagonal secundária.

Novidades implementadas:

Posicionamento diagonal

Verificação de sobreposição

Manipulação mais avançada de matriz

Nível MESTRE

Neste nível o foco não é apenas navios, mas habilidades especiais com área de efeito.

O tabuleiro é reinicializado novamente e são aplicadas três habilidades:

Habilidade CONE

Representada por uma matriz 5x5:

0 0 1 0 0
0 1 1 1 0
1 1 1 1 1
0 0 0 0 0
0 0 0 0 0

Origem definida no código.

Marca o tabuleiro com valor 5.

Afeta células em formato de cone.

Habilidade CRUZ

Representação:

0 0 1 0 0
0 0 1 0 0
1 1 1 1 1
0 0 1 0 0
0 0 1 0 0

Aplicada com ajuste para centralização.

Marca o tabuleiro com valor 2.

Afeta células em formato de cruz.

Habilidade OCTAEDRO

Representação:

0 0 2 0 0
0 2 2 2 0
2 2 2 2 2
0 2 2 2 0
0 0 2 0 0

Aplicada com ajuste de deslocamento.

Marca o tabuleiro com valor 1.

Forma um padrão semelhante a um losango expandido.

Regras Implementadas no Código

Verificação de limite do tabuleiro

Verificação de sobreposição

Aplicação de matriz auxiliar sobre matriz principal

Centralização de habilidades

Impressão formatada do tabuleiro

Como Executar

Compile o código:

gcc batalhanaval.c -o batalhanaval

Execute:

./batalhanaval

O programa exibirá no terminal:

Tabuleiro NOVATO

Tabuleiro AVENTUREIRO

Tabuleiro MESTRE

Conceitos Trabalhados

Matrizes bidimensionais

Estruturas de repetição (for)

Estruturas condicionais (if)

Validação de limites

Lógica espacial

Manipulação de coordenadas

Simulação de área de efeito