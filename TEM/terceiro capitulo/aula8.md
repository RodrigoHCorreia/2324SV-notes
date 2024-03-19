# Continuação 

## Ex 1

- g):

- Parâmetro a estimar: Y0
- Nível de confiança: 1-Alpha = 0,99
- Dimensão da amostra: n=16
- Variável fulcral: 
- Outros dados:
- Quando x0 = [1, 80, 8]
- Tem-se Y com til 0 = 2244,46
- Intervalo de confiança determinista:

]I0,99[ * Y0 = ]2210,806;2278,114[
Estima-se que o valor de Y para a observação x1 = 80, e x2 = 8, varia entre 2210,806 e 2278,114, com um nível de confiança de 99%.

## Seleção das variáveis e construção do "melhor" modelo

![alt text](<WhatsApp Image 2024-03-19 at 11.55.04_f2ed094a.jpg>)

## Ex 1

- h):

Nota: Na regressão múltipla, R^2 não é um bom indicador do grau de ajustamento do modelo.
Por outro lado, o modelo com maior R^2ajust é coinsiderado como sendo um bom candidato para a melhor equação de regressão.
Da avaliação do output para r^2ajust, conclui-se que o "melhor" modelo é o que tem maior valor de r^2ajust, (0,916), obtido com as duas variáveis, podendo escrever-se a equação:

y com til i = 1566,0778 + 7,6213xi1 + 8,5848x12, com i=1,...,16

## Método da regressão StepWise:

- AIC - Akaike Information Criterion
- Funciona em três direções possíveis:
- Forward
- Backward
- both

## Ex 1

- i):

Nota: O AIC - Akaike Information Criterion - é uma medida de ajustamento que penaliza o modelo por ter demasiadas variáveis.
Sabemos que, se o AIC aumenta, o ajustamento piora. Se o AIC diminui, o ajustamento melhor.
A regressão stepwise, pode ser feita para três dimensões:

- Forward: começa com o modelo só com B0 e vai-se acrescentando uma a uma das variáveis.
- Backward: Começa-se com todas as variáveis e vai-se retirando uma a uma das variáveis. (**é preferível ao forward**)
- Both: mistura-se os dois casos anteriores.

- i1) i2) i3)

Da avaliação do output, conclui-se que o "melho" modelo é o que tem menor valor de AIC (92,11), obtido com as duas variáveis independentes, escrevendo-se a equação: 
y com til i = 1566,078+7,621xi1+8,585xi2, com i=1,...,16

## Ex 2

- a) O modelo de regressão múltipla ajustado é o seguinte:

![alt text](<WhatsApp Image 2024-03-19 at 12.39.41_434c33a5.jpg>)

- b): 

r^2ajust = 1- ((27-1)/(27-12))(1-0,9484) = 0,91056

Podemos concluir que o modelo de regressão múltipla é um ajustamento de boa qualidade, pois cerca de 91,6% da variabilidade da concentração do magnésio é bem explicada pelas restantes variáveis independentes, (cálcio, sódio, ferro, zinco, cobre, cómio, cádmio, chumbo, arsénio, cobalto e manganês), através do modelo ajustado.

- c):
Como se pode verificar, pela observação do gráfico de comparação de quantis, o conjunto de pontos obtido forma uma linha aproximadamente reta, o que nos permite supor que os dois conjuntos de quantis deverão ser provenientes de uma população com distribuição normal.
Para além disso, existe um valor que apresenta um grande afastamento dos restantes erros, e2=4,097, o que nos leva a desconfiar que este resíduo (e2) poderá ser um outlier.

- c2) Da observação dos diagrama de extremos e quantis podemos concluir que a amostra dos resíduos tem um outlier, que é o maior valor observado, e2 = 4,097, em seguida vamos classificar este outlier.Para isso podemos calcular a barreira externa superior: Q3/4 + 3IQ.
Sabemos que (output da alínea (a)):
- 1º Quantil: Q1/4 = -1,0852
- 3º Quantil: Q3/4 = 0,7419
Então, tem-se o intervalo inter-quantis:
IQ = Q3/4 - Q1/4 = 0,7419 - (-1,0852) = 1,8271

Assim, tem-se a barreira externa superior:

Q3/4 + 3IQ = 0,7419 + 3*1,8271 = 6,2232

Dado que e2 = 4,097 < 6,2232 = Q3/4 + 3IQ, podemos concluir que e2=4,097 é um outlier moderado.

- c3):

Análise de um teste de aderência ou qualidade de ajuste de Kolmogorov-Smirnov, com correção de Lilliefors:

Formulação das hipóteses:

H0: A amostra de resíduos é possivelmente de uma população com distribuição normal
H1: A amostra de resíduos não é de uma população com distribuição normal

Nível de significância: alpha = 0,01
Dimensão da amostra: n = 27
Valor da estatística de teste:
D0 = 0,12141
P-value = 0,3884
Valor crítico para n=27 e alpha = 0,01:
Dcrítico;0,01 = 0,195 (fazendo a média de 25 e 30) ou 0,198 (fazendo o cálculo correto dado no fim da tabela)
Decisão: Dado que:

D0 = 0,12141 < D crítico;0,01 = 0,198
ou
alpha = 0,01 > p-value = 0,3884

Não se deve rejeitar H0 ao nível de significância de 1%, ou seja, não existe evidência estatística significante para concluir que a amostra de resíduos não é de uma população com distribuição normal.

