# ⚔ DUNGEON-CRAWLER
Projeto desenvolvido como parte da segunda avaliação da disciplina Programação 1, por Alycia Brasil e Paulo Amaral. Trata-se de um jogo no estilo **Dungeon Crawler**, com foco em **aventura e resolução de puzzles**, que desafia o jogador a avançar por três fases com dificuldade progressiva.

## 📜 Sobre o Projeto

Você joga como Detetive Perani, tentando capturar o criminoso conhecido como O Relojoeiro. Para encontrá-lo, você precisa seguir as pistas e atravessar diferentes fases cheias de perigos.
O objetivo principal é concluir três fases, superando obstáculos e inimigos em cada uma delas. Em todas as fases, o jogador deve encontrar uma chave para abrir a porta trancada e seguir para a próxima etapa.
Conforme o jogador avança, a dificuldade aumenta, com o surgimento de novos inimigos, armadilhas e mecânicas interativas que tornam a jogabilidade mais desafiadora e estratégica.

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
| `&`     | Representa o **jogador** conhecido como "Detetive Perani". Este é o personagem controlado pelo usuário.                                                                                       |
| `P`     | Representa um **NPC** que é o ajudante do Detetive e conta sobre o crime.                                                                                                                     |
| `*`     | **Parede**. O jogador não pode atravessar paredes. Elas funcionam como barreiras.                                                                                                             |
| `@`     | **Chave**. Quando o jogador interage com a chave, a porta de saída é destrancada.                                                                                                             |
| `D`     | **Porta fechada**. Bloqueia a saída até que o jogador colete a chave.                                                                                                                         |
| `=`     | **Porta aberta**. Aparece após a interação com a chave e permite concluir a fase.                                                                                                             |
| `O`     | **Botão de ação**. Fica no chão e o jogador precisa ficar sobre ele para ativá-lo. A ação resultante do botão é desativar os espinhos |
| `#`     | **Espinhos**. Se o jogador tocar neles, a fase é reiniciada. Após três reinícios, o jogo retorna ao menu principal.                                                                           |
| `>`     | **Teletransporte**. Sempre vem em pares. Leva o jogador de um ponto a outro instantaneamente.                                                                                                 |
| `X`     | **Capanga**. Move-se aleatoriamente (cima, baixo, esquerda, direita). Se encostar no jogador, a fase é reiniciada.                                                                    |
| `V`     | **O Relojoeiro**. Possui inteligência para seguir o jogador. Se encostar no jogador, a fase é reiniciada.                                                                                  |


## 🗺️ Telas e Estrutura do Jogo

O jogo é composto por diversas telas e fases que guiam a experiência do jogador. Abaixo está a descrição de cada uma:

### 🖥 Telas do Jogo

* **Menu Principal**
  Exibe o título do jogo e três opções principais:
 ![Captura de Tela (2)](https://github.com/user-attachments/assets/ce67d6b9-0d99-4cce-9190-8b8c61d98e82)
  * **Jogar**: Inicia o jogo a partir da Vila.
  * **Créditos**: Exibe os nomes dos desenvolvedores.
  * **Sair**: Mostra uma mensagem de despedida e encerra o programa.


* **Créditos**
  Tela com os nomes dos criadores do jogo.

![Captura de Tela (3)](https://github.com/user-attachments/assets/10f60eff-2145-45c0-8147-38ade8273b0e)

* **Sair**
  Tela com uma mensagem de encerramento simpática antes de fechar o jogo.

* **Museu (Tutorial)**
  Fase introdutória que contextualiza o jogador, contem o ajudante do Detetive (NPC), a chave e a porta para a fase inicial.


![Captura de Tela (4)](https://github.com/user-attachments/assets/62ac5aa7-ba33-4a73-9c69-c49df62d2cc9)

* **Tentativas**
  O jogador tem até 3 tentativas de vida, quando perde uma, aparece na tela quantas tentativas ele ainda possui antes de definir derrota.

  ![Captura de Tela (6)](https://github.com/user-attachments/assets/1c64bbf4-ae4e-4f90-b76e-e18d98bab178)


* **Vitória** 🏆
  Exibida quando o jogador conclui a Fase 3. Mostra uma mensagem de parabéns e retorna ao menu principal.

![Captura de Tela (8)](https://github.com/user-attachments/assets/90fa0062-4eca-4890-895e-851f5e9c9040)

* **Derrota** ☠
  Exibida quando o jogador perde. Mostra uma mensagem e retorna ao menu principal.

![Captura de Tela (7)](https://github.com/user-attachments/assets/be42c76f-4e65-4930-8e1e-376a8401e703)


### 🧭 Fases do Jogo

Cada fase possui tamanho e elementos específicos, aumentando em complexidade:

| Fase                | Dimensão | Elementos                                                 |
| ------------------- | -------- | --------------------------------------------------------- |
| **Museu (Tutorial)** | 10x10    | NPCs, paredes, chave e porta                              |
| **Fase 1**          | 10x10    | Jogador, paredes, chave e porta                           |
| **Fase 2**          | 20x20    | Todos da Fase 1 + botão, espinhos e Capanga (`X`) |
| **Fase 3**          | 40x40    | Todos da Fase 2 + teletransporte e O Relojoeiro (`V`)  |

O diagrama a seguir demonstra como funciona a transição entre as telas do jogo.
![Captura de Tela (1)](https://github.com/user-attachments/assets/ea5a9a73-f4c5-4cef-b0fb-b1f26dea3361)
