

#http://stackoverflow.com/questions/13443372/simple-way-to-subset-spatialpolygonsdataframe-i-e-delete-polygons-by-attribut

# http://stackoverflow.com/questions/22525647/r-highlighting-some-of-the-boundaries-or-borders-of-the-region-in-a-shape-file

Topico ligado aos s3_08=7 e s3_08

# Pegar as coordenadas de um polígono específico


```r
## 1 Pegar os polígonos do shape
shape_ListaPoligonos <- dados_municipios@polygons;
```

```
Error in eval(expr, envir, enclos): object 'dados_municipios' not found
```

```r
## 2 Pegar os dados de um polígono específico
SubPoligono_dados <- slot(shape_ListaPoligonos[[4]],"Polygons");
```

```
Error in slot(shape_ListaPoligonos[[4]], "Polygons"): object 'shape_ListaPoligonos' not found
```

```r
class(SubPoligono_dados);
```

```
Error in eval(expr, envir, enclos): object 'SubPoligono_dados' not found
```

```r
## 3 Transforma da estrutura lista para a estrutura Polygon
SubPoligono_dados <- SubPoligono_dados[[1]];
```

```
Error in eval(expr, envir, enclos): object 'SubPoligono_dados' not found
```

```r
class(SubPoligono_dados);
```

```
Error in eval(expr, envir, enclos): object 'SubPoligono_dados' not found
```

```r
## 4 Pega as coordenadas do subpolígono
SubPoligono_coordenadas <- SubPoligono_dados@coords;
```

```
Error in eval(expr, envir, enclos): object 'SubPoligono_dados' not found
```
