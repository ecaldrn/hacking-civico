# Explora un conjunto de datos para encontrar insights

Exploración de los casos de COVID-19 en México usando el conjunto de datos abiertos de la secretaría de salud.
Usa el siguiente [Notebook](https://colab.research.google.com/github/CodeandoMexico/hacking-civico/blob/master/notebooks/05_Exploracion_de_datos.ipynb) como referencia para hacer un análisis exploratorio de los datos.

Puedes encontrar el conjunto de datos [aquí](https://datos.gob.mx/busca/dataset/informacion-referente-a-casos-covid-19-en-mexico).

Una vez que hayas explorado los datos responde las siguiente preguntas:

- ## ¿Tienen los pacientes con hipertensión un riesgo más alto de defunción?
Sí, comparado con las personas sin esta comorbilidad, los pacientes con hipertensión tienen un porcentaje de defunción **4.2** veces mayor.

| Hipertensión | Defunción | porcentaje |
|:------------:|:---------:|:----------:|
|      NO      |   False   |  0.960621  |
|              |    True   |  **0.039379**  |
|   SE IGNORA  |   False   |  0.871967  |
|              |    True   |  0.128033  |
|      SI      |   False   |  0.834159  |
|              |    True   |  **0.165841**  |

- ## ¿Cuántos casos confirmados se tienen por Estado?
|            entidad_um           |  #casos |
|:-------------------------------:|:------:|
|          AGUASCALIENTES         |  6351  |
|         BAJA CALIFORNIA         |  18012 |
|       BAJA CALIFORNIA SUR       |  8740  |
|             CAMPECHE            |  5881  |
|             CHIAPAS             |  6063  |
|            CHIHUAHUA            |  8832  |
|         CIUDAD DE MÉXICO        | 131667 |
|       COAHUILA DE ZARAGOZA      |  23817 |
|              COLIMA             |  4219  |
|             DURANGO             |  7449  |
|            GUANAJUATO           |  35902 |
|             GUERRERO            |  15963 |
|             HIDALGO             |  10988 |
|             JALISCO             |  22877 |
|       MICHOACÁN DE OCAMPO       |  17281 |
|             MORELOS             |  5241  |
|              MÉXICO             |  52283 |
|             NAYARIT             |  5323  |
|            NUEVO LEÓN           |  33214 |
|              OAXACA             |  14460 |
|              PUEBLA             |  29636 |
|            QUERÉTARO            |  7712  |
|           QUINTANA ROO          |  10886 |
|         SAN LUIS POTOSÍ         |  20381 |
|             SINALOA             |  17213 |
|              SONORA             |  22954 |
|             TABASCO             |  30033 |
|            TAMAULIPAS           |  26437 |
|             TLAXCALA            |  5925  |
| VERACRUZ DE IGNACIO DE LA LLAVE |  29973 |
|             YUCATÁN             |  16452 |
|            ZACATECAS            |  6134  |

- ## ¿Cuántas defunciones se tienen por Estado?
|            entidad_um           | # defunciones |
|:-------------------------------:|:-------------:|
|          AGUASCALIENTES         |      625      |
|         BAJA CALIFORNIA         |      4014     |
|       BAJA CALIFORNIA SUR       |      524      |
|             CAMPECHE            |      968      |
|             CHIAPAS             |      1145     |
|            CHIHUAHUA            |      2012     |
|         CIUDAD DE MÉXICO        |     15004     |
|       COAHUILA DE ZARAGOZA      |      2188     |
|              COLIMA             |      637      |
|             DURANGO             |      697      |
|            GUANAJUATO           |      3140     |
|             GUERRERO            |      2216     |
|             HIDALGO             |      2083     |
|             JALISCO             |      3887     |
|       MICHOACÁN DE OCAMPO       |      1856     |
|             MORELOS             |      1238     |
|              MÉXICO             |     10685     |
|             NAYARIT             |      812      |
|            NUEVO LEÓN           |      3543     |
|              OAXACA             |      1577     |
|              PUEBLA             |      4686     |
|            QUERÉTARO            |      1056     |
|           QUINTANA ROO          |      1892     |
|         SAN LUIS POTOSÍ         |      1742     |
|             SINALOA             |      3739     |
|              SONORA             |      3313     |
|             TABASCO             |      2978     |
|            TAMAULIPAS           |      2891     |
|             TLAXCALA            |      1252     |
| VERACRUZ DE IGNACIO DE LA LLAVE |      4693     |
|             YUCATÁN             |      1810     |
|            ZACATECAS            |      751      |

- ## ¿Cuántos fallecimientos han ocurrido en el Estado con mayor número de casos confirmados?
**15004** personas han fallecido en Ciudad de México, lugar donde hay el mayor número de casos confirmados.

- ## ¿Cuántos fallecimientos han ocurrido en los pacientes Ambulatorios?
**9558** pacientes ambulatorios han fallecido.
