# Explora un conjunto de datos para encontrar insights

Exploración de los casos de COVID-19 en México usando el conjunto de datos abiertos de la secretaría de salud.
Usa el siguiente [Notebook](https://colab.research.google.com/github/CodeandoMexico/hacking-civico/blob/master/notebooks/05_Exploracion_de_datos.ipynb) como referencia para hacer un análisis exploratorio de los datos.

Puedes encontrar el conjunto de datos [aquí](https://datos.gob.mx/busca/dataset/informacion-referente-a-casos-covid-19-en-mexico).

Una vez que hayas explorado los datos responde las siguiente preguntas:

- ## ¿Tienen los pacientes con hipertensión un riesgo más alto de defunción?
Sí, comparado con las personas sin esta comorbilidad, los pacientes con hipertensión tienen un porcentaje de defunción **4.2** veces mayor.
```python
data.groupby('hipertension').defuncion.value_counts(normalize=True)
```
| Hipertensión | Defunción | porcentaje |
|:------------:|:---------:|:----------:|
|      NO      |   False   |  0.960621  |
|              |    True   |  **0.039379**  |
|   SE IGNORA  |   False   |  0.871967  |
|              |    True   |  0.128033  |
|      SI      |   False   |  0.834159  |
|              |    True   |  **0.165841**  |

- ## ¿Cuántos casos confirmados se tienen por Estado?


- ## ¿Cuántas defunciones se tienen por Estado?
```python
defunciones_estado = data.groupby('entidad_um').defuncion.value_counts()
defunciones_estado = defunciones_estado.sort_index()[1::2]
```

- ## ¿Cuántos fallecimientos han ocurrido en el Estado con mayor número de casos confirmados?

- ## ¿Cuántos fallecimientos han ocurrido en los pacientes Ambulatorios?
