# Análise discriminante linear

Objetivo: Tentar discriminar uma variável qualitativa (variável dependente) à custa de variáveis quantitativas (variáveis independentes).

## Pressupostos

- Cada grupo é uma amostra aleatória de uma população normal multivariada.

Shapiro-wilk para a normalidade multivariada (p-value)

- Matrizes de variâncias covariâncias idênticas para todos os grupos.

Teste M de Box (p-value)

## Exercício 1

Temos 4 variáveis, x1, x2, x3 e x4 (p=4)

Temos 3 variedades (grupos) de maçãs (k=3)

Para cada variedade de maçãs foram recolhidas 20 observações (n1=n2=n3=20)

- a:)
Para o 2º grupo (variedade 2 de maçã)

- Formulação das hipóteses:

H0: A amostra do 2º grupo é proveniente de uma população com distribuição normal multivariada.
H1: A amostra do 2º grupo é proveniente de uma população com distribuição diferente da distribuição normal multivariada

- Nível de significância: alpha=0,05
- P-value = 0,01613
- Decisão: dado que alpha = 0,05 >= 0,01613 = p-value deve-se rejeitar H0 ao nível de significância de 5%, ou seja, existe evidência estatística suficiente para concluir que a amostra do 2º grupo (variedade 2) não é proveniente de uma população com distribuição normal multivariada.

- a2:)

Teste M de Box para a homogeneidade das matrizes de variância covariâncias:

- Formulação das hipóteses:

H0: As matrizes de Variâncias Covariâncias são idênticas para todos os grupos
H1: As matrizes de variâncias Covariâncias não são identicas para todos os grupos

- Nível de significância: alpha=0,05

- P-value = 0,09682

- decisão: dado que alpha = 0,05 < 0,09682 = p-value, não se rejeita H0 ao nível de significância de 5%, ou seja, não existe evidência estatística suficiente para concluir que as matrizes de variâncias covariâncias não são idênticas para todos os grupos.

**Nota:** A robustez à violação do pressuposto de que a amostra de um determinado grupo é proveniente de uma população com distribuição normal multivariada (teste de shapiro-wilk para a normalidade multivvariada) **está assegurada se os grupos tiverem dimensões semelhantes de, pelo menos, 20 observações.**

## Estimação do número de funções discriminantes a considerar

m = min { k-1; p }

m - número de funções discriminantes
k = número de grupos
p = número de variáveis

Yi = ai1x1+ai2x2+...+aikxk, i = 1,2,...,m

- b:)

O número de funções discriminantes é dado por:

m = min { k-1; p } = min { 3-1; 4 } = min { 2; 4 } = 2, ou seja, devemos considerar 2 funções discriminantes.

- c:)

Análise do output para as funções discriminantes lineares lda (vard ~.  (v1, v2, v3))

vard ~ - escrevemos variedade em função das restantes variáveis (x1, x2, x3, x4)

- c1:)

**Nota:** Os coeficientes aij das funções discriminantes são uma medida relativa da importância das variáveis originais nas funções discriminantes. O sinal associado, apenas indica se a contribuição da variável é positiva ou negativa. Quanto maior for o coeficiente de uma variável numa determinada função, maior será a sua contribuição na discriminação entre grupos.

Sabemos que as funções discriminantes são dadas por: Yi  = ai1x1 + ai2x2 + ai3x3 + ai4x4, com i = 1,2

A 1ª função discriminante é dada por:

Y1 =  0,4373x1 - 0,1873x2 - 0,3093x3 - 0,2396x4

Podemos dizer que a 1ª função discriminante, é essencialmente, determinada pelas variáveis "sacarose" (x1) e "frutose" (x3). A variável x1, tem contribuição muito forte, sendo a mesma positiva, enquanto que a variável x3 tem uma contribuição negativa.

A 2ª função discriminante é dada por:

Y2 = -0,03622x1 + 0,3917x2 - 0,2999x3 - 0,1613x4

Podemos dizer que a 2ª função discriminante é, essencialmente, determinada, pelas variáveis "glicose" (x2) e x3. a variável x2 tem uma contribuição positiva, enquanto que a variável x3 tem uma contribuição negativa.

- c2:)

Sabemos que n = n1+n2+n3 = 20+20+20=60

Assim, as probabilidades a priori dos elementos pertencerem a cada um dos grupos são dadas por:

P1 = n1/n = 20/60 = 1/3
P2 = n2/n = 20/60 = 1/3
P3 = n3/n = 20/60 = 1/3

- c3:)

A média da variável "sacarose" (x1) no 1º grupo (variedade 1 das maçãs) obtem-se fazendo:

(24+27+...+32)/20 = 26,8 g/l (a amostra da variedade 1 sobre a concentração de sacarose)

- c4:)
Queremos interpretar a percentagem de variabilidade entre grupos que é explicada por cada função discriminante linear (proportion of trace)

A percentagem de variabilidade entre grupos, que é explicada pela 1ª função discriminante é 87,17%. Enquanto que, a segunda função discriminante explica 12,83% da variabilidade entre grupos.

