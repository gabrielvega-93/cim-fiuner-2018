# PENELOPE. Introducción.

#### P. Pérez
###### FI-UNER, 5/07/18

---

## PENELOPE

### PENetration and Energy LOss of Positrons and Electrons

Al principio PENELOPE  no incorporaba fotones.

### Nuclear Energy Agency

Proyecto de la Agencia de Energía Nuclear Europea.

### Universitat de Barcelona

Salvat, Fernandez-Varea y Sempau. Directores del proyecto.

---

## PENELOPE

* Realiza simulación Monte Carlo del transporte acoplado electrón-fotón.
* Sobre materiales arbitrarios.
* Rango de energías entre algunos eV a aproximadamente 1 GeV.
* Transporte detallado estándar de fotones.
* Historias de electrones y positrones generadas en base a procedimiento mixto que combina simulación detallada de eventos *"duros"* y simulación condensada para eventos *"blandos"*.

---

## PENELOPE

* PENGEOM
	- Paquete de geometrías que permite la generación de lluvias aleatorias electrón-fotón.
	- Se realiza sobre cuerpos de materiales homogéneos limitados por superficies cuadráticas (planos, esferas, cilindros, etc.).
* Manual: ```doc/penelope-2008.pdf````
	- Manual del código PENELOPE.
	- Detalle sobre bases y teoría de los algoritmos de simulación Monte Carlo.

---

## Consideraciones

* La simulación del transporte de electrones y positrones es mucho más difícil que en el caso de los fotones
* En una interacción de un electrón, la energía perdida es muy baja (decenas de eV)
* Los $e^{-}$ de alta energía entonces sufren una gran cantidad de interacciones antes de ser finalmente absorbidos
* La simulación detallada es eficiente solo cuando el número medio de interacciones por *track* no es muy grande (algunos cientos)
* Para $e^{-}$ y $e^{+}$ de alta energía la mayoría de los códigos de simulación MC recurre a teorías de *multiple-scattering*
* Esto permite la simulación del efecto global de un gran número de eventos en un segmento de camino
* Por Berger (1963) estos procedimientos de simulación son conocidos como métodos MC "condensados"

---

## Simulación *"condensada"*

* Las teorías de *multiple-scattering* implementadas en algoritmos de simulación condensada son solo aproximadas y pueden llevar a errores sistemáticos
* Esto se hará evidente por la dependencia de los resultados buscados en la longitud del paso adoptado (Bielajew y Rogers, 1987)
* Para analizar esto, se pueden hacer hacer simulaciones del mismo arreglo cambiando el tamaño del paso
* Los resultados suelen estabilizarse al disminuir el paso, creciendo rápidamente el costo computacional
* Dependiendo de los algorimos utilizados, achicar mucho el paso puede llevar también a resultados falsos

---

## Simulación *"condensada"*

* Por ejemplo, la teoría de *multple-elastic-scattering* de Molière no es aplicable para longitudes de paso menores a algunas veces el camino libre medio elástico
* En este caso se debe desactivar la dispersión elástica múltiple
* Por esto, la estabilización de los resultados al acortar el paso elegido, no implica que los resultados sean correctos.
* Los algoritmos de condensación también presentan problemas en la generación de *tracks* de partículas en las cercanías de una interfaz
* En las cercanías de una interfaz, el paso debe mantenerse menor que la distancia a esta interfaz que separa dos medios

---

## PENELOPE

* PENELOPE simula el transporte acoplado electrón-fotón
* El algoritmo de simulación se basa en un modelo de *scattering* que combina bases de datos numéricas con modelos de secciones eficaces analíticas para diferentes mecanismos de interacción
* El transporte de $e^{-}$ y $e^{+}$  es realizado por un procedimiento mixto:
	- las interacciones duras, con ángulo de *scattering* $\theta$ y pérdida de energía $W$ mayor que los pre-seleccionados $\theta_c$ y $W_c$, se realizan de forma detallada
	- las interacciones blandas con $\theta < \theta_c$ y $W<W_c$ son descriptas por aproximaciones de *multiple-scattering*
	- Las simulaciones son bastante estables ante cambios de $\theta_c$ y $W_c$ y las mismas deben ser utilizadas para acelerar el tiempo de cómputo sin alterar los resultados

---

## PENELOPE. 

* La ionización de las capas internas por impacto de $e^{-}$ y $e^{+}$ se describe utilizando bases de datos numéricas de secciones eficaces totales para capas K, L y M, calculadas por la teoría descripta por Bote y Salvat (2008)
* Se incluyen efectos de polarización de fotones en *scattering* Rayleigh y Compton
* El paquete incluye dos ejemplos de programas principales: ```pencil``` (para transporte en geometrías cilíndricas y ```penmain``` (para transporte en geometrías cuadráticas
* Se permiten fuentes extendidas, polarización de fotones y cálculo de distribuciones de energía de una fluencia media en cuerpos seleccionados
* Se cuenta con un visualizador de geometrías para simplificar (solo Windows)

---

## Distribución PENELOPE 2008

* ```Sub material/```: algunos materiales de ejemplo
* ```doc/```: manuales y tutoriales
* ```fsource/```: archivos fuente principales para simulación
* ```mains/```: *"mains"* de PENELOPE ```pencyl``` y ```penmain```, y ejemplos
* ```other/```: ```emfield/```,  ```gview/```, ```shower.exe``` y ```tables/```
* ```pendbase```: crear tablas y materiales

