# Comandos básicos

## Comandos Strings
* **SET** : Este comando establece la clave con el valor especificado. Si la clave ya existe, su valor anterior será reemplazado por el nuevo valor.
* **GET** : Recupera el valor asociado con la clave especificada. Si la clave no existe, se devuelve un valor nulo.
* **SETNX** : Establece el valor de una clave solo si la clave no existe. Es útil para establecer una clave si no está ya definida.
* **MSET** : Establece múltiples claves y sus respectivos valores en una sola operación atómica.
* **MGET** : Recupera los valores asociados con múltiples claves especificadas en una sola operación.
* **FLUSHSALL** : Borra todas las claves y sus valores en la base de datos Redis. Ten cuidado al usar este comando, ya que borra todos los datos de la base de datos actual.
* **INCR** : Incrementa el valor numérico de la clave en 1. Si la clave no existe, se establece en 1.
* **INCRBY** : Incrementa el valor numérico de la clave por la cantidad especificada.
* **DECR** : Decrementa el valor numérico de la clave en 1. Si la clave no existe, se establece en -1.
* **DECRBY** : Decrementa el valor numérico de la clave por la cantidad especificada.


## Comandos de listas
* **LPUSH** : Inserta uno o varios valores al inicio de una. Si la lista no existe, se crea una nueva lista antes de agregar los elementos.
* **RPUSH** : Inserta uno o varios valores al final de una. Si la lista no existe, se crea una nueva lista antes de agregar los elementos.
* **LLEN** : Devuelve la longitud de una lista, es decir, el número de elementos que contiene.
* **LRANGE** : Devuelve los elementos de una lista en el rango especificado. Por ejemplo, LRANGE lista 0 2 devolverá los primeros tres elementos de la lista "lista".
* **LMOVE** : Mueve un elemento desde una lista de origen a una lista de destino.
* **LTRIM** : Recorta una lista para que solo contenga los elementos especificados en el rango.
* **LPOP** : Elimina y devuelve el primer elemento de una lista.
* **RPOP** : Elimina y devuelve el ultimo elemento de una lista.

## Comandos de conjuntos
* **SADD** : Agrega uno o más miembros al conjunto especificado. Si el conjunto no existe, se crea antes de agregar los miembros.
* **SDIFF** : Devuelve la diferencia entre múltiples conjuntos. Es decir, los elementos que están presentes en el primer conjunto pero no en los otros conjuntos especificados.
* **SUNION** : Devuelve la unión de múltiples conjuntos. Es decir, todos los elementos únicos presentes en todos los conjuntos especificados.
* **SINTER** : Devuelve la intersección de múltiples conjuntos en Redis. Es decir, los elementos que están presentes en todos los conjuntos especificados.
* **SCARD** : Devuelve el número de elementos en un conjunto.
* **SMEMBERS** : Devuelve todos los miembros de un conjunto.
* **SISMEMBER** : Verifica si un miembro específico está presente en un conjunto.
* **SREM** : Elimina uno o más miembros de un conjunto.