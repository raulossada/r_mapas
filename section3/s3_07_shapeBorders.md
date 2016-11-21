

# Conhecer as coordenadas min e max tanto em x quanto em y de um shape


```r
dados_municipios@bbox
```

```
Error in eval(expr, envir, enclos): object 'dados_municipios' not found
```

```r
plot( dados_municipios, axes=TRUE );
```

```
Error in plot(dados_municipios, axes = TRUE): object 'dados_municipios' not found
```

```r
points( x=dados_municipios@bbox[1,1], y=dados_municipios@bbox[2,1], col="blue" );
```

```
Error in points(x = dados_municipios@bbox[1, 1], y = dados_municipios@bbox[2, : object 'dados_municipios' not found
```

```r
points( x=dados_municipios@bbox[1,2], y=dados_municipios@bbox[2,1], col="blue" );
```

```
Error in points(x = dados_municipios@bbox[1, 2], y = dados_municipios@bbox[2, : object 'dados_municipios' not found
```

```r
points( x=dados_municipios@bbox[1,2], y=dados_municipios@bbox[2,2], col="blue" );
```

```
Error in points(x = dados_municipios@bbox[1, 2], y = dados_municipios@bbox[2, : object 'dados_municipios' not found
```

```r
points( x=dados_municipios@bbox[1,1], y=dados_municipios@bbox[2,2], col="blue" );
```

```
Error in points(x = dados_municipios@bbox[1, 1], y = dados_municipios@bbox[2, : object 'dados_municipios' not found
```

# Versão 2


```r
# Pegar as coordenadas dos polígonos de um shape
library("ggplot2");
Shape_coordenadas <- fortify(dados_municipios);
```

```
Error in fortify(dados_municipios): object 'dados_municipios' not found
```

```r
# Acrescentar umas linhas de código aqui, dá para pegar o min e max e um poligono especifico

Shape_coordenadas_MinMax <- apply(Shape_coordenadas[,c("long", "lat")], 2, range);
```

```
Error in apply(Shape_coordenadas[, c("long", "lat")], 2, range): object 'Shape_coordenadas' not found
```

```r
plot( dados_municipios, axes=TRUE );
```

```
Error in plot(dados_municipios, axes = TRUE): object 'dados_municipios' not found
```

```r
points( x=Shape_coordenadas_MinMax[1,1], y=Shape_coordenadas_MinMax[1,2] );
```

```
Error in points(x = Shape_coordenadas_MinMax[1, 1], y = Shape_coordenadas_MinMax[1, : object 'Shape_coordenadas_MinMax' not found
```

```r
points( x=Shape_coordenadas_MinMax[2,1], y=Shape_coordenadas_MinMax[1,2] );
```

```
Error in points(x = Shape_coordenadas_MinMax[2, 1], y = Shape_coordenadas_MinMax[1, : object 'Shape_coordenadas_MinMax' not found
```

```r
points( x=Shape_coordenadas_MinMax[2,1], y=Shape_coordenadas_MinMax[2,2] );
```

```
Error in points(x = Shape_coordenadas_MinMax[2, 1], y = Shape_coordenadas_MinMax[2, : object 'Shape_coordenadas_MinMax' not found
```

```r
points( x=Shape_coordenadas_MinMax[1,1], y=Shape_coordenadas_MinMax[2,2] );
```

```
Error in points(x = Shape_coordenadas_MinMax[1, 1], y = Shape_coordenadas_MinMax[2, : object 'Shape_coordenadas_MinMax' not found
```
