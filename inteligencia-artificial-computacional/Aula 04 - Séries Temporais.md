Conceitos de Análise Estocástica

Segundo a definição geral, processo estocástico é uma coleção de variáveis aleatórias que em geral, são utilizadas para estudar a evolução de de fenômenos (ou sistemas) que são observados ao longo do tempo.
Como exemplos de processos estocásticos, podemos considerar:

- X(t) representa o estado de uma máquina (ligad/desligada) no momento t;
- X(t) representa o número de clientes numa loja no instante t;
- X(t) representa o número de máquinas avariadas no fim do dia t;
- X(t) representa a cotação de uma ação no fim do dia t;
- X(t) representa o nível de estoque de um determinado artigo no fim do dia t;
- X(t) representa a condição de funcionamento de um component no instante t; 

Como se pode constatar pelos exemplos apresentados, há casos em que o tempo é considerado de forma discreta (... no fim do dia t) e outros em que é tomado de modo contínuo (... no momento t). A variável tempo é, por definição contínua, mas pode ser considerada discreta se os fenômenos forem observados a intervalos regulares.
Em casos de tempo discreto, em oposição ao tempo contínuo, o processo estocástico é uma sequência de variáveis aleatórias, como por exemplo uma cadeia de Markov. As variáveis correspondentes aos diversos tempos podem ser completamente diferentes, o único requisito é que esses valores diferentes estejam todos no mesmo espaço, isto é, no contradomínio da função.
A cadeia de Markov de forma simples é a relação de probabilidade dada uma sequência de estados finitos, assim dado determinado estado t temos a probabilidade p para a mudança  de estado t', concluindo que para predição do próximo estado só precisa ser conhecido o estado atual.
P(Xn + 1 = x | Xn = x)

Classificação de processos Estocásticos

Processos estocásticos podem ser classificados de acordo com a cardinalidade dos seus conjuntos indexados, normalmente interpretados como tempo, e o espaço de estado. Então para classificar os processos estocásticos analisam-se:
- O espaço de estados
- A naturesza do conjunto T 
- As características estatísticas das variáveis aleatórias que definem o processo

Espaço de estado
Se X for um conjuntos de estados finito ou contável (X = { 0, 1, 2, ... n } ), o conjunto de inteiros não negativos. X(t) é um processo discretos, do exemplo referido os três primeiros são cadeias, enquantos que os restantes podem ser processos de estados contínuos.

A variável temporal
Se o conjunto T, que especifica os valores da variável t, for finito ou contável, X(t) é um processo em tempo discreto e a notação usada é ( X ( t, t = { 0, 1, 2, 3, ... n } )). No exemplo, os números 3, 4, e 5 são processos em tempo discreto uma vez que representam quantidades observadas no dia a dia, enquanto que os restantes são processos estocásticos em tempo contínuo por representarem fenômenos observados em qualquer momento do tempo.

Características estatísticas das variáveis aleatórias
Um processo estocástico diz-se estácionaário se o seu comportamento estocástico for independente do tempo, ou seja se a função distribuição (Função distribuição) das variáveis aleátorias que o definem não variar com o tempo. Por exemplo de fato para um processo de Markov é completamente irrelevante qualquer informação sobre estados passados ou sobre o tempo de permanência no estado presente.


Séries Temporáis - Exemplos

Uma série temporal se considera como realização de um processo estocástico (esporádico) e que estão ordenadas em intervalos regulares de tempo (cada dia, mês ano), ex:

![[Screen Shot 2021-09-11 at 23.04.29.png]]

A análise de séries temporais é um importante instrumento no entendimento de dados e na formulação de planos de ação e estratégia.

Por exemplo, podemos monitorar a latência de rede, e formular e medir a efetividade de planos de ação em casos de falhas.

![[Screen Shot 2021-09-11 at 23.13.48.png]]

Ou a quantidade de vacinas do covid 19 por mês
![[Screen Shot 2021-09-11 at 23.16.27.png]]

Modelos de séries temporais são muito utilizados para avaliar ocomportamento de uma variável ao longo do tempo. Um site eccommerce por exemplo em dia de black friday tende ter um número de acesso anorlmal, quais recursos deveriam ser escalado na infraestrutura para suportar o pico na quantidade de acesso no dia de promoção?

Na verdade, os modelos estatísticos para séries temporais utilizam o passado histórico da variável para projetar observações futuras. Dessa forma, se pode ter uma ideia, em média, de como a variável se comportará nos próximos períodos.

![[Screen Shot 2021-09-11 at 23.30.15.png]]

Por exemplo a alta correlação de acesso em meses e lag poderia ser esclarecedora na tomada de decisão dos recursos a serem escalados.

A tendência de uma série temporal é definida como um padrão de crescimento/descrecimento da variável em um certo período de tempo. Existem testes específicos para a identificação da tendência, como o Teste de Wald e o de Cox-Stuart. Entretanto, uma técnica muito utilizada é o ajuste de uma Regressão Linear Simples para a identificação da inclinação da reta de tendência. Vale lembrar que o ajuste da Regressão Linear, neste caso, pode levar a resultados enviesados e, para evitar este problema, estimadores robustos à autocorrelação podem ser utilizados.