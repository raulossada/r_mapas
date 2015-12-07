

## Como ver os atributos da projeção

#### Função: proj4string

Para ver os atributos da projeção de um objeto carregado usando a função `readOGR`, podemos usar a função `proj4string` do pacote `sp`.

Parâmetros interessantes da função: 
- `obj`: Nome do objeto com os dados do shapefile.

1) Vamos carregar o shapefile:

```r
library("rgdal");
pb_poligonos_rgdal <- readOGR(dsn="aesa_pb/Municipios", layer="Municipios", verbose=FALSE, stringsAsFactors=FALSE);
```

**2) Vamos ver quais são os atributos da projeção desse shapefile:**

```r
proj4string(obj=pb_poligonos_rgdal);
```

```
[1] "+proj=longlat +ellps=aust_SA +no_defs"
```

Alguns atributos de projeções:
- `+ellps`
- `+datum`
- `+proj`
- `+zone`
- `+units`
- `+init`

**Importante!** É importante conhecer os atributos de uma projeção para evitar problemas como: pontos aparecendo fora de um mapa ou cálculos de distância entre pontos muito absurdos, etc.


Sugestões de busca em inglês: "r shapefile projection".
