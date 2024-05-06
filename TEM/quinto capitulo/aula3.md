# Análise de cluster continuação

## Método de partição das k-médias (método não hierárquico)

Notas:

- O número de clusters é definido à partida
- O resultado final é influenciado pelo número de clusters escolhido

ex 1:

- J:

Determinação dos clusters, usando o método de partição das k-médias, para k=2 clusters, tendo-se inicialmente os clusters (1,2,5) e (3,4)
- 1º passo: O processo é iniciado, por exemplo, com os dois clusters (1,2,5) e (3,4)
- 2º passo: vamos calcular as componentes de cada centróide, ou seja, as médias para cada variável com os indivíduos considerados em cada cluster, obtendo assim os centróides dos clusters. 

Para o cluster (1,2,5) tem-se:

média x1 = (8+10+3)/3 = 7,0

média x2 = (3+5+9)/3 = 5,7

média x3 = (10+7+2)/3 = 6,3

Para o cluster (3,4):

média x1 = (2+3)/2 = 2,5

média x2 = (5+4)/2 = 4,5

média x3 = (8+5)/2 = 6,5

têm-se os centróides:

| Clusters | média x1 | média x2 | média x3|
| --- | --- | --- | --- |
| (1,2,5) | 7,0 | 5,7 | 6,3 |
| (3,4) | 2,5 | 4,5 | 6,5 |

As distâncias dos objetos ou indivíduos aos centróides vão ser calculadas usando o quadrado da distância euclidiana, dada por: 

dij^2 = (xi1 - xj1)^2 + (xi2 - xj2)^2 + (xi3 - xj3)^2 - comparar os valores asssumidos pelo indivíduo i, em cada variável, com os valores obtidos no respectivo centróide.

Para o objeto 1, tem-se:

d(1;(1,2,5))^2 = (8-7)^2 + (3-5,7)^2 + (10-6,3)^2 = 22

Para o objeto 2, tem-se:

d(2;(1,2,5))^2 = (10-7)^2 + (5-5,7)^2 + (7-6,3)^2 = 10,0

Para o objeto 5, tem-se:

d(5;(1,2,5))^2 = (3-7)^2 + (9-5,7)^2 + (2-6,3)^2 = 45,4

Para o objeto 3, tem-se:

d(3;(1,2,5))^2 = (2-7)^2 + (5-5,7)^2 + (8-6,3)^2 = 28,4

Para o objeto 4, tem-se:

d(4;(1,2,5))^2 = (3-7)^2 + (4-5,7)^2 + (5-6,3)^2 = 20,6

d(1;(3,4))^2 = (8-2,5)^2 + (3-4,5)^2 + (10-6,5)^2 = 44,8
d(2;(3,4))^2 = (10-2,5)^2 + (5-4,5)^2 + (7-6,5)^2 = 56,8
d(3;(3,4))^2 = (2-2,5)^2 + (5-4,5)^2 + (8-6,5)^2 = 40,8
d(4;(3,4))^2 = (3-2,5)^2 + (4-4,5)^2 + (5-6,5)^2 = 2,8
d(5;(3,4))^2 = (3-2,5)^2 + (9-4,5)^2 + (2-6,5)^2 = 2,8

Pode verificar-se que o indivíduo 5 parece estar mais próximo do centróide do grupo (3,4) do que do grupo (1,2,5), no qual está colocado.

3º Passo: Vamos deslocar os objetos de forma a que cada umu deles fique colocado no grupo da partição que tem o centróide mais próximo.
Os resultados obtidos segem que o que o indivíduo 5 deve sair do cluster (1,2,5) e se junte ao cluster (3,4), obtendo-se os novos clusters: (1,2), (3,4,5)

4º passo: vamos calcular as componentes dos centróides dos novos clusters:

para o cluster (1,2):

média x1 = (8+10)/2 = 9,0

média x2 = (3+5)/2 = 4,0

média x3 = (10+7)/2 = 8,5

para o cluster (3,4,5):

média x1 = (2+3+3)/3 = 2,7

média x2 = (5+4+9)/3 = 6,0

média x3 = (8+5+2)/3 = 5,0

têm-se os centróides:

| Clusters | média x1 | média x2 | média x3|
| --- | --- | --- | --- |
| (1,2) | 9,0 | 4,0 | 8,5 |
| (3,4,5) | 2,7 | 6,0 | 5,0 |

Vamos calcular as distâncias dos objetos aos centróides dos novos clusters:

d(1;(1,2))^2 = (8-9)^2 + (3-4)^2 + (10-8,5)^2 = 4,3

d(2;(1,2))^2 = (10-9)^2 + (5-4)^2 + (7-8,5)^2 = 4,3

d(3;(1,2))^2 = (2-9)^2 + (5-4)^2 + (8-8,5)^2 = 50,3

d(4;(1,2))^2 = (3-9)^2 + (4-4)^2 + (5-8,5)^2 = 48,3

d(5;(1,2))^2 = (3-9)^2 + (9-4)^2 + (2-8,5)^2 = 103,3

d(1;(3,4,5))^2 = (8-2,7)^2 + (3-6)^2 + (10-5)^2 = 62,1

d(2;(3,4,5))^2 = (10-2,7)^2 + (5-6)^2 + (7-5)^2 = 58,3

d(3;(3,4,5))^2 = (2-2,7)^2 + (5-6)^2 + (8-5)^2 = 10,5

d(4;(3,4,5))^2 = (3-2,7)^2 + (4-6)^2 + (5-5)^2 = 4,1

d(5;(3,4,5))^2 = (3-2,7)^2 + (9-6)^2 + (2-5)^2 = 18,1

## Exercício 2

a) os valores das variâncias parecem ser muito diferentes.

b) testes de homocedasticidade

- Formulação das hipóteses:
- H0: As variâncias são iguais
- H1: Existe pelo menos um par de variâncias diferentes

- Nível de significância: alpha = 0,05

b1): Teste de Bartlett

- P-value aproximadamente 0
- Decisão: dado que alpha = 0,05 >= 0, deve-se rejeitar H0 ao nível de significância de 5%, ou seja, existe evidência estatística suficiente para concluir que as variâncias dos componentes não são idênticas.

b2): Teste de Levene

- Estatística de teste: F = 13,384
- Valor crítico, com k=5 variáveis, e n= n1+n2+...n5 = 20+20+...+20 = 100: f(K-1; n-k; 1-alpha)  = f(4;95;0,95) = 2,467494
- Decisão: Dado que Fobservado = 13,384 >= 2,467494 Logo deve-se rejeitar H0 ao nível de significância de 5%.
Ou seja, Existe evidência estatística suficiente para concluir que as variâncias da composição dos alimentos não são identicas.
