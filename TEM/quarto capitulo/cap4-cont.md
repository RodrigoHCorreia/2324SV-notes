# Rotação e interpretação dos componentes principais

## Ex 1

- m):

Notas:
O método ortogonal varimax maximiza a variação entre os pesos de cada componente principal, ou seja, maximiza as variâncias dos quadrados dos loadings.
A rotação dos componentes principais permite encontrar um novo conjunto de pesos das variáveis para cada componente. São maximizadas as diferenças entre as contribuições das variáveis, aumentando os pesos das que mais contribuem e diminuindo os pesos das que menos contribuem. Depois de efetuada a rotação, torna-se mais simples identificar e interpretar cada componente principal. A partir dos pesos das variáveis que as compõe.
Quando mais perto de 1 ou de -1, mais forte é a associação entre essa variável e a componente, enquanto que um peso próximo de zero permite concluir que essa variável pouco contribui para a formação do factor. Em geral, são considerados como significativos os pesos iguais ou superiores a 0,5 (em valor absoluto). Quando se usa o software R, após a rotação com método ortoggonal VARIMAX, os pesos entre -0,1 e 0,1, por defeito não aparecem. Assume-se que esses valores são aproximadamente zero.

- m1):

Componentes principais obtidas pelo método de rotação ortogonal de VARIMAX:

Y1 = -0,161x1+0,893x2+0,834x3-0,504x4+0,492x5+0,379x6+0,888x7+0,613x8

As variáveis "serviço pós venda" (x2), não desvalorização (x3), preço de compra (x4), "segurança" (x7) e facilidade condução (x8) são as que têm maior peso. Apenas a variável X4 tem uma contribuição negativa.

Y3 = -0,163x1+0,381x2+0,490x3-0,563x4+0,707x5+0,880x6+0,351x7-0,317x8

As variáveis x4, x5 e x6 sã oas que têm maior peso. apenas a variável x4 tem uma contribuição negativa.

Y2 = 0,965x1-0,168x3+0,621x4-0,421x5-0,239x6+0,695x8

As variáveis X1, X4 e X8 são as que têm maior peso, todas elas com valor positivo:

RC1: x2, x3 e x7
RC3: x5 e x6
RC2: x1, x4 e x8

Proporção da variância explicada por cada componente principal: 

RC1 = 0,415 (41,5%) Em falta ~= 58,5%
RC3 = 0,694-0,415= 0,279 (27,9%)
RC2 = 0,259 (25,9%)

A variância explicada acumulada por cada uma das componentes principais é dada por: 

RC1 = 0,415
RC3 = 0,415 + 0,279 = 0,694
RC2 = 0,694+0,279=0,953

- m2):

Análise do gráfico dos scros (a verificar o nome).
**Rotação da primeira componente principal:** Esta componente tende a distinguir os veículos pelo x2, x3, x4, x7 e x8. Por exemplo, distingue as marcas de veículos mais baratas, com pior serviço pós venda, com maior desvalorização, como é o caso das marcas trabant e wartburg, das marcas de veículos mais caras, com melhor serviço pós venda e com menos desvalorização, como é o caso das marcas BMW, Mercedes e Volvo. Separa ainda, as marcas Citroen, Fiat, Ford, Hyundai, Lada, entre outras, por terem características intermédias nos testes avaliados. 

**Rotação da terceira componente principal:** Esta componente tende a distinguir os veículos pelo x4, x5 e x6. Por exemplo, agrupa as marcas Ferrari e Jaguar, que são ambas marcas caras e com designo mais apelativo e em oposição relação as marcas trabant e wartburbg, por serem mais baratas e com um design menos atrativo.

**Rotação da segunda componente principal:** Esta componente tende a distinguir os veículos pelo x1, x4 e x8. Por exemplo, dinstingue as marcas de veículos mais económicos, como é o caso da Fiar, Opel, Ford, Nissan, Hyundai, entre outras, das marcas que apresentam consumos mais elevados como é o caso da Ferrari, Jaguar, Watburg e Trabat.

## Ex 2

a) Vamos analisar o teste de esfericidade de Bartlett: 
- Formulação da hipóteses:
- H0 : p = I (Matriz de correlações == matriz identidade)
- H1 : p = I

- Nível de significância: alpha = 0,01
- Tamanho da amostra: n = 4171
- Valos da estatística de teste: Qui^2obs = 6779,29
- p-value aproximadamente 0
- Valor crítico:
- (Qui^2p(p-1))/2;1-alpha = qui^228;0,99 = 48,2782

- Decisão:
Dado que Qui^2O = 67799,29 >= 48,2782 = Qui^2 28;0,99 
ou
0~= p-value 
Deve-se rejeitar H0 ao nível de significância de 1%, ou seja, existe evidência estatística suficiente para concluir que a técnica de análise de componentes principais é adequada para analisar estes dados, pelo que se concluir que existem correlações significativas entre as variáveis.

b)
Análise do output do teste K-M-O

- Valor da estatística de teste: KMO = 0,86 (overall MSA)
- Decisão: A adequação da técnica de análise de componentes principais a estes dados é "Boc"  (overall MSA E  [0,80; 0,90])
