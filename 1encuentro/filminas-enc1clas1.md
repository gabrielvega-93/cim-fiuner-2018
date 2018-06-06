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

* Las características aleatorias permanecen permanecen constantes en el intervalo de tiempo de interés

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
* Si para cada instante $t$, $X_t$ es una variable discreta, entonces describe un procesos estocástico de estado discreto

---

##### Cadena

Proceso estocástico en el cual el tiempo evoluciona de manera discreta y la variable aleatoria solo puede tomar valores discretos en el espacio de estados.

##### Proceso de saltos puros

Proceso estocástico para el cual los cambios de estados suceden de forma aislada y aleatoria pero la variable aleatoria sólo asume valores discretos en el espacio de estados correspondiente

##### Proceso continuo

Los cambios de estado se producen para cualquier valor de (instante) $t$ y hacia cualquier estado dentro de un espacio continuo de estados correspondiente

---

##### Procesos de estado discreto y cadenas de Markov

$$\{ X_{0} = x_{0}, X_{1} = x_{1}, ... , X_{n} = x_{n} \}$$

donde $X_j: j \in [1,n]$ presenta una distribución de probabilidades (generalmente) diferente al de las otras variables

