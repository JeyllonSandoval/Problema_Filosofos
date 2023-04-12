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

Consiste en un arreglo de Rlock, que presenta los tenedores. La forma en que esta diseñado para que se tome el tenedor de la izquierda, y ver si el tenedor de la derecha se puede tomar. Si se logra tomar el de la derecha, el Filósfo comienza a comer.

<pre><code>tenedor_izq.acquire()
if Tenedor_der.acquire(blocking=False):
    return True
else:
    Tenedor_izq.release()
    return False
</code></pre>

