# 📘 Atividade: Jogo da Forca

## 🎯 Objetivo

Pratique manipulação de strings, listas, seleção aleatória, loops e condicionais ao criar um jogo da Forca em Python. O jogador deverá adivinhar uma palavra oculta antes de esgotar as tentativas.

## 📝 Tarefas

### 🛠️ Preparação do Jogo

#### Descrição
Prepare o estado inicial do jogo selecionando uma palavra aleatória da lista disponível e criando as variáveis necessárias para acompanhar os palpites.

#### Requisitos
O programa concluído deve:

- Selecionar aleatoriamente uma palavra da lista predefinida.
- Exibir cada letra ainda não descoberta como `_`, separando as posições para mostrar o progresso.
- Registrar as letras já tentadas e definir um limite de tentativas incorretas.
- Atualizar o progresso quando uma letra palpitada estiver na palavra e contar uma tentativa incorreta quando não estiver.

### 🛠️ Rodada e Encerramento da Partida

#### Descrição
Implemente o loop de interação para que o jogador possa palpitar letras até descobrir a palavra ou esgotar as tentativas.

#### Requisitos
O programa concluído deve:

- Solicitar um palpite de letra a cada rodada e aceitar letras maiúsculas ou minúsculas.
- Rejeitar entradas que não sejam uma única letra e não descontar tentativas por entradas inválidas ou letras já tentadas.
- Exibir o progresso da palavra e o número de tentativas incorretas restantes após cada palpite válido.
- Encerrar a partida quando todas as letras forem descobertas ou quando o limite de tentativas incorretas for atingido.
- Exibir uma mensagem indicando vitória ou derrota; em caso de derrota, revelar a palavra.
