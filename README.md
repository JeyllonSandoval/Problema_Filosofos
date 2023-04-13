# Problema_Filosofos

Este código en Python implementa una solución al problema conocido como "El Problema de los Filósofos" utilizando hilos en Python. El problema consiste en: Cinco filósofos se sientan alrededor de una mesa y pasan su vida cenando y pensando. Cada filósofo tiene un plato de fideos y un tenedor a la izquierda de su plato. Para comer los fideos son necesarios dos tenedores y cada filósofo sólo puede tomar los que están a su izquierda y derecha. Si cualquier filósofo toma un tenedor y el otro está ocupado, se quedará esperando, con el tenedor en la mano, hasta que pueda tomar el otro tenedor, para luego empezar a comer. 
> Este código utiliza la biblioteca threading de Python para crear hilos para cada Tenedor. También utiliza semáforos para manejar las secciones críticas.

# Funcionamiento del Código
Al comienzo del código se definene varias Constantes, como:

`CANTIDAD_FILOSOFOS = 0`

`MAX_INTENTOS =10`

`HAMBRIENTO = "H"`

`COMIENDO = "C"`

`MUERTO = "M"`

### Solución

Consiste en un arreglo de RLock, que presenta los tenedores. La forma en que esta diseñado para que se tome el tenedor de la izquierda, y ver si el tenedor de la derecha se puede tomar. Si se logra tomar el de la derecha, el Filósfo comienza a comer.

> RLock (Reentrant Lock):

<pre><code>tenedor_izq.acquire()
if Tenedor_der.acquire(blocking=False):
    return True
else:
    Tenedor_izq.release()
    return False
</code></pre>


***

# Concurrencia 
Es la capacidad de un sistema informático para realizar múltiples tareas o procesos simultáneamente, de manera que parezca que están sucediendo al mismo tiempo.


# Paralelismo vs. Concurrencia en informática
Ambos conceptos se refieren a la ejecución simultánea de procesos, pero el paralelismo implica la ejecución real simultánea de múltiples tareas en diferentes núcleos o procesadores, mientras que la concurrencia implica la ejecución aparente simultánea de múltiples tareas mediante la alternancia entre ellas.


# Hilos implementación en Python
Python tiene una biblioteca estándar de hilos llamada threading, que permite la creación y administración de hilos en aplicaciones Python. Los hilos son una forma de lograr la concurrencia en Python.


# Deadlock
Ocurre cuando dos o más procesos se bloquean entre sí mientras esperan recursos que poseen los otros procesos, lo que resulta en una situación en la que ningún proceso puede avanzar.


# Exclusión mutual
Es un mecanismo que se utiliza para garantizar que solo un proceso pueda acceder a un recurso compartido en un momento dado, para evitar conflictos y condiciones de carrera.


# Mantenga y espere
Es una técnica utilizada para prevenir los problemas de interbloqueo, que implica que un proceso mantenga cualquier recurso que ya tenga mientras espera para adquirir otros recursos que necesita.

# No preventivo
Un sistema de interbloqueo no preventivo no toma medidas para evitar o prevenir el interbloqueo. En lugar de eso, intenta resolver los problemas de interbloqueo después de que hayan ocurrido.


# Espera circular
Es una situación en la que un conjunto de procesos se bloquea mutuamente en un ciclo de espera circular, lo que resulta en un interbloqueo.


# Cómo manejar el interbloqueo en sistemas operativos – Compara con el problema de los filósofos
El problema de los filósofos es un problema clásico de concurrencia que implica a varios filósofos sentados alrededor de una mesa con un plato de comida, y una horquilla para cada uno. El problema se puede solucionar utilizando técnicas como exclusión mutua, espera aleatoria y ordenamiento de recursos. De manera similar, el interbloqueo en sistemas operativos se puede solucionar utilizando técnicas como exclusión mutua, ordenamiento de recursos y liberación de recursos en un orden específico.



### Código de la solucion del problema de python

> [Problema de los Filósofos](https://github.com/EmmanuelETM/Problema_Filosofos/blob/main/Problema_Filosofos.py)
> 
### Diagrama de Flujo

> [Diagrama de Flujo](https://github.com/EmmanuelETM/Problema_Filosofos/blob/main/Diagrama%20del%20problema%20de%20los%20filosofos.png)

### Video Explicativo sobre la solucion del problema de los barberos

> [Video Explicativo](https://miucateciedu-my.sharepoint.com/:v:/g/personal/20211155_miucateci_edu_do/EYnSq10pPTVJhfvMNnj8OPYBksV_n3fiQ_sL9aYX3-BVeQ?e=ATFvko)
