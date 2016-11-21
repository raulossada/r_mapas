

# Como selecionar apenas as rodovias que passam por SP?


```r
rodovias_rgdal <- readOGR(dsn="shapefiles/Shapefiles", layer="ST_DNIT_Rodovias_SNV2015_03", verbose=FALSE, stringsAsFactors=FALSE);
```

```
Error in ogrInfo(dsn = dsn, layer = layer, encoding = encoding, use_iconv = use_iconv, : Cannot open data source
```

```r
## 1 Encontrar o indice numérico correspondente ao município desejado
indices_rodovias_SP <- which( rodovias_rgdal@data$uf=="SP" );
```

```
Error in which(rodovias_rgdal@data$uf == "SP"): object 'rodovias_rgdal' not found
```

```r
## 2 Pegar as coordenadas das linhas do município desejado
dados_rodovias_SP <- rodovias_rgdal[indices_rodovias_SP, ];
```

```
Error in eval(expr, envir, enclos): object 'rodovias_rgdal' not found
```

```r
## 3 Fazer o plot
plot( dados_rodovias_SP, axes=TRUE, col="yellow", lwd=3 )
```

```
Error in plot(dados_rodovias_SP, axes = TRUE, col = "yellow", lwd = 3): object 'dados_rodovias_SP' not found
```

```r
sp_uf <- readOGR(dsn="sp_unidades_da_federacao", layer="35UFE250GC_SIR", 
                 verbose=FALSE, stringsAsFactors=FALSE);
```

```
Error in ogrInfo(dsn = dsn, layer = layer, encoding = encoding, use_iconv = use_iconv, : Cannot open data source
```

```r
plot(sp_uf, add=TRUE, axes=TRUE);
```

```
Error in plot(sp_uf, add = TRUE, axes = TRUE): object 'sp_uf' not found
```
