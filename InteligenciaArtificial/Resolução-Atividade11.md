# Atividade sobre agentes inteligentes

Aula 19/10/2026 | Professora Kadidja Valéria | Inteligência artificial

**Disciplina:** Inteligência Artificial, Linguagens Formais e Autômatos

**Estudante:** Júlia Sernagiotto Barbosa | **Turma:** Engenharia de Software N1


## Exercício 2.3
Para cada afirmação, indique V ou F, justifique e forneça exemplo ou contraexemplo. Explicite as hipóteses utilizadas.

### a. Um agente que detecta apenas informações parciais sobre o estado não pode ser perfeitamente racional.

- Julgamento: F
- Justificativa: Um agente pode ser pode ser perfeitamente racional sem observar todo o estado do ambiente, desde que tome a ação que maximiza o desempenho esperado com base nas informações disponíveis.
- Exemplo ou contraexemplo: Um ambiente em que há apenas uma ação possível. Mesmo sem observar nada do ambiente, o agente sempre executa essa única ação e obtém o melhor desempenho possível.

### b. Existem ambientes de tarefa nos quais nenhum agente reativo puro pode comportar-se racionalmente.

- Julgamento: V
- Justificativa: Em ambientes parcialmente observáveis, duas situações distintas podem produzir exatamente a mesma percepção atual, exigindo ações diferentes. Nesse caso, para agir racionalmente o agente precisa de memória do histórico ou de um modelo interno do estado.
- Exemplo ou contraexemplo: Mundo do aspirador parcialmente observável.

### c. Existe um ambiente de tarefa em que todo agente é racional.

- Julgamento: V
- Justificativa: Basta construir um ambiente em que qualquer ação produza exatamente o mesmo resultado na medida de desempenho.
- Exemplo ou contraexemplo: Um ambiente com: apenas um estado, qualquer ação gera recompensa 0, o episódio termina imediatamente.

### d. A entrada para o programa de agente é a mesma que a entrada para a função de agente.

- Julgamento: F
- Justificativa: o programa de agente normalmente recebe apenas a percepção atual e utiliza memória interna para representar o histórico.
- Exemplo ou contraexemplo: Um agente baseado em modelo.

### e. Toda função de agente é implementável por uma combinação de programa/máquina.

- Julgamento: F
- Justificativa: O conjunto de funções de agente é muito maior que o conjunto de programas computáveis.
- Exemplo ou contraexemplo: Uma função de agente cuja decisão dependa da solução geral do Problema da Parada.

### f. Suponha que um agente selecione sua ação uniformemente ao acaso do conjunto de ações possíveis. Existe um ambiente de tarefa determinista em que esse agente é racional.

- Julgamento: V
- Justificativa: Se todas as ações tiverem exatamente a mesma consequência, então escolher aleatoriamente é tão bom quanto qualquer outra estratégia.
- Exemplo ou contraexemplo: Estado único: ações {A, B, C}, qualquer ação gera recompensa 10.

### g. É possível para um dado agente ser perfeitamente racional em dois ambientes de tarefa distintos.

- Julgamento: V
- Justificativa: Nada impede que o mesmo comportamento seja ótimo em mais de um ambiente.
- Exemplo ou contraexemplo: Um agente que sempre executa a ação "Parar". Um ambiente onde a única ação possível é Parar e outro ambiente onde qualquer ação produz exatamente o mesmo resultado.

### h. Todo agente é racional em um ambiente não observável.

- Julgamento: F
- Justificativa: Mesmo sem percepções, pode existir uma ação melhor que as demais. Agentes que não escolham essa ação não serão racionais.
- Exemplo ou contraexemplo: Um agente que não escolhe a melhor ação no ambiente.

### i. Um agente jogador de pôquer perfeitamente racional nunca perde.

- Julgamento: F
- Justificativa: Um agente perfeitamente racional escolhe a ação que maximiza o valor esperado, mas ainda pode perder uma mão ou até uma sequência de mãos devido ao acaso.
- Exemplo ou contraexemplo: Um agente racional recebe uma mão excelente e aposta corretamente, mas o adversário completa uma combinação improvável no river e vence.

## Exercício 2.4
Para cada caso, delimite o agente, preencha o PEAS e justifique todas as classificações. Considere Titã como cenário hipotético do exercício.

### Caso 1 — Jogar futebol.

- Agente analisado: Jogador autômato de futebol
- Objetivo e hipóteses: Vencer a partida marcando mais gols que o adversário. Assume-se uma partida regulamentada, com equipes adversárias e companheiros de equipe.
- P — Medida de desempenho: Vitórias, saldo de gols, participação em jogadas, poucas faltas, cumprimento das regras.
- E — Ambiente: Campo de futebol, bola, colegas de equipe, adversários, árbitro e condições do jogo.
- A — Atuadores: Pernas, braços, deslocamento, chute, passe, cabeceio.
- S — Sensores:Visão, audição, sensores de posição, velocidade e proximidade.

| Propriedade | Classificação | Justificativa |
|---|---|---|
| Observabilidade | Parcialmente observável | O agente não conhece perfeitamente intenções dos adversários e nem todos os detalhes do campo em todos os instantes. |
| Número de agentes | Multiagente (cooperação e competição) | Coopera com colegas e compete contra a equipe adversária. |
| Previsibilidade | Estocástico | As ações dos demais jogadores tornam o resultado incerto. |
| Dependência entre decisões | Sequencial | Cada ação influencia estados e decisões futuras. |
| Mudança durante a decisão | Dinâmico | O jogo continua mudando enquanto o agente decide.|
| Natureza dos elementos | Contínuo | Tempo, posições, velocidades e movimentos são contínuos.|
| Conhecimento do funcionamento | Conhecido | As regras do futebol são conhecidas, embora os adversários não sejam totalmente previsíveis. |

### Caso 2 — Explorar os oceanos subterrâneos de Titã.

- Agente analisado: Robô explorador submarino autônomo.
- Objetivo e hipóteses:Mapear o oceano subterrâneo, coletar dados científicos e retornar informações à base. Assume-se um ambiente pouco conhecido.
- P — Medida de desempenho: Área explorada, qualidade dos dados coletados, sobrevivência da missão, economia de energia.
- E — Ambiente: Oceano subterrâneo de Titã, obstáculos, correntes, relevo e condições físicas desconhecidas.
- A — Atuadores: Hélices, propulsores, braços robóticos, instrumentos de coleta.
- S — Sensores: Sonar, câmeras, sensores químicos, profundidade, temperatura e navegação.

| Propriedade | Classificação | Justificativa |
|---|---|---|
| Observabilidade | Parcialmente observável | Nem todo o ambiente pode ser percebido instantaneamente. |
| Número de agentes | Agente único | Considera-se apenas um explorador autônomo. |
| Previsibilidade | Estocástico | Fenômenos naturais e desconhecidos podem alterar resultados. |
| Dependência entre decisões | Sequencial | O trajeto e as coletas futuras dependem das decisões anteriores. |
| Mudança durante a decisão | Dinâmico |Correntes, condições físicas e descobertas podem mudar o ambiente.|
| Natureza dos elementos | Contínuo | Espaço, movimento e medições variam continuamente. |
| Conhecimento do funcionamento | Desconhecido | O agente não possui modelo completo do ambiente de Titã. |

### Caso 3 — Comprar livros usados de IA na Internet.

- Agente analisado: Agente comprador automático.
- Objetivo e hipóteses: Comprar livros usados de IA pelo melhor custo-benefício.
- P — Medida de desempenho:Menor preço, qualidade do livro, confiabilidade do vendedor e prazo de entrega.
- E — Ambiente: Sites de venda, vendedores, compradores concorrentes e sistemas de pagamento.
- A — Atuadores: Pesquisar, enviar consultas, realizar lances ou compras.
- S — Sensores: Informações das páginas, avaliações, preços e disponibilidade.

| Propriedade | Classificação | Justificativa |
|---|---|---|
| Observabilidade |Parcialmente observável | Nem sempre é possível verificar o real estado do livro ou a intenção do vendedor. |
| Número de agentes | Multiagente (competição) | Há vendedores e compradores influenciando o mercado. |
| Previsibilidade | Estocástico | Preços e disponibilidade podem mudar inesperadamente. |
| Dependência entre decisões |Sequencial | Pesquisas e compras anteriores influenciam decisões futuras.|
| Mudança durante a decisão | Dinâmico| Novos anúncios podem surgir e livros podem ser vendidos.|
| Natureza dos elementos | Combinação | Existem elementos discretos (anúncios) e contínuos (preços e tempo). |
| Conhecimento do funcionamento | Conhecido | O agente conhece as regras do site, mas não todos os fatores do mercado. |

### Caso 4 — Jogar uma partida de tênis.

- Agente analisado: Jogador de tênis.
- Objetivo e hipóteses: Vencer a partida conquistando mais pontos, games e sets.
- P — Medida de desempenho: Pontuação final e vitória na partida.
- E — Ambiente: Quadra, bola, adversário, vento e arbitragem.
- A — Atuadores: Movimentação, saque e golpes com a raquete.
- S — Sensores: Visão, audição e percepção corporal.

| Propriedade | Classificação | Justificativa |
|---|---|---|
| Observabilidade |Parcialmente observável| Não é possível observar diretamente a estratégia e intenção do adversário. |
| Número de agentes | Multiagente (competição) | Há um adversário com objetivos opostos.|
| Previsibilidade | Estocástico| O comportamento do adversário gera incerteza.|
| Dependência entre decisões |Sequencial| Cada jogada altera a situação seguinte. |
| Mudança durante a decisão | Dinâmico | A bola e o adversário continuam em movimento. |
| Natureza dos elementos | Contínuo | Movimento, tempo e posição variam continuamente. |
| Conhecimento do funcionamento | Conhecido | Regras e dinâmica física são conhecidas. |

### Caso 5 — Praticar tênis contra uma parede.

- Agente analisado: Jogador treinando sozinho.
- Objetivo e hipóteses: Manter trocas de bola e aperfeiçoar a técnica.
- P — Medida de desempenho: Quantidade de rebatidas corretas, precisão e regularidade.
- E — Ambiente: Quadra, parede, bola e condições físicas do local.
- A — Atuadores: Movimentação e golpes com a raquete.
- S — Sensores: Visão, audição e percepção corporal.

| Propriedade | Classificação | Justificativa |
|---|---|---|
| Observabilidade | Completamente observável | Os elementos relevantes são visíveis e previsíveis. |
| Número de agentes | Agente único | Não existe adversário tomando decisões. |
| Previsibilidade | Determinístico | A resposta da parede depende principalmente das leis físicas. |
| Dependência entre decisões | Sequencial | Cada golpe afeta o próximo retorno da bola. |
| Mudança durante a decisão | Dinâmico | A bola continua em movimento durante a tomada de decisão. |
| Natureza dos elementos | Contínuo | Posição, velocidade e tempo são contínuos. |
| Conhecimento do funcionamento | Conhecido | O comportamento da parede e as regras físicas são conhecidas. |

### Caso 6 — Realizar um salto de altura.

- Agente analisado: Atleta executando o salto.
- Objetivo e hipóteses: Ultrapassar o sarrafo na maior altura possível sem derrubá-lo.
- P — Medida de desempenho: Altura alcançada e sucesso do salto.
- E — Ambiente: Pista, sarrafo, colchão e condições climáticas.
- A — Atuadores: Músculos responsáveis pela corrida, impulso e salto.
- S — Sensores: Visão, equilíbrio e propriocepção.

| Propriedade | Classificação | Justificativa |
|---|---|---|
| Observabilidade | Completamente observável | O atleta consegue perceber os elementos relevantes da prova. |
| Número de agentes | Agente único | O desempenho depende apenas do atleta durante a execução.|
| Previsibilidade | Determinístico | O resultado decorre principalmente das ações do atleta e das leis físicas. |
| Dependência entre decisões | Sequencial | A corrida de aproximação influencia a impulsão e o salto. |
| Mudança durante a decisão | Dinâmico | O corpo está em movimento durante a execução. |
| Natureza dos elementos | Contínuo | Tempo, velocidade e posição são contínuos. |
| Conhecimento do funcionamento | Conhecido | O comportamento físico do ambiente é conhecido. |

### Caso 7 — Participar de um leilão de um item, realizando lances.

- Agente analisado: Agente participante do leilão.
- Objetivo e hipóteses: Adquirir o item desejado pelo menor preço possível.
- P — Medida de desempenho: Obter o item respeitando limite de gasto e maximizando utilidade.
- E — Ambiente: Plataforma de leilão, item, leiloeiro e demais participantes.
- A — Atuadores: Fazer lances, desistir, definir limites de oferta.
- S — Sensores: Histórico de lances, preço atual e tempo restante.

| Propriedade | Classificação | Justificativa |
|---|---|---|
| Observabilidade | Parcialmente observável | Não se conhece o valor máximo que os concorrentes estão dispostos a pagar. |
| Número de agentes | Multiagente (competição) | Os participantes competem pelo mesmo item. |
| Previsibilidade | Estocástico | As decisões dos concorrentes são imprevisíveis |
| Dependência entre decisões | Sequencial | Cada lance influencia os próximos. |
| Mudança durante a decisão | Dinâmico | Os lances podem mudar enquanto o agente avalia sua ação. |
| Natureza dos elementos | Combinação | Existem ações discretas (lances) e aspectos contínuos (tempo e valores monetários). |
| Conhecimento do funcionamento | Conhecido | As regras do leilão são conhecidas, embora as estratégias dos rivais não sejam. |

### Opções para classificação
- **Observabilidade:** Completamente observável, parcialmente observável ou não observável.
- **Número de agentes:** Agente único ou multiagente; indique cooperação ou competição quando pertinente.
- **Previsibilidade:** Determinístico ou estocástico; considere a influência estratégica de outros agentes.
- **Dependência entre decisões:** Episódico ou sequencial.
- **Mudança durante a decisão:** Estático, dinâmico ou semidinâmico.
- **Natureza dos elementos:** Discretos, contínuos ou combinação; considere estados, tempo, percepções e ações.
- **Conhecimento do funcionamento:** Conhecido ou desconhecido para o agente.

### Comparação final
1. O que muda entre jogar tênis contra outra pessoa e praticar contra uma parede?
2. Por que comprar livros usados pode exigir decisões com informações incompletas?
3. Como outros agentes influenciam futebol e leilões?

Respostas: 
1. Contra outra pessoa, o ambiente é multiagente, competitivo e estocástico, porque o adversário toma decisões estratégicas. Contra uma parede, o ambiente torna-se agente único e aproximadamente determinístico, já que a parede não toma decisões nem possui estratégia.

2. Porque nem todas as informações relevantes estão disponíveis. O comprador pode não conhecer exatamente o estado físico do livro, a honestidade do vendedor, atrasos de entrega ou futuras alterações de preço. Assim, o ambiente é parcialmente observável.

3. No futebol, colegas ajudam e adversários tentam impedir o objetivo do agente, tornando o ambiente competitivo e cooperativo ao mesmo tempo. No leilão, outros participantes elevam preços e afetam a estratégia de lance. Em ambos os casos, as ações de terceiros tornam o ambiente mais imprevisível e estocástico.

## Exercício 2.5
Defina cada termo com suas palavras em duas a quatro linhas e apresente um exemplo.

### Agente

- Definição: Um agente é uma entidade que percebe o ambiente por meio de sensores e age sobre ele usando atuadores. Seu objetivo é tomar decisões e executar ações de acordo com as informações que recebe.
- Exemplo: Um robô aspirador que detecta obstáculos e escolhe caminhos para limpar uma casa.

### Função de agente

- Definição: A função de agente descreve qual ação deve ser tomada para cada sequência possível de percepções. Ela representa o comportamento ideal do agente.

- Exemplo: Em um termostato, a função pode determinar que, ao perceber uma temperatura abaixo de 20°C, a ação será ligar o aquecedor.

### Programa de agente

- Definição: É a implementação prática da função de agente em software. O programa recebe percepções como entrada e produz ações como saída.
- Exemplo: O código que controla um carro autônomo e decide acelerar, frear ou virar com base nos dados dos sensores.

### Racionalidade

- Definição: Racionalidade é a capacidade de escolher a ação que maximiza o desempenho esperado, considerando as informações disponíveis e os objetivos do agente.

- Exemplo: Um GPS que escolhe a rota mais rápida com base no trânsito atual.

### Autonomia

- Definição: Autonomia é a capacidade de um agente agir com pouca ou nenhuma intervenção humana, aprendendo e tomando decisões a partir de sua própria experiência.

- Exemplo: Um drone que navega sozinho e ajusta sua rota quando encontra obstáculos.

### Agente reativo

- Definição: Um agente reativo toma decisões apenas com base na percepção atual, sem considerar um histórico ou modelo interno do ambiente.
- Exemplo: Uma porta automática que abre sempre que detecta alguém à sua frente.

### Agente baseado em modelo

- Definição: Esse agente mantém uma representação interna do ambiente para lidar com informações incompletas e prever mudanças de estado.
- Exemplo: Um aspirador robótico que cria um mapa da casa para lembrar áreas já limpas.

### Agente baseado em objetivos

- Definição: Além de conhecer o ambiente, esse agente considera metas específicas e escolhe ações que o aproximem de seus objetivos.
- Exemplo: Um aplicativo de navegação que busca o caminho até um destino definido pelo usuário.

### Agente baseado em utilidade

- Definição: Esse agente avalia diferentes alternativas usando uma medida de utilidade e escolhe a que produz o melhor resultado esperado.
- Exemplo: Um sistema de investimentos que seleciona a carteira com melhor equilíbrio entre risco e retorno.

### Agente com aprendizagem

- Definição: É um agente capaz de melhorar seu desempenho ao longo do tempo, utilizando experiências e dados coletados durante a interação com o ambiente.
- Exemplo: Um filtro de spam que aprende a identificar mensagens indesejadas com base nas marcações feitas pelos usuários.

## Síntese com autômatos
Escolha um caso do item 2.4. Apresente três estados internos, três percepções, três ações e duas regras no formato estado atual + percepção → próximo estado e ação. Explique como estados internos representam informação passada e cite uma limitação da simplificação.

Resposta:
