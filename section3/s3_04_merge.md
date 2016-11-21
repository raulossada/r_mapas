

# Como fazer um merge de 2 SpatialPolygonsDataFrame


```r
osasco <- sp_mapa[which( sp_mapa@data$NM_MUNICIP == "OSASCO"), ];
```

```
Error in eval(expr, envir, enclos): object 'sp_mapa' not found
```

```r
mogi <- sp_mapa[which( sp_mapa@data$NM_MUNICIP == "MOGI DAS CRUZES"), ];
```

```
Error in eval(expr, envir, enclos): object 'sp_mapa' not found
```

```r
## Via maptools
library("maptools")
```

```
Error in library("maptools"): there is no package called 'maptools'
```

```r
bel_nld <- spRbind(osasco, mogi)
```

```
Error in eval(expr, envir, enclos): could not find function "spRbind"
```

```r
plot(bel_nld)
```

```
Error in plot(bel_nld): object 'bel_nld' not found
```

```r
## Via sp
library("sp")
bel_nld1 <- rbind(osasco, mogi)
```

```
Error in rbind(osasco, mogi): object 'osasco' not found
```

```r
plot(bel_nld1, col=c("red", "blue") )
```

```
Error in plot(bel_nld1, col = c("red", "blue")): object 'bel_nld1' not found
```
