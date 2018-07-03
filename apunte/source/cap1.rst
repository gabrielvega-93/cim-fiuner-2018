Procesos estocásticos
=====================

El *Capítulo* está dedicado a los elementos básicos sobre
procesos estocásticos. Se introducen conceptos generales,
consideraciones estadísticas y fenómenos físicos de carcácter
intrínsecamente aleatorio. Se dedica especial atención al transporte de
radiación en su característica estocástica.


Introducción y definiciones de procesos estocásticos
----------------------------------------------------

En los procesos estocásticos se representan los pasos necesarios para
la realización de un cierto evento, así como también los maneras en que
cada uno de los pasos puede ser realizado en términos de las respectivas
probabilidades. Por tanto, cualquier proceso en el que se vean
involucradas probabilidades de ocurrencia resulta ser un proceso
estocástico.

Al describir variables de carácter aleatorio, vinculadas a fenómenos de
tipo probabilísticos como lo es el transporte de radiación, es asumido,
como premisa implícita por defecto, el hecho de que las características
aleatorias permanecen constantes durante el intervalo de tiempo de
interés, aunque desde una perspectiva genérica podría no satisfacerse
esta asumpción.

En efecto, al incorporar la dependencia (o evolución) de variables
consideradas determinísticas, éstas describirán un proceso evolutivo de
tipo analítico, mientras que para el caso de variables aleatorias
mostrarán una evolución condicionada por el vínculo al fenómeno
probabilístico asociado. Entonces, toda función definida a partir de
variables aleatorias, como por ejemplo funciones de distribución o
funciones de densidad, presentarán dependencia temporal determinada por
su carácter aleatorio, dando lugar a la naturaleza estocástica del
fenómeno físico involucrado.

Una definición más formal de un proceso estocástico es la siguiente:

*El proceso estocástico consiste en el conjunto (o familia) de variables
aleatorias* :math:`\{X_{t} \, t \in [t_{ini}, t_{fin}]\}` *que se ordenan de
acuerdo con el índice* :math:`t` *, por lo general identificando al
tiempo.*

En consecuencia, se tiene que para cada valor de :math:`t` (instante)
existe la variable aleatoria representada por :math:`X_{t}`, de modo que
el proceso estocástico puede interpretarse como una sucesión de
variables aleatorias, las que pueden variar (evolucionar) en sus
características.

Los *estados de variables aleatorias* son los posibles valores que éstas
pueden asumir. Por lo tanto, existe un *espacio de estados* asociados a
las variables aleatorias. En particular, la variable temporal :math:`t`
puede ser de tipo discreto o bien de tipo continuo. La modificación de
la variable :math:`t`, por ejemplo, daría lugar a cambios de estado que
ocurren en el instante :math:`t`.

Por tanto, de acuerdo con el conjunto de índices [1]_
:math:`t \in T=[t_{ini}, t_{fin}]`, la variable aleatoria :math:`X_{t}`
puede clasificarse según los siguientes criterios para procesos
estocásticos:

-  Si el conjunto :math:`T` es continuo (por ejemplo :math:`\Re^{+}`),
   resulta que :math:`X_{t}` describe un proceso estocástico de
   parámetro continuo.

-  Si el conjunto :math:`T` es dicreto, :math:`X_{t}` describe un
   proceso estocástico de parámetro discreto.

-  Si para cada valor (instante) :math:`t` la variable aleatoria
   :math:`X_{t}` es de tipo continuo, resulta que proceso estocástico es
   de estado continuo.

-  Si para cada valor (instante) :math:`t` la variable aleatoria
   :math:`X_{t}` es de tipo discreto, resulta que proceso estocástico es
   de estado discreto.

Una *cadena* es un proceso estocástico para el cual el tiempo evoluciona
de manera discreta y la variable aleatoria sólo puede tomar valores
discretos en el espacio de estados correspondiente.

Un *proceso de saltos puros* es un proceso estocástico para el cual los
cambios de estados suceden de forma aislada y aleatoria pero la variable
aleatoria sólo asume valores discretos en el espacio de estados
correspondiente. Diversamente, un *proceso continuo* se refiere al caso
en que los cambios de estado se producen para cualquier valor de
:math:`t` (instante) y hacia cualquier estado dentro de un espacio
continuo de estados correspondiente.

Procesos de estado discreto y cadenas de Markov
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

En el caso de procesos estocásticos con espacio de estados discreto, una
secuencia de variables que indique el valor del proceso en instantes
sucesivos [2]_ puede representarse del siguiente modo:

.. math::

   \begin{aligned}
       \{ X_{0} = x_{0}, X_{1} = x_{1}, ... , X_{n} = x_{n} \}
   \label{EqLXXXIV}\end{aligned}

donde cada variable :math:`X_{j} \, \: j \in [1, n]` presenta una
distribución de probabilidades tal que, en general, es diferente de las
otras variables aunque podría haber características comunes.

Uno de los principales objetivos del estudio del caso discreto es el
cálculo de probabilidades de ocupación de cada estado a partir de las
probabilidades de cambio de estado. Si para el valor :math:`t_{j-1}`
(instante) el sistema está en el estado :math:`x_{j-1}`, la probabilidad
de que al instante siguiente :math:`t_{j}` se encuentre en el estado
:math:`x_{j}` se obtiene a partir de la probabilidad de transición o
cambio de estado de :math:`x_{j-1}` a :math:`x_{j}` (o probabilidad
condicionada) denotada por
:math:`P\left( X_{j} = x_{j} / X_{j-1} = x_{j-1} \right) = P_{j, j-1}`,
donde :math:`P_{j, j-1}` es el valor que asume la probabilidad para el
caso específico en consideración.

Las probabilidades del tipo :math:`P \left( X_{j} = x_{j} \right)` se
denominan probabilidades de ocupación de estado.

De modo similar, otro tipo de probabilidad de interés es la de ocupar un
cierto estado en un instante :math:`t_{j}`, dado que en todos los
instantes anteriores, desde :math:`t_{ini}` a :math:`t_{j-1}` se conoce
en qué estados estuvo el proceso. En este caso, la probabilidad
condicionada es
:math:`P \left( X_{j} = x_{j} / X_{ini} = x_{ini}, \, ... , \, X_{j-1} = x_{j-1} \right) =
P_{ini, ..., j-1, j}`

Por tanto, la probabilidad :math:`P_{ini, ..., j-1, j}` depende de toda
la “historia pasada del proceso”, mientras que la probabilidad de
transición depende únicamente del estado actual que ocupe el proceso.

**Propiedad de Markov:**

Se dice que un proceso cumple la propiedad de Markov cuando toda la
historia pasada del proceso se puede resumir en la posición actual que
ocupa el proceso para poder calcular la probabilidad de cambiar a otro
estado. Es decir, se cumple:

.. math::

   \begin{aligned}
       P \left( X_{j} = x_{j} / X_{ini} = x_{ini}, \, ... , \, X_{j-1} = x_{j-1} \right) =
       P \left( X_{j} = x_{j} /  X_{j-1} = x_{j-1} \right)
   \label{EqLXXXVII}\end{aligned}

Además, una propiedad importante que puede tener una cadena es que los
valores :math:`p_{mn} (j)` no dependan del valor de :math:`j`. Entonces,
se tiene que las probabilidades de cambiar de estado son las mismas en
cualquier instante. Por lo tanto, esta propiedad indica que las
probabilidades de transición son estacionarias.


Procesos de saltos puros
~~~~~~~~~~~~~~~~~~~~~~~~

En este caso, el proceso sigue siendo discreto en estados pero la gran
diferencia es que los cambios de estado ocurren en cualquier instante en
el tiempo (tiempo continuo).

Un proceso estocástico en tiempo continuo :math:`\{ N(t) \, t \ge 0 \}`
se denomina *proceso de conteo* si representa el número de veces que
ocurre un suceso hasta el instante de tiempo :math:`t`.

En particular, se tiene :math:`N(t) \in \mathbf{N}` y
:math:`N(t^*) \le N(t) \, \; \forall t^* < t`.

Un proceso de conteo es un *proceso de Poisson homogéneo* de tasa
:math:`\lambda` si satisface:

#. :math:`N(0) = 0`

#. :math:`N(t_{k}) - N(t_{k-1})` es una variable aleatoria independiente
   (proceso de incrementos independientes) :math:`\forall \, k`.

#. :math:`N(t + t^*) - N(t^*)`, que denota la cantidad de eventos que
   ocurren entre el instante :math:`t^*` y :math:`t`, sigue una
   distribución de Poisson de parámetro :math:`\lambda t`.


Procesos de estados continuos y series temporales
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Un concepto importante en procesos estocásticos es la *realización*, o
bien una realización de una experiencia aleatoria, que es el resultado
de una repetición de esa experiencia. Por tanto, en la experiencia
aleatoria de “lanzar una vez un dado” una realización posible sería
obtener el número 2, en el único lanzamiento hecho. En ese caso, la
realización se reduce a un único número :math:`\{X\}`. Si se repite la
experiencia, podrían obtener otras realizaciones (cualquiera de los
números 1, 3, 4, 5 y 6).

En una experiencia :math:`M`-dimensional, una realización es el
resultado obtenido de los :math:`M` parámetros, denotado por
:math:`\{X_{1}, ..., X_{M} \}`.

Una *serie temporal* es una realización parcial de un proceso
estocástico de parámetro tiempo discreto. De aquí que la teoría de los
procesos estocásticos es de aplicación a las series temporales. Sin
embargo, existe una fuerte restricción que radica en el hecho de que en
muchas series temporales, ellas son la única realización observable del
proceso estocástico asociado.


Características y medidas de procesos estocásticos
--------------------------------------------------

Para un espacio de estados :math:`M`-dimensional, pueden calcularse
cantidades y medidas estadísticamente representativas para los estados
descritos por las variables :math:`M`-dimensionales. En particular, se
definen -entre tantos- medidas como tensores de valor medio y de
covarianzas, que permiten obtener características representativas de los
procesos estocástico.


Procesos estocásticos estacionarios
-----------------------------------

En primera aproximación, se considerarán estacionarios a los procesos
estocásticos que tengan un comportamiento constante a lo largo del
tiempo.

Un *proceso estocástico estacionario en sentido estricto* requiere que
al realizar un mismo desplazamiento en el tiempo de todas las variables
de cualquier distribución conjunta finita se obtenga que esta
distribución no varía. Es decir:

.. math::

   \begin{aligned}
       F \left( X_{i_1}, ... , X_{i_M} \right) =   F \left( X_{i_1 + j}, ... , X_{i_M + j} \right) \: \, \forall i_k , \, j
   \label{EqLXXXVIII}\end{aligned}

En cambio, un *proceso estocástico esestacionario en sentido débil*
requiere que se mantengan constantes todas sus características lo largo
del tiempo. Es decir, que :math:`\forall t`:

#. :math:`\langle X_t \rangle = \langle X \rangle \; \, \forall t` donde
   :math:`\langle X \rangle` denota el valor medio o de expectación.

#. :math:`\sigma_{X_t}  = \sigma_{X} \; \, \forall t` donde
   :math:`\sigma_{X}` denota la varianza.

#. :math:`Cov \left( t, t+j \right) = Cov \left( t^*, t^*+j \right) = C_{j} \, \; \forall j = 0, \pm 1, \pm 2, ...`
   donde :math:`Cov` denota la covarianza y :math:`C` es una constante.


Procesos de ruido blanco
~~~~~~~~~~~~~~~~~~~~~~~~

Un proceso estocástico utilizado frecuentemente es el de “ruido blanco”,
dado por el proceso estacionario :math:`RB_{t}` que satisface:

-  :math:`\langle RB_{t} \rangle = \langle RB \rangle = 0  \, \: \forall t`

-  :math:`Var(RB_{t}) = \sigma^2`

-  :math:`Cov(RB_{t}, RB_{t^*}) = 0 \; \, t^* \ne t`

En este sentido, puede interpretarse al ruido blanco como una sucesión
de valores sin relación alguna entre ellos, oscilando en torno al cero
dentro de un margen constante. En este tipo de procesos, conocer valores
pasados no proporciona ninguna información sobre el futuro ya que el
proceso es “puramente aleatorio”, y por consiguiente “carece de
memoria”.


El transporte de radiación como proceso estocástico
---------------------------------------------------

En la simulación del transporte de radiación por método Monte Carlo, la historia (*track*) de una partícula es vista como una sucesión aleatoria de secuencias de *vuelos* libres que terminan con un evento de interacción donde la partícula puede cambiar su estado (dirección de movimiento y energía cinética) e incluso puede llegar a generar partículas secundarias.

La simulación del transporte de un dado experimento (por ejemplo, un fotón/electrón ingresando en un fantoma de agua) consiste en la generación de historias random. Para realizar esta simulación, es necesario un "*modelo de interacción*", por ejemplo un set de secciones eficaces diferenciales (DCS) para los mecanismos de interacción relevantes o más importantes. Estas DCS determinan las funciones de distribución de probabilidad (PDFs) de las variables random que caracterizan la historia:

1. camino libre entre eventos de interacción sucesivos
2. tipo de interacción que se realiza
3. pérdida de energía y deflexión angular en cada evento
4. *estado inicial de las partículas secundarias emitidas*, si corresponde
   
Una vez conocidas las PDFs, las historias pueden ser generadas por medio del uso de métodos de sampleo apropiados. Si el número de historias generadas es lo suficientemente grande, la información cuantitativa del proceso de transporte puede ser obtenida del cálculo de la media de las historias simuladas.

El método Monte Carlo provee la misma información que la ecuación de transporte de Boltzmann, con el mismo modelo de interacción pero más fácil de implementar (Berger, 1963). En particular, la simulación del transporte de radiación en geometrías complejas es fácil de obtener (pagando costo computacional razonable), mientras que el transporte en una simple geometría finita es muy difícil de modelar con la ecuación de transporte.

La desventaja del método Monte Carlo reside en su naturaleza estocástica, ya que todos los resultados se ven afectados por incerteza estadística, pero esta puede ser reducida al precio del costo computacional. En algunas circunstancias especiales, las incertezas estadísticas pueden ser reducidas por medio del uso de técnicas de reducción de varianzas (Rubinstein, 1982; Bielajew y Rogers, 1988).

Elementos de teoría de probabilidad
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

La probabilidad de que una variable aleatoria :math:`x` que toma valores en :math:`x_{min} < x < x_{max}` obtenga valores en el intervalo :math:`(a,b)` queda determinada por :math:`P\{x|a<x<b\}` definido por :math:`n/N` donde :math:`n` es el número de veces que obtuvo un valor en el intervalo y :math:`N` el número total de valores generados cuando :math:`N\rightarrow\infty`.

Ahora bien, la probabilidad de obtener :math:`x` en un intervalo diferencial :math:`dx` alrededor de :math:`x_1` puede ser expresada entonces como

.. math::
   
   P\{x | x_1 < x < x_1 + dx\} = p(x_1) dx

donde :math:`p(x)` es la PDF de :math:`x`.

Como la probabilidad debe ser una cantidad no nula y los valores de :math:`x` deben encontrarse en el intervalo :math:`(x_{min},x_{max})`, la PDF debe ser definida positiva y normalizada a la unidad:

.. math::
   
   p(x) \geq 0 \text{   y   } \int_{x_{min}}^{x_{max}} p(x)dx = 1

y toda función que satisfaga esta condición puede ser considerada una PDF.

En simulaciones Monte Carlo se utiliza mucho la distribución normal:

.. math::
   
   U_{x_{min}, x_{max}} (x) \equiv \left\{ 
                                    \begin{array}{lc}
                                    1/(x_{max} - x_{min}) & si x_{min} \leq x \leq x_{max} \\
                                    0                     & x < x_{min} \,\,\, \text{o} \,\,\, x_{max} < x
                                    \end{array}
                                   \right.

Esta definición incluye distribuciones como la función de Dirac, e incluso una PDF de una variable random :math:`x` que puede tomar valores discretos :math:`x = x_1, x_2, ...` con probabilirades :math:`p_1, p_2, ...` puede ser expresada como una suma de distribuciones delta.

Dada una variable :math:`x`, la función de distribución acumulativa de :math:`x` queda expresada por:

.. math::
   
   \mathcal{P}(x) \equiv \int_{x_{min}}^x p(x') dx

la cual constituye una función creciente que varía de 0 a 1. En el caso de las PDF discretas es una función tipo escalera.

El momento n-ésimo de :math:`p(x)` se define como 

.. math::
   
   \langle x^n\rangle \equiv \int_{x_{min}}^{x_{max}} x^n p(x)

Lo que muestra que :math:`\langle x^0\rangle`, es la integral de :math:`p(x)`, que es igual a 1. Después, el primer momento (si existe) es conocido como valor madio o de expectancia. Si además existe el segundo momento, podemos definir la varianza :math:`var(x) = \langle(x - \langle x \rangle)^2\rangle`, mientras que la desviación estándar se conoce como la raíz cuadrada de la varianza.



Reformulación integral de la ecuación de transporte
---------------------------------------------------

A partir de la expresión íntegro-diferencial de la ecuación de
transporte de Boltzmann

.. image:: 1.png
    :width: 200px
    :align: center

es posible reformular los términos para arribar a una ecuación completamente integral, lo cual
resulta de particular utilidad para el manejo de soluciones de tipo
numéricas, necesarias para situaciones realistas, ya que -como se sabe-
las soluciones analíticas directas sólo son posibles en una cantidad
miuy limitada de configuraciones.

Operando y reordenando los términos en la ecuación de Boltzmann resulta:

.. math::

   \begin{aligned}
    t = t_{0} + \frac{s}{\lvert\vec{v}\rvert}       \nonumber \\
    \vec{r} = \vec{r_{0}} + s\, \vec{\Omega}
    \label{EcXI}\end{aligned}

Por lo tanto, se obtiene:

.. math::

   \begin{aligned}
       \frac{d}{d s} \, \Psi \left( \vec{r_{0}} + s \vec{\Omega}, \vec{\Omega}, E, t_{0} +\frac{s}{\lvert\vec{v}\rvert}  \right) +
       \Sigma \; \Psi \left( \vec{r_{0}} + s \vec{\Omega}, \vec{\Omega}, E, t_{0} +\frac{s}{\lvert\vec{v}\rvert} \right)
       = \\
       \Gamma \left( \vec{r_{0}} + s \vec{\Omega}, \vec{\Omega}, E, t_{0} +\frac{s}{\lvert\vec{v}\rvert} \right)
    \label{EqXII}\end{aligned}

donde se ha definido
:math:`\Gamma \left( \vec{r_{0}} + s \vec{\Omega}, \vec{\Omega}, E, t_{0} +\frac{s}{\lvert\vec{v}\rvert} \right)`
como sigue:

.. math::

   \Gamma \equiv S + \iint \, \Sigma _{s} \left( \vec{r_{0}} + s \vec{\Omega}, (\vec{\Omega'}, E') \rightarrow (\vec{\Omega}, E)  \right)
       \Psi \left( \vec{r_{0}} + s \vec{\Omega}, \vec{\Omega'}, E', t_{0} +\frac{s}{\lvert\vec{v}\rvert}  \right) \, \, d \, \vec{\Omega'} \, d \, E'

Puede verse [3]_

.. math::

   \Psi \left( \vec{r_{0}}, \vec{\Omega}, E, t_{0} \right) = \int  _{-\infty} ^{0} \, \: ds \left[ e^{ \int _{0} ^{s}
       \Sigma \left( \vec{r_{0}} - s' \vec{\Omega}, E \right) \, ds' }  \; \:
       \Gamma \left( \vec{r_{0}} + s \vec{\Omega}, \vec{\Omega}, E, t_{0} +\frac{s}{\lvert\vec{v}\rvert} \right) \right]

Considerando que las variables :math:`\vec{r_{0}}` y :math:`t_{0}` son
arbitrarias, se obtiene:

.. math::

   \begin{aligned}
       \Psi \left( \vec{r}, \vec{\Omega}, E, t \right) =   %\nonumber \\
        \int  _{0} ^{\infty} \, \: e^{ \int _{0} ^{s} \Sigma \left( \vec{r_{0}} - s' \vec{\Omega}, E \right) \, ds' }  \; \cdotp \; \: \nonumber \\
       \left[ \iint \Sigma_{s} \left( \vec{r} - s \vec{\Omega}, (\vec{\Omega'}, E') \rightarrow (\vec{\Omega}, E)  \right)
       \Psi \left( \vec{r} - s \vec{\Omega}, \vec{\Omega}, E, t - \frac{s}{\lvert\vec{v}\rvert} \right) %\nonumber \\
       +  S \left( \vec{r} - s' \vec{\Omega}, \vec{\Omega}, E, t  \right)  \right]
           %\right]
   \end{aligned}

Es decir, se obtuvo una forma integral para la ecuación de Boltzmann,
que puede escribirse en término de operadores [4]_:

.. math::

   \Psi = \mathbf{K} \; \Psi + S'
    \label{EqXVI}

Se obtiene la solución para el flujo:

.. math::

   \Psi = \Sigma _{i=0} ^{\infty} \Psi_{i}
    \label{EqXVII}

Donde los términos son:

.. math::

   \begin{aligned}
       \Psi_{i} = \mathbf{K} \; \Psi_{i-1} \nonumber \\
       \Psi_{0} = S'
    \label{EqXVIII} \end{aligned}

Matemáticamente, la solución obtenida se denomina serie de von Neuman.
La interpretación física del formalismo desarrollado es particularmente
apropiada en el vínculo entre los términos de la serie y los procesos
físicos involucrados. El término de orden 0 se refiere al flujo primario
estrictamente proveniente de la fuente de emisión :math:`S`, mientras
que los términos :math:`\Psi_{i}` son las contribuciones de *scattering*
a orden :math:`i` obtenidas a partir del operador del *kernel de
scattering* :math:`\mathbf{K}`.

.. [1]
   Estrictamente, subíndices.

.. [2]
   Se asume que la variable :math:`t` refiere al tiempo.

.. [3]
   Introdúzcase
   :math:`e^{ \int _{-\infty} ^{s} \, \, \Sigma \left( \vec{r_{0}} + s' \vec{\Omega}, E \right) \, \, ds'}`
   y calcúlese :math:`\frac{d}{d s} \Psi` .

.. [4]
   Resulta conveniente expresar la ecuación de este modo para la
   resolución numérica de la misma, por ejemplo utilizando métodos
   estadísticos como Monte Carlo.
