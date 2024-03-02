# Comandos básicos

## Comandos Strings

* **SET** : Este comando establece la clave con el valor especificado en Redis. Si la clave ya existe, su valor anterior será reemplazado por el nuevo valor.
* **GET** : Recupera el valor asociado con la clave especificada en Redis. Si la clave no existe, se devuelve un valor nulo.
* **SETNX** : Establece el valor de una clave solo si la clave no existe en Redis. Es útil para establecer una clave si no está ya definida.
* **MSET** : Establece múltiples claves y sus respectivos valores en Redis en una sola operación atómica.
* **MGET** : Recupera los valores asociados con múltiples claves especificadas en Redis en una sola operación.
* **FLUSHSALL** : Borra todas las claves y sus valores en la base de datos Redis. Ten cuidado al usar este comando, ya que borra todos los datos de la base de datos actual.
* **INCR** : Incrementa el valor numérico de la clave en 1 en Redis. Si la clave no existe, se establece en 1.
* **INCRBY** : Incrementa el valor numérico de la clave por la cantidad especificada en Redis.
* **DECR** : Decrementa el valor numérico de la clave en 1 en Redis. Si la clave no existe, se establece en -1.
* **DECRBY** : Decrementa el valor numérico de la clave por la cantidad especificada en Redis.