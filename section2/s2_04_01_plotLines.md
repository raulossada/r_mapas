

## Como plotar um mapa no R

#### Extra: Adicionar um shape de linhas

Vamos adicionar o shape de linhas de Estrada de Ferro

1) Carregar o shape de polígonos e verificar os atributos de sua projeção:

```r
pb_poligonos_rgdal <- readOGR(dsn="aesa_pb/Municipios", layer="Municipios", verbose=FALSE, stringsAsFactors=FALSE);

proj4string(pb_poligonos_rgdal);
```

```
[1] "+proj=longlat +ellps=aust_SA +no_defs"
```

2) Carregar o shape de linhas e verificar os atributos de sua projeção:

```r
pb_linhas_rgdal <- readOGR(dsn="aesa_pb/Estrada_Ferro", layer="Estrada_Ferro", verbose=FALSE, stringsAsFactors=FALSE);

proj4string(pb_linhas_rgdal);
```

```
[1] "+proj=longlat +ellps=aust_SA +no_defs"
```

**Observe** que no caso deste exemplo os atributos do shape de polígonos e de linhas são os mesmos. Caso eles fossem diferentes seria necessário transformar os atributos de um dos shapes para garantir a consistência de nossas análises.

3) Plotar o mapa de municípios e adicionar as linhas da estrada de ferro:

```r
plot(pb_poligonos_rgdal, axes=TRUE, border="darkgrey", lty=1, lwd=1, col="white", main="Mapa dos municipios do Estado da Paraiba (Estrada de Ferro)");

plot(pb_linhas_rgdal, add=TRUE, col="black");
```

<img src="figure/unnamed-chunk-3-1.png" title="plot of chunk unnamed-chunk-3" alt="plot of chunk unnamed-chunk-3" style="display: block; margin: auto;" />

Sugestões de busca em inglês:
