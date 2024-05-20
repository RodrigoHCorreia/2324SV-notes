# Análise de clusters - Cont.

## Ex 

- g3:)

Método de partição das k-médias (métodos não hierárquico)

k=2:

Cluster 1: É constituido pelas observações do rio Juru.
Cluster 2: É constituido pelas observações do rio Jejawi.

Os clusters são bem separados. O cluster 2 é coeso, enquanto que o cluster 1 é pouco coeso.

k=3:

Cluster 1: É constituido pelas observações 1, 2, 4, 5 e 6 do rio Juru.
Cluster 2: É constituido pelas observações 3, 7, 8, 9, e 10 do rio Juru.
Cluster 3: É constituido pelas observações do rio Jejawi.

Os clusters estão bem separados. Os clusters 1 e 3 têm uma boa coesão interna enquanto que o cluster 2 é o que apresenta uma coeão mais fraca.

- g4:)
Análise dos gráficos de silhouette: 
k=2: todas as observações parecem estar no cluster correto, pois nenhuma delas tem coeficiente negativo. Dado que a largura média de silhouette é de 0,51 podemos concluir que estamos perante um agrupamento razoável.

k=3: Existe uma observação no cluster 2 que, provavelmente está colocada no cluster errado, porque o seu coeficiente de silhouette é negativo. Trata-se muito provavelmente, da observação Juru 3.

As restantes observações parecem estar colocadas no cluster correto. 
O valor da largura média de silhouette é de (0,51) indica que estamos perante um agrupamento razoável.

