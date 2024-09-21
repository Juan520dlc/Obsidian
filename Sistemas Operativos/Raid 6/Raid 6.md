### ¿Qué es?
Principio de almacenamiento en el que se combinan cuatro o más discos duros en una unidad lógica individual. De esta manera, aumenta la fiabilidad y al mismo tiempo la velocidad de lectura en comparación con los soportes de datos individuales. Para es es fundamental la **combinación de striping y paridad**, que también se aplican en el nivel original RAID 5. No es casualidad que el RAID 6 también se conozca como la extensión de RAID 5.

Implementan el enfoque del striping de la manera clásica: todos los datos se dividen en bloques y reparten uniformemente en los discos duros conectados. Esto brinda a los usuarios la posibilidad de acceder simultáneamnte a varios discos y leer parte de los bloques de una franja de datos en paralelo.

El sistema siempre almacena dos fases de información de paridad, lo que en caso de fallo de uno o dos discos permite restaurar los datos **[[XOR]]** o la mezcla con la corrección de errores de varios bits mediante el código **Reed-Solomon**. 