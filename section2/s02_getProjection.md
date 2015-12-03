

## Como ver os atributos da projeção

#### Função: proj4string

Para ver os atributos da projeção de um objeto carregado usando a função `readOGR`, podemos usar a função `proj4string` do pacote `sp`.

Parâmetros interessantes da função: 
- `obj`: Nome do objeto com os dados do shapefile.

1) Vamos carregar o shapefile:

```r
library("rgdal");
sp_mapa_rgdal <- readOGR(dsn="sp_municipios", layer="35MUE250GC_SIR", 
                         verbose=FALSE, stringsAsFactors=FALSE);
```

**2) Vamos ver qual a projeção desse shapefile:**

```r
proj4string(obj=sp_mapa_rgdal);
```

```
[1] "+proj=longlat +ellps=GRS80 +no_defs"
```

Alguns atributos de projeções:
- `+ellps`
- `+datum`
- `+proj`
- `+zone`
- `+units`
- `+init`

Sugestões de busca em inglês: "r shapefile projection".

***

#### Em outros pacotes: maptools - função: proj4string

Para um objeto carregado usando a função `readShapeSpatial`, também podemos usar a função `proj4string`.

1) Carregando o shapefile:

```r
library("maptools");
sp_mapa_maptools <- readShapeSpatial(fn="sp_municipios/35MUE250GC_SIR");
```

**2) Verificando os atributos da projeção:**

```r
proj4string(obj=sp_mapa_maptools);
```

```
[1] NA
```
Como havíamos mencionado anteriormente, a função `readShapeSpatial` não lê o arquivo ".prj" que contém as informações sobre os atributos da projeção de um shapefile. Assim, cabe ao usuário conhecer e inserir essas informações. Processo que será realizado a seguir:

3) Alterando os atributos da projeção:

```r
proj4string(obj=sp_mapa_maptools) <- "+proj=longlat +ellps=GRS80 +no_defs";
```

4) Verificando se os atributos da projeção foram alterados:

```r
proj4string(obj=sp_mapa_maptools);
```

```
[1] "+proj=longlat +ellps=GRS80 +no_defs"
```
Como podemos ver, agora o objeto `sp_mapa_maptools` possui os atributos da projeção.

****

#### Em outros pacotes: PBSmapping - Função: attr

Já para um objeto carregado usando a função `importShapefile`, temos que usar a função `attr`.

1) Carregando o shapefile:

```r
library("PBSmapping");
sp_mapa_pbsmapping <- importShapefile(fn="sp_municipios/35MUE250GC_SIR", readDBF=TRUE);
```

**2) Verificando os atributos da projeção:**

```r
attr(x=sp_mapa_pbsmapping, which="prj");
```

```
[1] "GEOGCS[\"GCS_SIRGAS_2000\",DATUM[\"D_SIRGAS_2000\",SPHEROID[\"GRS_1980\",6378137.0,298.257222101]],PRIMEM[\"Greenwich\",0.0],UNIT[\"Degree\",0.0174532925199433]]"
```
Como havíamos mencionado anteriormente, a função `importShapefile` lê o arquivo ".prj", mas usa um formato diferente do **formato proj4**, como as funções anteriores.

