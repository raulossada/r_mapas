

## Como carregar um shapefile no R

#### Função: readOGR

Recomenda-se o uso da função `readOGR` do pacote `rgdal`, pois esta lê tanto o arquivo ".shp", quanto o arquivo ".prj".

Parâmetros interessantes da função: 
- `dsn`: Pasta (diretório), onde se encontram os arquivos (\*.cpg, \*.dbf, \*.prj, \*.shp, \*.shx, etc).
- `layer`: Nome do arquivo, sem a extensão.
- `verbose`: Indica se deve ser exibido um relatório de progresso da leitura do arquivo.
- `stringsAsFactors`: Indica se os vetores do tipo *character* devem ser convertidos para o tipo *factor*.


```r
library("rgdal");
sp_mapa_rgdal <- readOGR(dsn="sp_municipios", layer="35MUE250GC_SIR", 
                         verbose=FALSE, stringsAsFactors=FALSE);
```

Sugestões de busca em inglês: "r read shapefile".
Sugestões de busca em português: "r como abrir um shapefile", "r como ler um shapefile". 


**Importante!** Neste livro, os shapefiles serão carregados com essa função. 
Ficando as funções de outros pacotes como uma curiosidade extra.

***

#### Outras funções: readShapeSpatial

Outra função que pode ser usada é a `readShapeSpatial` do pacote `maptools`, mas ela só lê o arquivo ".shp".
Ficando a cargo do usuário inserir manualmente as informações sobre a projeção, contidas no arquivo ".prj". Ou seja, essa função supõe que o usuário já saiba quais são os atributos da projeção do shape.

```r
library("maptools");
sp_mapa_maptools <- readShapeSpatial(fn="sp_municipios/35MUE250GC_SIR");
```

****

#### Outras funções: importShapefile

Por fim, pode-se usar a função `importShapefile` do pacote `PBSmapping`, que lê tanto o arquivo ".shp" quanto o arquivo ".prj", porém não utiliza o **formato proj4** para os atributos da projeção, como as funções anteriores.

```r
library("PBSmapping");
sp_mapa_pbsmapping <- importShapefile(fn="sp_municipios/35MUE250GC_SIR", readDBF=TRUE);
```

