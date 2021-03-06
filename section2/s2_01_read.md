

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

pb_poligonos_rgdal <- readOGR(dsn="aesa_pb/Municipios", 
                              layer="Municipios", 
                              verbose=FALSE, 
                              stringsAsFactors=FALSE);
```

Sugestões de busca em inglês: "r read shapefile".

Sugestões de busca em português: "r como abrir um shapefile", "r como ler um shapefile". 


**Importante!** Neste livro, os shapefiles serão carregados com essa função. 
Ficando as funções de outros pacotes como uma curiosidade extra.
