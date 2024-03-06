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