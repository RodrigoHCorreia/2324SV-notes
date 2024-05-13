# Análise de clusters (Continuação)

- Se temos dendrograma, é um método hierárquico

## Ex2 

- g2:

Análise da representação gráfica da análise de clusters


- k=3 clusters, com os métodos da ligação simples e da ligação média: Os clusters estão bem separados. O cluster 2 tem uma coesão interna mais fraca devido aos alimentos "queijo serra" e "queijo flamengo". Estes clusters são consistentes com os resultados obtidos para os dendrogramas.
- k=3 clusters, com o método da ligação completa: O cluster 1 e o cluster 2 têm uma separação um pouco mais fraca, estes dois clusters também apresentam uma coesão mais fraca, devido aos alimentos "azeite e manteiga", no caso do cluster 1 e devido ao "queijo da serra" e "queijo flamengo", no caso do cluster 2. Estes clusters são consistentes com os resultados obtidos para os dendrogramas.
- k=4 clusters, para os métodos de ligação simples e média: Os clusters estão bem separados e são coesos. Estes clusters são consistentes com os resultados obtidos para os dendrogramas.
- k=4 clusters, para o método da ligação completa: Estes clusters apresentam uma separação mais fraca, quando comparados com os clusters obtidos pelos outros dois métodos. apenas o cluster 2 apresentam uma coesão fraca, porque os alimentos "queijo da serra" e "queijo flamengo" estão muito afastados dos restantes alimentos desses clusters. Os clusters obtidos são consistentes como os clusters que se observa nos dendrogramas.

- g3:

Para os métodos de ligação simples e da ligação médica obtêm-se soluções de qualidade razoável (>0,8). Apesar disto, estes resultados são inferiores aos que se obtiverem com a distância euclidiana.
Para o método da ligação completa, obtêm-se um valor (<0,8) que nos obriga a ponderar se existe ou não uma estrutura hierárquica nas observações e que talvez devessemos usar outros métodos de aglomeração.

**Coeficientes de correlação cofenética só se usa com métodos hierarquicos**

- Próximo de 1 - agrupamento bom
- interior a 0,8 - o agrupamento hierárquico fica em causa

- g4:

Para os métodos da ligação simples e média, o número ótimo de clusters é 4. Para o método da ligação completa o número ótimo de clusters é 2.

- g5:

A análise da representação dos clusters, sugere que se considerem os seguintes clusters:

| 2 clusters| Método da ligação completa |
| --- | --- |
| Cluster 1 | Restantes alimentos |
| Cluster 2 | Feijão |

O cluster 1 apresenta uma coesão fraca e, ambos os clusters apresentam uma separação mais fraca.
Todos estes resultados permitem concluir que a distância de mahalanobis, em conjunto com o método da ligação completa terá uma má adequação aos dados.

- h1: 

Anãlise dos resultados obtidos com o método não hierárquico de particionamento das k-médias:

Da análise do gráfico do número ótimo de clusters decidimos considerar k=4, k=5 e k=6 clusters.

- h2:

**Nota (slide 61)** - o quociente entre a soma de quadrados entre os grupos e a total deve ser máxima.
O quociente entre as somas dos quadrados entre os grupos e a soma de quadrados total deve ser máxima. 
Como se pode observar, quando consideramos k=6 clusters obtivemos somas de quadrados dentro dos grupos com valores menores e um quociente entre as somas de quadrados entre grupos e a soma de quadrados total máxima (91,8%).
Assim, k=6 parece ser a melhor solução.

- h3:
Análise das representações da análise de clusters se pelo método de partição das k-médias:

- k=4:
Cluster 1: feijão, cenoura, espinafres
Cluster 2: restantes alimentos
Cluster 3: manteiga, azeite
Cluster 4: queijo da serra, queijo flamengo

Os clusters 1 e 2 não estão bem separados.
O cluster 1 é pouco coeso porque o "feijão" está muito afastado das "cenouras" e dos "espinafres".

- k=5:
Cluster 1: Restantes alimentos
Cluster 2: Manteiga, azeite
Cluster 3: queijo da serra, queijo flamengo
Cluster 4: feijão
Cluster 5: frango, vaca, pescada, massa, arroz, pão

Os clusters 1 e 5 estão mal separados.
No qual, os clustrs são coesos.

- k=6:

Cluster 1: Frango, vaca, pescada
Cluster 2: Couve, cenoura, espinafres, alface
Cluster 3: Queijo serra e queijo flamento
Cluster 4: restantes alimentos
Cluster 5: manteiga e azeite
Cluster 6: feijão

Os clusters 2 e 4 estão mais mal separados.
Os clusters são coesos.

**coeficiente de silhouette (dá para todos e é fácil de observar)** - Uma barra por indivíduo/objeto
valores entre -1 e 1
O coeficiente é 0 se o cluster é formado por apenas um indivíduo
Se for um valor próximo de 0 - o indivíduo está na fronteira entre dois clusters
Se o valor é negativo - o indivíduo está no cluster errado

- h4:

Análise dos gráficos de silhouette:

- k=4: todos os alimentos parecem estar no cluster correto, pois membros deles tem valor de silhouette negativo. O valor da largura média de silhouette indica que se trata de um agrupamento razoável.
