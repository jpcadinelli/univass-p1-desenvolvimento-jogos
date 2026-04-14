# Jogo de Plataforma

## 1. Introdução

Este projeto foi desenvolvido como parte das atividades da disciplina de Laboratório de Desenvolvimento de Jogos Digitais, com o objetivo de aplicar, na prática, os conceitos estudados ao longo das aulas sobre jogos do tipo plataforma. A proposta consistiu na criação de um protótipo jogável que reunisse as principais mecânicas apresentadas no material da disciplina, contemplando tanto aspectos de jogabilidade quanto de organização estrutural do game.

Como requisito da atividade, o jogo deveria apresentar uma tela de menu inicial com as opções **Jogar**, **História**, **Controles**, **Autores** e **Finalizar**, permitindo ao jogador navegar entre diferentes telas informativas antes de iniciar a experiência. Além disso, o protótipo deveria conter pelo menos **três fases**, sistema de **coleta de itens**, sistema de **dano e morte do personagem**, progressão condicionada ao cumprimento de objetivos e telas de **vitória** e **derrota**, oferecendo ao jogador a escolha de reiniciar a partida ou retornar ao menu principal.

Outro ponto importante do desenvolvimento foi a preocupação em utilizar um personagem diferente daquele apresentado no material de apoio da disciplina, bem como selecionar assets visuais coerentes com a temática e com a narrativa proposta para o jogo. Dessa forma, o projeto buscou não apenas atender aos requisitos técnicos da atividade, mas também construir uma experiência mais consistente em termos de identidade visual, ambientação e progressão.

Este repositório reúne os arquivos do jogo, sua documentação e informações relevantes sobre a estrutura do projeto, com o propósito de registrar o processo de desenvolvimento e apresentar o resultado final da atividade.

## 2. Hitória

Em um mundo que antes vivia em equilíbrio com a natureza, a poluição começou a se espalhar por florestas, rios e montanhas, consumindo a energia vital que mantinha todas as formas de vida em harmonia. Com o avanço dessa destruição, o **Cristal da Vida**, uma relíquia sagrada responsável por sustentar o equilíbrio natural do mundo, foi rompido, espalhando seus fragmentos por diferentes regiões agora corrompidas.

Sem a proteção do cristal, a natureza perdeu sua estabilidade. Criaturas que antes coexistiam em paz com o ambiente passaram a agir de forma hostil, transformadas pela contaminação e pela ausência da energia sagrada. Além disso, os caminhos naturais foram afetados pela degradação, fazendo surgir perigos e obstáculos ao longo da jornada, como áreas instáveis, espinhos e passagens bloqueadas.

Diante desse cenário, o protagonista parte em uma missão para recuperar os fragmentos do Cristal da Vida e devolvê-los à natureza. Durante a aventura, ele deve atravessar regiões tomadas pela poluição e reativar antigos mecanismos esquecidos, como alavancas que liberam plataformas e restabelecem a passagem por áreas bloqueadas.

Nesta jornada, o herói encontra dois tipos de itens fundamentais: as maçãs, que simbolizam a força regeneradora da própria natureza e ajudam a restaurar sua vitalidade, e as moedas, que representam tesouros perdidos nas áreas corrompidas. Diferente da energia vital, as moedas servem como um registro das conquistas do herói, sendo acumuladas para compor sua pontuação final ao concluir o objetivo de salvar o mundo.

O momento de maior importância ocorre ao final de cada região. Antes de atravessar a porta que leva ao próximo desafio, o herói deve coletar uma porção concentrada da energia do Cristal. Esse ato simboliza a purificação daquela área e garante ao protagonista a força necessária para avançar. Assim, cada fase superada representa um passo crucial na reconstrução do Cristal da Vida e na esperança de devolver ao mundo a pureza que a poluição quase destruiu por completo.

## 3. Mecânicas Principais

O jogo foi desenvolvido no gênero plataforma e incorpora mecânicas centrais voltadas à movimentação, sobrevivência, progressão por fases e sistema de pontuação. A proposta busca aplicar os conceitos trabalhados ao longo da disciplina, estruturando a experiência de forma progressiva entre uma fase inicial de tutorial e três fases principais.

### Movimentação do jogador
O personagem pode se deslocar horizontalmente para a esquerda e para a direita, além de realizar saltos verticais. Como diferencial de mobilidade, o jogo também conta com a mecânica de **salto duplo**, permitindo ao jogador executar um segundo salto ainda no ar, o que amplia as possibilidades de exploração e desvio de obstáculos.

### Sistema de vida
O jogador inicia a partida com **3 pontos de vida**, podendo alcançar o máximo de **5 pontos** ao longo da fase. Para recuperar vida, é possível coletar **maçãs**, sendo que cada maçã restaura **1 ponto de vida**. Caso a vida do personagem chegue a zero, é exibida a condição de **game over**, e o jogador é retornado ao menu principal.

### Sistema de coleta
O jogo possui dois tipos principais de itens coletáveis:

- **Maçãs**: utilizadas para recuperação de vida;
- **Moedas**: utilizadas exclusivamente para compor a pontuação do jogador.

As moedas coletadas são contabilizadas ao longo das fases e contribuem para o resultado final obtido pelo jogador.

### Obstáculos e dano
Durante as fases, o jogador deve lidar com diferentes ameaças. Os **espinhos** causam perda de vida e lançam o personagem para cima ao serem tocados. Além disso, há **inimigos** que atacam arremessando suas armas. O jogador perde vida tanto ao ser atingido pela arma quanto ao encostar lateralmente nos inimigos.

Como mecânica de combate, o inimigo pode ser derrotado caso o jogador o atinja **por cima**, pulando sobre ele.

### Interação com o cenário
Algumas partes do mapa exigem interação para liberar a progressão. Entre essas interações, destaca-se a **alavanca**, que precisa ser acionada pelo jogador ao pular sobre ela. Após ser ativada, uma **plataforma de passagem** é liberada, permitindo a continuidade da fase.

### Progressão e avanço de fases
O jogo conta com uma **fase inicial de tutorial**, responsável por introduzir o jogador às mecânicas básicas, seguida por **três fases principais**. O avanço entre as fases ocorre quando o jogador alcança a **porta localizada ao final do mapa**, representando a conclusão do objetivo daquela etapa.

Caso o jogador caia para fora do mapa, ele não perde imediatamente a partida, mas retorna ao **início da fase atual**, funcionando como uma penalização de reposicionamento.

### Checkpoints
O sistema de checkpoint está definido de forma simples: o **início de cada fase** funciona como ponto de retorno para o jogador em situações de queda no mapa ou reinício daquela etapa.

### Sistema de pontuação
O jogo possui um sistema de pontuação calculado com base no desempenho do jogador. Ao final das fases, são considerados os seguintes elementos:

- **tempo gasto em cada fase**;
- **quantidade de moedas coletadas**;
- **quantidade de vida restante**.

O tempo é contabilizado separadamente em cada fase e incorporado ao cálculo de pontuação ao término da etapa, compondo o desempenho final do jogador ao longo da experiência.

## 4. Controles

Os controles do jogo foram definidos de forma simples e intuitiva, permitindo ao jogador movimentar o personagem com diferentes teclas equivalentes no teclado. Essa abordagem busca facilitar a jogabilidade e tornar a experiência mais acessível.

### Movimentação horizontal
- **A** ou **Seta Esquerda**: move o personagem para a esquerda;
- **D** ou **Seta Direita**: move o personagem para a direita.

### Salto
- **W**, **Espaço** ou **Seta Cima**: realiza o salto do personagem.

### Salto duplo
O jogo também conta com a mecânica de **salto duplo**, permitindo ao jogador executar um segundo salto enquanto ainda estiver no ar. Esse recurso é fundamental para alcançar plataformas mais altas, desviar de obstáculos e superar determinados trechos das fases.

### Interações durante a fase
Algumas interações com o cenário ocorrem por meio do próprio movimento do personagem. Um exemplo disso é a **alavanca**, que deve ser acionada ao ser atingida por cima, fazendo com que o jogador precise saltar sobre ela para liberar a passagem na fase.

## 5. Sistema de Pontuação

O sistema de pontuação do jogo foi planejado para avaliar o desempenho do jogador de forma equilibrada, considerando três aspectos principais da partida: **coleta de moedas**, **vida restante** e **tempo de conclusão da fase**. Dessa forma, a pontuação final não depende apenas da velocidade, mas também da capacidade de exploração e sobrevivência ao longo do jogo.

### Critérios de pontuação

Ao final de cada fase, a pontuação do jogador é calculada com base nos seguintes elementos:

- **Moedas coletadas**: recompensam a exploração do cenário;
- **Vida restante**: valoriza a capacidade de superar os desafios com menor dano;
- **Tempo da fase**: concede bônus de desempenho conforme a rapidez na conclusão.

### Proposta de cálculo

Para manter o sistema balanceado, a pontuação pode ser calculada da seguinte forma:

**Pontuação da fase = (moedas coletadas × 10) + (vidas restantes × 50) + bônus de tempo**

#### 1. Pontuação por moedas
Cada moeda coletada concede:

- **10 pontos por moeda**

Essa escolha valoriza a coleta sem permitir que ela, sozinha, domine completamente o resultado final.

#### 2. Pontuação por vida restante
Cada ponto de vida restante ao final da fase concede:

- **50 pontos por vida restante**

Como o jogador pode terminar a fase com até 5 pontos de vida, esse critério recompensa quem joga com maior precisão e evita danos ao longo do percurso.

#### 3. Bônus por tempo
O tempo não reduz a pontuação do jogador. Em vez disso, ele gera um bônus de desempenho com base na rapidez de conclusão da fase.

Sugestão de faixas:

- **Até 1 minuto**: 100 pontos de bônus
- **Até 2 minutos**: 70 pontos de bônus
- **Até 3 minutos**: 40 pontos de bônus
- **Acima de 3 minutos**: 20 pontos de bônus

Esse modelo permite premiar jogadores mais rápidos sem prejudicar excessivamente aqueles que preferem avançar com mais cautela.

### Exemplo de cálculo
Se um jogador terminar uma fase com:

- **12 moedas coletadas**
- **4 pontos de vida restantes**
- **tempo de 1 minuto e 45 segundos**

A pontuação será:

- Moedas: 12 × 10 = 120 pontos
- Vida restante: 4 × 50 = 200 pontos
- Bônus de tempo: 70 pontos

**Pontuação total da fase = 390 pontos**

### Pontuação final
A pontuação final do jogo será obtida pela **soma da pontuação das três fases principais**, permitindo uma avaliação geral do desempenho do jogador ao longo da experiência.

### Justificativa do balanceamento
A distribuição proposta busca equilíbrio entre diferentes estilos de jogo:

- jogadores exploradores são recompensados pelas moedas;
- jogadores mais cuidadosos são recompensados pela vida restante;
- jogadores mais rápidos recebem bônus por eficiência.

Com isso, o sistema evita privilegiar apenas um único fator e incentiva uma experiência mais completa dentro da proposta do jogo.

## 6. Ambientação das Fases

As fases do jogo foram planejadas para representar a progressão da degradação causada pela poluição no mundo do Cristal da Vida.

- **Fase 1 – Floresta em Desequilíbrio:** apresenta uma região natural ainda parcialmente preservada, mas já marcada por sinais de contaminação, como vegetação enfraquecida, céu acinzentado e pequenas áreas degradadas.

- **Fase 2 – Ruínas da Natureza Corrompida:** mostra uma área mais afetada pela poluição, com árvores secas, rios contaminados, estruturas antigas degradadas e atmosfera mais sombria, reforçando o aumento da dificuldade e do perigo.

- **Fase 3 – Núcleo da Poluição:** representa o estágio mais crítico da destruição ambiental, com cenário devastado, céu escuro, solo corrompido e poucos vestígios de vida, simbolizando o confronto final contra o colapso da natureza.

## 7. Autores

| Nome | Matrícula | GitHub |
|---|---|---|
| [João Pedro Coelho Cadinelli dos Santos](https://github.com/jpcadinelli) | 202313598 | [@jpcadinelli](https://github.com/jpcadinelli) |
| [Julio Fernando Martins Leite](https://github.com/devjuliomartins) | 202310535 | [@devjuliomartins](https://github.com/devjuliomartins) |
| [Pedro Leal Primo Teixeira Coelho](https://github.com/pedro-coelho1604) | 202310631 | [@pedro-coelho1604](https://github.com/pedro-coelho1604) |
| [Heloisa Coelho Cabral](https://github.com/devheloisacabral) | 202311029 | [@devheloisacabral](https://github.com/devheloisacabral) |
