# Análisis y procesamiento de imágenes radiológicas en el ámbito médico

## Introducción al método Monte Carlo

#### P. Pérez

###### FAMAF (UNC) & IFEG (CONICET)

---

### un poco de historia...

* la física históricamente ha sido conocida como *filosofía natural* y su estudio ha sido através de investigación puramente teórica
	- progreso "verdadero" limitado por la falta de conocimiento real
	- casi imposible determinar cuando una teoría aplicaba realmente a la naturaleza
* la investigación aplicada se convirtió en la forma aceptada de investigación
	- limitada a la capacidad de los físicos para preparar una muestra para un estudio
* con el advenimiento de la computadora, se pudieron llevar a cabo simulaciones de situaciones reales modeladas
	- la capacidad de cálculo actual permitió el mejoramiento de los modelos de las condiciones naturales de forma realista

---

### simulaciones

* gracias a las computadoras, las simulaciones en física se convirtieron en una nueva forma de investigación
	- en muchos casos las simulaciones proveen las bases teóricas para el entendimiento de los resultados experimentales
	- en otros casos, las simulaciones proveen datos "*experimentales*" que permiten contrastar y mejorar la teoría

---

### simulaciones en radiación ionizante

* la ec. de transporte de Boltzmann es una ecuación integro-diferencial sin solución analítica para casos generales
* se puede estimar una solución numérica
* resolver la ec. de forma computacional permite explorar experimentos en una computadora personal que no serían posibles de realizar en situaciones de laboratorio 

---

### Monte Carlo

* técnica que utiliza números aleatorios (*random*) para resolver problemas
* el primer trabajo a gran escala data de mediados de s. XX
	- estudios de multiplicación, *scattering*, propagación y absorción de neutrones en un medio, o saliendo de él
	- Ulam, von Neumann y Fermi <- <span style="color:red">los primeros!</span>
	- se resolvieron por primera vez problemas prácticos de transporte
	- para la bomba!
* el término proviene de la afición de los físicos al juego por plata
* antes ya lo habían usado a mediados de s. XIX para calcular $\pi$
	- fue Buffon!
---

### En la física?

* las bolas de Galton
	- fines de s. XIX
	- bolas cayendo sobre un arreglo de puntos
	- los puntos dispersando las bolas aleatoreamente
	- bolas colectadas en compartimentos verticales abajo
	- la altura de las bolas en los compartimentos aproximan la **distribución binomial**
	- constituye una demostración del *Teorema Central del Límite*
* Pearson usó números aleatorios en los 20's para resolver problemas complejos de probabilidad y estadística
	- primeras tablas de números aleatorios!

---

### Un poco más...

* Kelvin propone descripción de técnicas Monte Carlo modernas (hace 100 años!) para discutir las ecuaciones de Boltzmann
	- pero Kelvin estaba más preocupado por los resultados que por la técnica!
* la técnica deriva de un juego popular en Mónaco (o del casino dicen algunos)
	- los niños tiraban piedritas, en la playa, sobre un cuadrado que tenía un círculo dibujado adentro, de forma aleatoria
	- de la fracción de piedritas que caen en el cículo se puede inferir $\pi$
	- otros afirman que el nombre proviene de la afición de unos físicos por calcular probabilidades de triunfo en el casino de Monte Carlo

---

### Qué es una simulación Monte Carlo?

* en una simulación Monte Carlo (MC, de ahora en más) se sigue la evoución de un parámetro físico
* en radiaciones, se sigue la partícula (fotón, $e^-$, $e^+$, n, $\nu$, etc) en sus interacciones
	- cuál es la probabilidad de que recorra determinada distancia?
	- cuál es la probabilidad de que interactúe con electrones del medio?
	- cuál es la probabilidad de que el evento de interacción sea de tipo $k$?
	- cuál es la probabilidad de que dado el evento $k$, la partícula salga con energía $E_f \neq E_i$?
	- cuál es la probabilidad de que salga en un ángulo $(\theta, \phi)$?
	- <span style="color:red">*loop*</span> hasta que me canse

---

Ahora que sabemos de qué se trata...

A almorzar!