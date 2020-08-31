# Calcula la densidad poblacional y encuentra relaciones con el gasto público 🏙️

Muchas veces vemos cómo año con año cambian los montos en el presupuesto para el gasto público destinado a cierto sector específico (como salud, educación, etc.), pero para saber si de verdad se está invirtiendo más o sólo se está ajustando al incremento de la población, es necesario ver si el gasto per cápita aumenta, se mantiene o disminuye comparado con lo años previos. Para esto deberás investigar el dato del gasto público del último año y uno anterior del sector de tu interés (puede ser a nivel local, estatal o federal en cualquier tema) y crea una programa en Python que te ayude a calcular la densidad población y el gasto per cápita.

## Pasos a seguir 📚 (Solución en la siguiente sección :bookmark_tabs:)

### ☝️ Primero:
- [x] Investiga el número de habitantes que hay en tu ciudad, estado y país, así como la superficie (en km²) de los mismos.
- [x] Escribe una función llamada densidad_poblacional que tome dos argumentos, poblacion y area_ciudad.
- [x] Haz que la función devuelva una densidad de población calculada a partir de esos valores (investiga la fórmula).
- [x] Prueba esta función con los 3 casos diferentes: país, tu estado y tu ciudad.
- [x] Responde lo siguiente:
  * ¿Cuál es la densidad poblacional?
  * ¿Qué pasa comparar varios estados o ciudades?
  
### ☝️ Segundo:

Utiliza la información que encontraste sobre el gasto público del sector de tu interés y de acuerdo a la población correspondiente calcula el gasto per cápita del último año y uno anterior.

* [x] Responde lo siguiente:
  * ¿En qué porcentaje aumentó o disminuyó?
  * ¿A qué crees que se deba?
  
### ☝️ Tercero:
* [x] Responde lo siguiente:
  * ¿Para qué crees que nos pueda ser útil esta información?
  * ¿Qué decisiones podría tomar el gobierno basado en ésta?
  
## Solución :floppy_disk:

 **Población:**
 * Salamanca: 273,271 habitantes
 * Guanajuato: 5,853,677 habitantes
 * México: 119,530,753 habitantes

 **Superficie:**
 * Salamanca: 756,54 km²
 * Guanajuato: 30,608 km²
 * México: 1,964,375 km²
 
 ```python
def densidad_poblacional(poblacion,area_ciudad):
    """
    Entrega la densidad poblacional de una ciudad
    
    Parameters:
                    poblacion (int): An integer
                    area_ciudad (int, float): A decimal integer

            Returns:
                    dp (float): Float of the quotient of the input parameters.
    """
    dp = poblacion/area_ciudad
    return dp
```

 **Densidad Poblacional**
 * Salamanca: 361.211 hab/km²
 * Guanajuato: 191.246 hab/km²
 * México: 60.849 hab/km²
 
 **Qué pasa al comparar varios estados o ciudades?**
 Permite inferir algunas cosas como el tipo de asentamiento (las zonas urbanas son regularmente más densas que las zonas rurales). De igual manera la densidad de población nos ayuda a conocer mejor el tipo de problemas que tienen las zonas comparadas.
 
 **Gasto público en el ámbito de desarrollo social**
* **2019**
  * Nivel Federal: $3,311,000,000,000.00
  * Nivel Estatal: $49,469’041,584.91
* 2020
  * Nivel Federal: $2,797,320,000,000.00
  * Nivel Estatal: $48,542’831,578.33
 
 **¿El porcentaje aumentó o disminuyó?**
 En ambos casos **disminuyó**, 15.5% para el gasto federal y 1.8% para el gasto estatal.
 
 **¿A qué crees que se deba?** 
 Creo que se debe a que esa parte se destinó a otras áreas donde hay crisis como salud y seguridad.
 
 **¿Para qué crees que nos pueda ser útil esta información?**
 Para tener una referencia respecto a lo que se está realizando en el gobierno federal, para ver al final del año el impacto que tuvieron los ajustes realizados a los ámbitos comparados.
 
**¿Qué decisiones podría tomar el gobierno basado en ésta?**
Verificar que impacto tiene el dinero gastado y ver donde es más necesario invertir. Fortalecer los programas que han tenido resultados favorables y mejorar o eliminar los que no han surtido efecto, todo esto para enfrentar la crisis sanitaria y económica actual.
 
 
 ### Fuentes 
 1. [Data México](https://datamexico.org/)
 1. [Ley del presupuesto general de egresos estatal 2019](https://finanzas.guanajuato.gob.mx/c_legislacion/doc/leyes_estatales/Ley_del_Presupuesto_General_de_Egresos_2019.pdf)
 1. [Ley del presupuesto general de egresos estatal 2020](https://finanzas.guanajuato.gob.mx/c_legislacion/doc/leyes_estatales/ley_de_pge_del_estado_de_guanajuato_p_el_ejerc2020.pdf)
 1. [Transparencia Presupuestaria Gob 2019](https://www.transparenciapresupuestaria.gob.mx/es/PTP/infografia_ppef2019#:~:text=En%20el%20ejercicio%20fiscal%202019,con%20respecto%20al%20a%C3%B1o%20anterior.)
 1. [Transparencia Presupuestaria Gob 2020](https://www.transparenciapresupuestaria.gob.mx/es/PTP/infografia_ppef2020)
