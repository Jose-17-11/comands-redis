## Streams

Una secuencia de Redis es una estructura de datos que actúa como un registro de solo agregar, pero también implementa varias operaciones para superar algunos de los límites de un registro de solo agregar típico. Estos incluyen acceso aleatorio en tiempo O(1) y estrategias de consumo complejas, como grupos de consumidores. Puede utilizar transmisiones para grabar y distribuir eventos simultáneamente en tiempo real. Ejemplos de casos de uso de flujo de Redis incluyen:

* Búsqueda de eventos (p. ej., seguimiento de las acciones de los usuarios, clics, etc.)
* Monitoreo de sensores (p. ej., lecturas de dispositivos en el campo)
* Notificaciones (por ejemplo, almacenar un registro de las notificaciones de cada usuario en una secuencia separada)

Redis genera una identificación única para cada entrada de transmisión. Puede utilizar estos ID para recuperar sus entradas asociadas más adelante o para leer y procesar todas las entradas posteriores en la secuencia. Tenga en cuenta que debido a que estos ID están relacionados con el tiempo, los que se muestran aquí pueden variar y serán diferentes de los ID que ve en su propia instancia de Redis.

Bibliografia:
https://redis.io/docs/data-types/streams/

## Hashes

Los hashes de Redis son tipos de registros estructurados como colecciones de pares de valor de campo. Puedes utilizar hashes para representar objetos básicos y almacenar agrupaciones de contadores, entre otras cosas.

Si bien los hash son útiles para representar objetos , en realidad la cantidad de campos que puede colocar dentro de un hash no tiene límites prácticos (aparte de la memoria disponible), por lo que puede usar hashes de muchas maneras diferentes dentro de su aplicación.

Bibliografia:
https://redis-io.translate.goog/docs/data-types/hashes/?_x_tr_sl=auto&_x_tr_tl=es&_x_tr_hl=es-419

## Paramametros que llevan los comandos de streams: xadd, xack, xdel, xrange

XADD:
* clave: El nombre de la clave del stream al que se añadirá el elemento.
<<<<<<< HEAD
=======
* MAXLEN [~][count]: (Opcional) Especifica un límite de longitud para el stream. Puedes usar el modificador "~" para especificar que el límite se aplica al número de elementos en lugar de bytes. "count" es el límite de elementos o bytes, según el modificador utilizado.
>>>>>>> a3dcf33ef00d825e23f1894c62193b44fcbe4b09
* ID id: (Opcional) Especifica el ID para el elemento añadido. Si no se proporciona, Redis generará automáticamente un ID único.
* campo1 valor1 [campo2 valor2 ...]: Los pares campo-valor que constituyen los datos del elemento a añadir.

XACK:
* clave: El nombre de la clave del stream.
* grupo: El nombre del grupo de consumidores.
* ID [ID ...]: Los IDs de los mensajes que se están confirmando.

XDEL:
* clave: El nombre de la clave del stream.
* ID [ID ...]: Los IDs de los mensajes que se desean eliminar.

XRANGE:
* clave: El nombre de la clave del stream.
* inicio: El ID del mensaje inicial del rango.
* fin: El ID del mensaje final del rango.
* COUNT cantidad: (Opcional) El número máximo de elementos que se deben devolver en la lista.