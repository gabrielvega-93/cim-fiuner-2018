# Análisis y procesamiento de imágenes radiológicas en el ámbito médico

## Procesos estocásticos

#### P. Pérez

###### FAMAF (UNC) & IFEG (CONICET)

---

##### Procesos estocásticos

*"...concepto matemático que sirve para usar magnitudes aleatorias que varían con el tiempo o para caracterizar una sucesión de variables aleatorias (estocásticas) que evolucionan en función de otra variable"*

**<div style="text-align: right">La wiki</div>**


##### El método Monte Carlo

*"Monte Carlo numerical simulation methods can be described as statistical methods that use random numbers as a base to perform simulation of any specified situation."*

<div style="text-align: right"><b>M. Ljungberg</b><br><i>Monte Carlo simulations in Nuclear Medicine</i></div>

---

##### Qué sucede en un proceso estocástico?

* Se representan los pasos necesarios para la realización de un evento
* Se representan las maneras en las que cada paso puede ser realizado

##### Por tanto

* Cualquier proceso en el que se vean involucradas probabilidades de ocurrencia resulta un proceso estocástico

---

##### Asumpciones en transporte de radiación

* Las características aleatorias permanecen constantes en el intervalo de tiempo de interés

##### Una definición más formal

*El proceso estocástico consiste en el conjunto (o familia) de variables
aleatorias $\{X_{t}: \, t \in [t_{ini}, t_{fin}]\}$ que se ordenan de acuerdo con el índice $t$, por lo general identificando al tiempo.*

$\therefore$

para cada valor de $t$ existe una variable aleatoria $X_t$, por lo que el proceso estocástico puede interpretarse como sucesión de variables aleatorias, **que pueden evolucionar en sus características**.

---

##### Algunas definiciones

* **estados de variables aleatorias:** posibles valores que pueden asumir
* existe un **espacio de estados** asociado a las variables aleatorias
* $t$ puede ser de tipo discreto o continuo
* la variación de $t$ pueden dar lugar a cambios de estados que ocurren en el instante $t$

---

##### Entonces

Para $t \in T = \{t_{ini}, t_{fin}\}$, $X_t$ puede clasificarse para procesos estocásticos:

* Si $T$ es continuo, $X_t$ describe un proceso estocástico de parámetro contínuo
* Si $T$ es discreto, $X_t$ describe un proceso estocástico de parámetro discreto
* Si para cada instante $t$, $X_t$ es una variable contínua, entonces describe un procesos estocástico de estado continuo
* Si para cada instante $t$, $X_t$ es una variable discreta, entonces describe un proceso estocástico de estado discreto

---

##### Cadena

Proceso estocástico en el cual el tiempo evoluciona de manera discreta y la variable aleatoria solo puede tomar valores discretos en el espacio de estados.

##### Proceso de saltos puros

Proceso estocástico para el cual los cambios de estados suceden de forma aislada y aleatoria pero la variable aleatoria sólo asume valores discretos en el espacio de estados correspondiente

##### Proceso continuo

Los cambios de estado se producen para cualquier valor de (instante) $t$ y hacia cualquier estado dentro de un espacio continuo de estados correspondiente

---

##### Procesos de estado discreto y cadenas de Markov

En procesos estocásticos con espacio de estados discreto, la secuencia de variables que indique el valor del proceso en instantes sucecivos puede representarse por

$$\{ X_{0} = x_{0}, X_{1} = x_{1}, ... , X_{n} = x_{n} \}$$

donde $X_j: j \in [1,n]$ presenta una distribución de probabilidades (generalmente) diferente al de las otras variables.

Uno de los principales objetivos del estudio de este tipo de casos es el del cálculo de probabilidades de ocupación de cada estado a partir de probabilidades de cambio de estado.

Si para $t_{j-1}$ el proceso está en el estado $x_{j-1}$, la probabilidad de que para $t_j$ esté en $x_j$ se obtiene a partir de la probabilidad de transición $P(X_j = x_j / X_{j-1} = x_{j-1}) = P_{j,j-1}$. Las probabilidades de tipo $P(X_j = x_j)$ se denominan <span style="color: blue">probabilidades de ocupación de estado</span>.

---

##### Procesos de estado discreto y cadenas de Markov

Otro tipo de probabilidad de interés es el de ocupar un estado $x_j$ en el instante $t_j$ dado que se conocen todos los otros estados anteriores $\{x_{ini}, ..., x_{j-1}\}$. En este caso la probabilidad condicionada es $P(X_j = x_j/ X_{ini} = x_{ini}, ..., X_{j-1} = x_{j-1}) = P_{ini, ..., j-1}$.

$\therefore P_{ini, ..., j-1}$ depende de la "*historia*" del proceso.

Mientras que la probabilidad de transición depende *solo del estado actual*.

---

##### Propiedad de Markov

Se da cuando toda la historia pasada del proceso se puede resumir en la posición actual para poder calcular el paso a otro estado.

$$ P_{ini, ..., j-1} = P_{j,j-1}$$

Además, una propiedad importante que puede tener una cadena de Markov es que <span style="color: blue">los valores de la probabilidad de cambiar de estado son estacionarias</span>. Es decir, quelos valores $p_{mn}(j)$ no dependen de $j$.

---

##### Procesos de saltos puros

el proceso sigue siendo discreto en estados pero la gran diferencia es que los cambios de estado ocurren en cualquier instante en el tiempo (<span style="color: blue">tiempo continuo!</span>)

Un proceso estocástico en tiempo continuo $\{N(t) : t \geq 0\}$ se denomina proceso de conteo si representa el número de veces que ocurre un suceso hasta el instante de tiempo t.

En particular, se tiene $N(t) \in N$ y $N(t^{*}) \leq N(t) \, \forall \, t^{*} < t$.

---

##### Procesos de saltos puros

Un proceso de conteo es un proceso de Poisson homogéneo de tasa $\lambda$ si satisface:

1. $N(0) = 0$
2. $N(t_k) - N(t_{k-1})$ es una variable aleatoria independiente $\forall k$
3. $N(t + t^*) - N(t^*)$, que denota la cantidad de eventos que ocurren entre el instante $t^*$ y $t$, sigue una distribución de Poisson de parámetro $\lambda t$

---

##### Procesos de estados continuos y series temporales

* La *realización* de una experiencia es el resultado de una repetición de la experiencia.
* En la experiencia aleatoria de “lanzar una vez un dado” una realización posible sería obtener el número 2, en el único lanzamiento hecho.
	- En ese caso, la realización se reduce a un único número $\{X\}$.
	- Si se repite la experiencia, podrían obtener otras realizaciones (1, 3, etc).
* En una experiencia M-dimensional, una realización es el resultado obtenido de los M parámetros, denotado por $\{X_1,...,X_M\}$.
* Una serie temporal es una realización parcial de un proceso estocástico de parámetro tiempo discreto.

---

##### Características y medidas de procesos estocásticos

* Para un espacio de estados M-dimensional, pueden calcularse cantidades y medidas estadísticamente representativas para los estados descritos por las variables M-dimensionales. 
* En particular, se definen -entre otros- medidas como tensores de valor medio y de covarianzas, que permiten obtener características representativas de los procesos estocásticos.

---

##### Procesos estocásticos estacionarios

En primera aproximación, se considerarán estacionarios a los procesos estocásticos que tengan un comportamiento constante a lo largo del tiempo.

Un proceso estocástico **estacionario en sentido estricto** requiere que al realizar un mismo desplazamiento en el tiempo de todas las variables de cualquier distribución conjunta finita se obtenga que esta distribución no varía. Es decir:

$$F(X_{i_1},..., X_{i_M}) = F(X_{i_{1}+j}, ..., X_{i_{M}+j}) \, \forall i_k,j$$

---

##### Procesos estocásticos estacionarios

En cambio, un proceso estocástico **estacionario en sentido débil** requiere que se mantengan constantes todas sus características a lo largo del tiempo. Es decir, que $\forall$:

1. $\langle X_t\rangle = \langle X\rangle \, \forall t$ donde $\langle X\rangle$ es el valor medio o de expectación
2. $\sigma_{X_t} = \sigma_{X} \, \forall t$ donde $\sigma_{X}$ representa la varianza
3. $Cov(t, t+j) = Cov(t^*, t^*+j) = C_j \, \forall j = 0, \pm1, \pm2, ..$ donde $Cov$ es la covarianza y $C$ una constante

---

##### Procesos de ruido blanco

Un proceso estocástico utilizado frecuentemente es el de “ruido blanco”, dado por el proceso estacionario $RB_t$ que satisface:

* $\langle RB_t\rangle = \langle RB\rangle = 0 \, \forall t$
* $Var(RB_t) = \sigma^2$
* $Cov(RB_t,RB_{t^*})=0$ si $t^* \neq t$

En este sentido, puede interpretarse al ruido blanco como una sucesión de valores sin relación alguna entre ellos, oscilando en torno al cero dentro de un margen constante. 

En este tipo de procesos, conocer valores pasados no proporciona ninguna información sobre el futuro ya que el proceso es “puramente aleatorio”, y por consiguiente “carece de memoria”.