

## Como plotar um mapa no R

#### Função: plot

Para plotar um mapa de um objeto carregado usando a função `readOGR`, podemos usar a função `plot`.

Parâmetros interessantes da função: 
- `axes`: Indica se devem ser plotados os eixos x e y do gráfico.
- `border`: Define a cor da linha de borda dos polígonos. (Exemplos: "black", "darkgray", "red", etc).
- `lty`: Define o tipo da linha de borda. (1-linha contínua, 2-tracejado, 3-pontos, etc).
- `lwd`: Define a grossura das linhas de borda.
- `col`: Define a cor de preenchimento dos polígonos. (Exemplos: "white", "brown", "blue", etc)
- `main`: Texto do título do gráfico.

1) Vamos carregar o shapefile:

```r
library("rgdal");
pb_poligonos_rgdal <- readOGR(dsn="aesa_pb/Municipios", layer="Municipios", verbose=FALSE, stringsAsFactors=FALSE);
```

**2) Vamos plotar o mapa**

```r
plot(pb_poligonos_rgdal, axes=TRUE, border="darkgrey", lty=1, lwd=1, col="white", main="Mapa dos municipios do Estado da Paraiba");
```

<img src="figure/unnamed-chunk-2-1.png" title="plot of chunk unnamed-chunk-2" alt="plot of chunk unnamed-chunk-2" style="display: block; margin: auto;" />

Sugestões de busca em inglês: "r plot shapefile".
