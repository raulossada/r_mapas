

# Conhecer as coordenadas min e max tanto em x quanto em y de um polígono específico


```r
SubPoligono_coordenadas_MinMax <- apply(SubPoligono_coordenadas, 2, range);
```

```
Error in apply(SubPoligono_coordenadas, 2, range): object 'SubPoligono_coordenadas' not found
```

```r
plot( dados_municipios, axes=TRUE );
```

```
Error in plot(dados_municipios, axes = TRUE): object 'dados_municipios' not found
```

```r
points( x=SubPoligono_coordenadas_MinMax[1,1], y=SubPoligono_coordenadas_MinMax[1,2] );
```

```
Error in points(x = SubPoligono_coordenadas_MinMax[1, 1], y = SubPoligono_coordenadas_MinMax[1, : object 'SubPoligono_coordenadas_MinMax' not found
```

```r
points( x=SubPoligono_coordenadas_MinMax[2,1], y=SubPoligono_coordenadas_MinMax[1,2] );
```

```
Error in points(x = SubPoligono_coordenadas_MinMax[2, 1], y = SubPoligono_coordenadas_MinMax[1, : object 'SubPoligono_coordenadas_MinMax' not found
```

```r
points( x=SubPoligono_coordenadas_MinMax[2,1], y=SubPoligono_coordenadas_MinMax[2,2] );
```

```
Error in points(x = SubPoligono_coordenadas_MinMax[2, 1], y = SubPoligono_coordenadas_MinMax[2, : object 'SubPoligono_coordenadas_MinMax' not found
```

```r
points( x=SubPoligono_coordenadas_MinMax[1,1], y=SubPoligono_coordenadas_MinMax[2,2] );
```

```
Error in points(x = SubPoligono_coordenadas_MinMax[1, 1], y = SubPoligono_coordenadas_MinMax[2, : object 'SubPoligono_coordenadas_MinMax' not found
```
