# 🧩 Especificação do Sistema – Campo Minado

## 🎯 Objetivo

Desenvolver um jogo **Campo Minado** em **linguagem C**, com base em uma grade de células onde o jogador precisa descobrir todas as casas **sem minas**, marcando aquelas que contêm bombas.  
O jogo deve oferecer **feedback visual** a cada jogada.

---

## ⚙️ Requisitos Funcionais

- Permitir que o jogador **defina o tamanho do tabuleiro** (por exemplo, 8x8, 10x10).  
- Permitir que o jogador **escolha a dificuldade**, que determinará o número de minas.  
- **Gerar aleatoriamente** as minas pelo tabuleiro.  
- Permitir **revelar uma célula**.  
- Permitir **marcar uma célula com bandeira** (indicando mina suspeita).  
- Mostrar a **quantidade de minas adjacentes** quando uma célula é revelada.  
- Mostrar o **tabuleiro atualizado** a cada jogada.  
- Indicar **vitória ou derrota**.  

---

## ⚙️ Requisitos Não Funcionais

- Implementado em **linguagem C**.  
- Utilizar **estruturas de dados adequadas** (matrizes e structs).  
- Interação via **terminal** (entrada e saída padrão).  
- Código **modular e comentado**.  

---

## 🧱 Estrutura de Dados

Usaremos uma **matriz de structs**, representando cada célula do tabuleiro:

```c
#define MAX 20

typedef struct {
    int temMina;        // 1 se há mina, 0 se não há
    int revelado;       // 1 se o jogador já revelou a célula
    int marcado;        // 1 se o jogador marcou com bandeira
    int minasAdjacentes;// número de minas ao redor
} Celula;

Celula tabuleiro[MAX][MAX];

---

## 🧱 Entrada de Dados


O usuário informa:

Tamanho do tabuleiro (linhas e colunas).

Dificuldade (1 = fácil, 2 = médio, 3 = difícil).

A cada rodada:

Ação: Revelar (R) ou Marcar (M).

Coordenadas: linha e coluna.

--- 