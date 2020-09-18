# Visualiza datos científicos 📊

1. Crea un gráfico que:
- [x] Utilice datos de empleo de estados unidos (data.us_employment()).
- [x] Sea un gráfico de línea.
- [x] En el eje $x$ visualices los meses.
- [x] En el eje $y$ visualices el cambio en el sector no agricola (nonfram_change).
- [x] Que la línea sea de color negro.
- [x] Que el gráfico sea de un ancho de 650px.
- [x] Que el gráfico tenga un título descriptivo.
- [x] Bonus: El mismo gráfico pero en "área", es decir, que sea un gráfico de área.

```python
import altair as alt
import seaborn as sns
from vega_datasets import data

empleos = data.us_employment()

alt.Chart(empleos).mark_line( color='black').encode(
    x = alt.X("month:T"),
    y = alt.Y("nonfarm_change:Q")
).properties(
    title = "Cambio en el sector no-agrícola de Estados Unidos (2006-2015)",
    width = 650
)
```

![visualization](https://user-images.githubusercontent.com/15655912/93651746-38d5a880-f9d8-11ea-9ffd-fdf0d636373a.png)

¿Qué enfatiza más el gráfico de área, a comparación con el de línea? Se hace más visible el cambio en el eje y, como se observa en el año 2009 y la pérdida masiva de empleos.

2. Crea un gráfico que:
- [x] Utilice el conjunto de datos de pingüinos.
- [x] Los marcadores sean barras.
- [x] En el eje $x$ se visualiza la longitud promedio de las aletas de cada especie de pingüino.
- [x] En el eje $y$ se visualiza la especie del pingüino.
- [x] Cada barra tiene también una etiqueta con la especie del pingüino.

```python
alt.Chart(empleos).mark_area( color='black').encode(
    x = alt.X("month:T"),
    y = alt.Y("nonfarm_change:Q")
).properties(
    title = "Cambio en el sector no-agrícola de Estados Unidos (2006-2015)",
    width = 650
)
```

![visualization (1)](https://user-images.githubusercontent.com/15655912/93651853-979b2200-f9d8-11ea-88e2-b5cd9ca8ecf5.png)

3. Revisa el Notebook de compartir gráficos y exporta cualquiera de los gráficos que hayas creado:
- [x] Usa los colores y formato al que consideres más adecuado.
```python
base = alt.Chart(pinguinos).mark_bar().encode(
    x = alt.X("mean(bill_length_mm):Q",title='Longitud Promedio de Aleta'),
    y = alt.Y("species:N", title='Especie'),
    color = alt.Color("species:N", legend=None)
)

texto = alt.Chart(pinguinos).mark_text(size = 16, color='black').encode(
    x = alt.X("mean(bill_length_mm):Q"),
    y = alt.Y("species:N"),
    text = alt.Text("species:N")
)

base + texto
```

![visualization (2)](https://user-images.githubusercontent.com/15655912/93651901-b6011d80-f9d8-11ea-9c23-b70ec1dbe1b3.png)
