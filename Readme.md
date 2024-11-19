# Projeto de Jogo

## Membros do Projeto
- **Gabriel Garcia** - [Gabrieelgc2](https://github.com/Gabrieelgc2)
- **Vyktor Nascimento** - [VyNas07](https://github.com/VyNas07/VyNas07)
- **Isaac** - [Isaac-Daniel-A-D](https://github.com/Isaac-Daniel-A-D)

## Disciplina
**Programação Imperativa e Funcional - 2024.2**

## Instituição de Ensino
**Cesar School**

## Nome do Jogo
*Nome do jogo a ser desenvolvido*

## Instruções para Compilar e Executar o Jogo
*Instruções detalhadas para compilar e executar o jogo*

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Descrição do Jogo

Conceito Geral: O jogo é um escape room em um ambiente 3D, onde o jogador explora um quarto e interage com objetos para resolver enigmas e superar desafios. O ambiente é simulado em uma matriz que representa o quarto completo (a "matriz principal"), e uma segunda matriz reduzida (a "matriz de visão") é atualizada dinamicamente para refletir o campo de visão do jogador. Assim, o jogador "navega" pela cena ao interagir e resolver puzzles que impactam o ambiente.

## Matrizes e Visualização:

## 1. Matriz Principal (Ambiente Completo):

Esta matriz representa o ambiente total do quarto em um grid 3D, onde cada célula ou posição indica um objeto, estrutura, ou espaço vazio. Objetos interativos como portas, alavancas, e outros mecanismos estão representados nesta matriz.

Quando o jogador interage com um elemento, o estado da matriz principal é atualizado, alterando o ambiente global (ex.: abrir uma porta, mudar a posição de uma alavanca).

## 2. Matriz de Visão do Jogador (Campo de Visão):

A matriz de visão é uma versão reduzida e dinâmica da matriz principal, atualizada com base na posição e direção do jogador.

Apenas uma seção da matriz principal é mostrada ao jogador através desta matriz de visão, simulando o campo de visão e o ângulo de observação.

A atualização da matriz de visão depende dos inputs do jogador (movimento, rotação de cabeça etc.), para que a visualização corresponda ao que está à frente e ao redor.

## 3. HUD (Interface de Desafios e Indicadores):

Os elementos de interface de usuário (HUD), como as barras de quick time event (QTE) e indicadores, não fazem parte das matrizes, sendo componentes fixos e visíveis na tela.

Isso garante que o jogador tenha feedback visual constante dos desafios e indicadores, independentemente do ambiente ao redor.

## Interatividade e Puzzles:

## 1. Detecção de Objetos no Campo de Visão:

Um sistema de detecção verifica se um objeto interativo (ex.: uma alavanca) está no campo de visão, permitindo que o jogador o selecione.
Quando o objeto está visível na matriz de visão, uma barra verde aparece, sinalizando a possibilidade de interação.
Ao interagir com um objeto, o jogo processa o evento (como puxar uma alavanca ou abrir uma porta) e atualiza a matriz principal, alterando o ambiente e desbloqueando novas áreas ou desafios.

## 2. Atualização do Ambiente e Novas Interações:

Interagir com certos elementos pode desbloquear outras partes do ambiente, alterando a matriz principal e possibilitando novos caminhos, enigmas e interações.
Com cada ação, a matriz principal é atualizada para refletir o novo estado do ambiente, permitindo que a narrativa e a progressão do jogo avancem.

## Quick Time Events (QTEs):

## 1. Mecânica de Reflexos:
QTEs aparecem visualmente na tela como uma barra que indica o tempo em que o jogador precisa apertar um botão específico.
O QTE pode ser projetado para medir precisão (pressionar no momento exato) ou velocidade (pressionar o botão repetidamente ou em um curto período).
## 2. Feedback Visual e HUD:
As barras de QTE são exibidas na parte inferior da tela e estão fora das matrizes de visão e ambiente, proporcionando um feedback imediato e claro para o jogador sem interferir na exploração.
Uma animação ou indicador adicional pode fornecer feedback imediato de sucesso ou falha, promovendo a sensação de urgência e resposta rápida.

## Jogabilidade
Controles Básicos:
- A: Olha para a esquerda.
- D: Olha para a direita.

## Barra de Progresso para Desbloqueio
- No jogo, existe uma barra de progresso dinâmica que é ativada em determinada situações, após interagir com a animação de puxar a corrente para prosseguir é necessário clicar a tecla espaço. Essa barra não está diretamente ligada à barra verde de interação, mas funciona como uma mecânica de Quick Time Event (QTE), onde o jogador deve pressionar a tecla Espaço repetidamente para preenchê-la e concluir a ação.
- Funcionamento da Barra de Progresso
Início do Desafio:

Quando a barra aparece na tela, ela começa na cor vermelho, indicando o estado inicial de progresso.
Progresso Visual:

Conforme o jogador pressiona Espaço, a barra progride e muda de cor:
Vermelho: Inicial, fácil.
Amarelo: Progresso médio.
Verde: Próximo da conclusão.
A barra precisa atingir o estado verde completo para desbloquear o objetivo
