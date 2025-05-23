# ⚔ DUNGEON-CRAWLER
Projeto desenvolvido como parte da segunda avaliação da disciplina Programação 1, por Alycia Brasil e Paulo Amaral. Trata-se de um jogo no estilo **Dungeon Crawler**, com foco em **aventura e resolução de puzzles**, que desafia o jogador a avançar por três fases com dificuldade progressiva.

## ☆: .｡. Conceito .｡.:☆
Este é um jogo de aventura e quebra-cabeça (puzzle) onde o jogador assume o papel de protagonista em uma história interativa, impulsionada pela exploração e pela resolução de desafios.
O objetivo principal é concluir três fases, superando obstáculos e inimigos em cada uma delas. Em todas as fases, o jogador deve encontrar uma chave para abrir a porta trancada e seguir para a próxima etapa.
Conforme o jogador avança, a dificuldade aumenta, com o surgimento de novos monstros, armadilhas e mecânicas interativas que tornam a jogabilidade mais desafiadora e estratégica.

## 🎮 Comandos
O jogador possui os seguintes comando:
● W: O jogador movimenta uma unidade para cima;
● A: O jogador movimenta uma unidade para esquerda;
● S: O jogador movimenta uma unidade para baixo;
● D: O jogador movimenta uma unidade para direita;
● i: O jogador interage com o objeto que está em cima.

## 👾 Elementos gráficos
O jogo utiliza uma série de símbolos para representar os diferentes elementos presentes nas fases. Abaixo está a legenda com a descrição de cada um:

| Símbolo | Descrição                                                                                                                                                                                     |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `&`     | Representa o **jogador**. Este é o personagem controlado pelo usuário.                                                                                                                        |
| `P`     | Representa um **NPC** (personagem não jogável).                                                                                                                                               |
| `*`     | **Parede**. O jogador não pode atravessar paredes. Elas funcionam como barreiras.                                                                                                             |
| `@`     | **Chave**. Quando o jogador interage com a chave, a porta de saída é destrancada.                                                                                                             |
| `D`     | **Porta fechada**. Bloqueia a saída até que o jogador colete a chave.                                                                                                                         |
| `=`     | **Porta aberta**. Aparece após a interação com a chave e permite concluir a fase.                                                                                                             |
| `O`     | **Botão de ação**. Fica no chão e o jogador precisa ficar sobre ele para ativá-lo. A ação resultante do botão é definida pela equipe (ex: abrir passagens secretas, liberar armadilhas, etc). |
| `#`     | **Espinhos**. Se o jogador tocar neles, a fase é reiniciada. Após três reinícios, o jogo retorna ao menu principal.                                                                           |
| `>`     | **Teletransporte**. Sempre vem em pares. Leva o jogador de um ponto a outro instantaneamente.                                                                                                 |
| `X`     | **Monstro Nível 1**. Move-se aleatoriamente (cima, baixo, esquerda, direita). Se encostar no jogador, a fase é reiniciada.                                                                    |
| `V`     | **Monstro Nível 2**. Possui inteligência para seguir o jogador. Se encostar no jogador, a fase é reiniciada.                                                                                  |


## 🗺️ Telas e Estrutura do Jogo

O jogo é composto por diversas telas e fases que guiam a experiência do jogador. Abaixo está a descrição de cada uma:

### 🖥 Telas do Jogo

* **Menu Principal**
  Exibe o título do jogo e três opções principais:

  * **Jogar**: Inicia o jogo a partir da Vila.
  * **Créditos**: Exibe os nomes dos desenvolvedores.
  * **Sair**: Mostra uma mensagem de despedida e encerra o programa.

* **Créditos**
  Tela com os nomes dos criadores do jogo.

* **Sair**
  Tela com uma mensagem de encerramento simpática antes de fechar o jogo.

* **Vila (Tutorial)**
  Fase introdutória que ensina o jogador a jogar. Contém NPCs interativos com dicas e explicações. A entrada para a Masmorra (Fase 1) está localizada aqui.

* **Vitória** 🏆
  Exibida quando o jogador conclui a Fase 3. Mostra uma mensagem de parabéns e retorna ao menu principal.

* **Derrota** ☠
  Exibida quando o jogador perde. Mostra uma mensagem cômica e retorna ao menu principal.


### 🧭 Fases do Jogo

Cada fase possui tamanho e elementos específicos, aumentando em complexidade:

| Fase                | Dimensão | Elementos                                                 |
| ------------------- | -------- | --------------------------------------------------------- |
| **Vila (Tutorial)** | 10x10    | NPCs, paredes, chave e porta                              |
| **Fase 1**          | 10x10    | Jogador, paredes, chave e porta                           |
| **Fase 2**          | 20x20    | Todos da Fase 1 + botão, espinhos e Monstro Nível 1 (`X`) |
| **Fase 3**          | 40x40    | Todos da Fase 2 + teletransporte e Monstro Nível 2 (`V`)  |

O diagrama a seguir demonstra como funciona a transição entre as telas do jogo.
![Captura de Tela (1)](https://github.com/user-attachments/assets/ea5a9a73-f4c5-4cef-b0fb-b1f26dea3361)
