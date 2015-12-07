

## Como ver a classe de um objeto

#### Função: class

Para ver a classe do objeto que guarda os dados do shapefile podemos usar a função `class`.

Parâmetros interessantes da função: 
- `x`: Nome do objeto com os dados do shapefile.

1) Vamos carregar o shapefile:

```r
library("rgdal");
pb_poligonos_rgdal <- readOGR(dsn="aesa_pb/Municipios", layer="Municipios", verbose=FALSE, stringsAsFactors=FALSE);
```

**2) Vamos ver qual a classe do objeto que guarda os dados do shapefile:**

```r
class(x=pb_poligonos_rgdal);
```

```
[1] "SpatialPolygonsDataFrame"
attr(,"package")
[1] "sp"
```

Como podemos ver, nosso objeto pertence à classe **SpatialPolygonsDataFrame**. Ou seja, trata-se de um objeto que contém informações sobre um **shape de polígonos (*Spatial Polygons*)**.

Outras possibilidades que iremos explorar serão os objetos que contêm informações sobre um **shape de linhas (*Spatial Lines*)** e sobre um **shape de pontos (*Spatial Points*)**.

**Importante!** É importante saber à que tipo de classe um objeto pertence, pois uma mesma função pode apresentam saídas diferentes dependendo do tipo de objeto que é fornecido como entrada.


Sugestões de busca em inglês:
