# Problema_Filosofos
Este código en Python implementa una solución al problema conocido como "El Problema de los Filósofos" utilizando hilos en Python. El problema consiste en: Cinco filósofos se sientan alrededor de una mesa y pasan su vida cenando y pensando. Cada filósofo tiene un plato de fideos y un tenedor a la izquierda de su plato. Para comer los fideos son necesarios dos tenedores y cada filósofo sólo puede tomar los que están a su izquierda y derecha. Si cualquier filósofo toma un tenedor y el otro está ocupado, se quedará esperando, con el tenedor en la mano, hasta que pueda tomar el otro tenedor, para luego empezar a comer. 
> Este código utiliza la biblioteca threading de Python para crear hilos para cada Tenedor. También utiliza semáforos para manejar las secciones críticas.

# Funcionamiento del Código
Al comienzo del código se definene las siguientes Constantes:

`CANTIDAD_FILOSOFOS = 0`

`MAX_INTENTOS =10`

`COMER = 0`

`TIEMPO_COMER = 0`

`FILOSOFO = "F"`

`HAMBRIENTO = "H"`

`COMIENDO = "C"`

`SATISFECHO = "S"`

`MUERTO = "M"`

### Semáforos

`Tenedor_izq = candados[id_filosofo]`

`Tenedor_der = candados[(id_filosofo - 1) % CANTIDAD_FILOSOFOS]`

### Solución

La solución consiste en tener un arreglo de RLock, que representarán los palillos y la estrategia consiste en tomar el palillo de la izquierda, y revisar si está disponible el de la derecha, si este es el caso, entonces se toma el de la derecha y se empieza a comer.

<pre><code>palillo_izq.acquire()
if palillo_der.acquire(blocking=False):
    return True
else:
    palillo_izq.release()
    return False
</code></pre>

