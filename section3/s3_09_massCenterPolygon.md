

# Calcular o centro de massa de cada polígono


```r
library("rgeos");
```

```
Error in library("rgeos"): there is no package called 'rgeos'
```

```r
centro_massa_poligono <- gCentroid(spgeom=dados_municipios, byid=TRUE);
```

```
Error in eval(expr, envir, enclos): could not find function "gCentroid"
```

```r
points(centro_massa_poligono, pch=20);
```

```
Error in points(centro_massa_poligono, pch = 20): object 'centro_massa_poligono' not found
```
