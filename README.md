Red de sensores ( ADHOC - WiFi) <br>

Nodo 1: gateway
- Comunicación Ethernet con la Red WIFi Doméstica
- Red distribuida WIFi Adhoc
- Cliente http
- Servidor http
- Almacenamiento de estados de cada nodo
- Sincronización con la App Android

Nodo 2: 
- Red distribuida WiFi Adhoc
- Cliente http
- Servidor http
- Lectura sensor DTH11
- Control de temperatura PID
- Display LCD

Nodo 3: 
- Red distribuida  WIFi Adhoc (red Mesh en la librería de Arduino)
- Cliente http <br>
  Envía mensajes hacia el nodo gateway para actualizar el estado de sensores y actuadores.
- Servidor http <br>
  Mensajes recibidos desde el nodo gateway para configurar el arduino según requiera el cliente (la app): 
  - "a": pasa el arduino a modo automático (encendido y apagado de las lámparas según la medición de la fotoresistencia)
  - "b": pasa el arduino a modo manual (se controla la intensidad de las luces mediante la app, mediante los siguientes mensajes:
    - "ba": intensidad a 25% lámpara 1
    - "bb": intensiadad a 50% lámpara 1
    - "bc": intensiadad a 75% lámpara 1
    - "bd": intensiadad a 100% lámpara 1
    - "be": intensidad a 25% lámpara 2
    - "bf": intensiadad a 50% lámpara 2
    - "bg": intensiadad a 75% lámpara 2
    - "bh": intensiadad a 100% lámpara 2
  - "c": estado abierto del servo 1
  - "d": estado cerrado del servo 1
  - "e": estado abierto del servo 2
  - "f": estado cerrado del servo 2
  - "g": estado abierto del servo 3
  - "h": estado cerrado del servo 3
- Sensor: Fotoresistencia <br>
  El Arduino debe evaluar si existe luz en el ambiente y según esto encender o apagar automáticamente las luces.
- Actuadores: 3 servomotores <br>
  Cada servo debe tener dos instrucciones: Abierto o Cerrado (para controlar persianas de una casa)(En el código debe representar dos ángulos, Ej: 0 grados para opción abierto, 180 grados para cerrado)
- Actuadores: 2 lámparas LED <br>
  Se necesita controlar la luminosidad de cada lámpara. <br>
  Características de la lámpara:
  - Potencia de cada lámpara: 3W
  - Input: 85-265 V, 50/60 Hz

Nodo 4:
- Red distribuida  WIFi Adhoc
- Cliente http
- Servidor http
- Fotoresistencia
- Control de lámpara LED luminosidad variable
