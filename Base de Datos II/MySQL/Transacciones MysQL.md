Secuencia de operaciones realizadas como una sola unidad de trabajo. Es un grupo de comandos que se ejecutan con un único comando. Son una parte fundamental en la gestión de bases de datos. 
Permite a los usuarios manejar datos de forma segura y eficiente, garantizando la integridad de los datos incluso en caso de falla del sistema.

Si todas las operaciones dentro de la transacción se ejecutan exitosamente, la transacción se considera exitosa y todos los cambios de datos se guardan permanentemente en la BD. De lo contrario, si cualquiera de las operaciones falla, todos los cambios realizados durante la transacción se revierten y la BD permanece en el mismo estado que tenía antes de que comenzara la transacción.

Las transacciones siguen el modelo ACID (Atomicidad, Consistencia, Aislamiento, Durabilidad), que es un conjunto de propiedades que garantizan la confiabilidad de las transacciones.
##### 1. **Atomicidad:**

- **Todo o nada:** Las transacciones deben garantizar que todas las operaciones dentro de ellas se completen en su totalidad. Si alguna operación falla, todas las operaciones previas se revierten (rollback) y la base de datos vuelve a su estado anterior, asegurando que la transacción no quede incompleta.

##### 2. **Consistencia:**

- **Estado consistente:** Una transacción lleva la base de datos de un estado consistente a otro. Si al principio los datos cumplen con todas las reglas de integridad, al final de la transacción también lo harán. Los cambios parciales o incompletos no son permitidos.

##### 3. **Aislamiento:**

- **Independencia de transacciones:** Las transacciones concurrentes se ejecutan de manera aislada unas de otras, lo que significa que una transacción no puede ver los cambios realizados por otra transacción hasta que esta última haya sido confirmada (commit). MySQL ofrece diferentes niveles de aislamiento para manejar cómo se deben tratar las lecturas entre transacciones:
    - **Read Uncommitted:** Permite leer datos no confirmados, lo que puede llevar a lecturas sucias.
    - **Read Committed:** Solo permite leer datos confirmados por otras transacciones.
    - **Repeatable Read:** Garantiza que una transacción vea los mismos datos durante toda su ejecución, incluso si otros realizan cambios.
    - **Serializable:** El nivel más alto de aislamiento, que asegura que las transacciones se ejecuten secuencialmente, evitando cualquier interferencia.

##### 4. **Durabilidad:**

- **Persistencia de datos:** Una vez que una transacción ha sido confirmada (commit), los cambios realizados en la base de datos son permanentes, incluso en caso de fallos del sistema. Esto asegura que los datos persistan correctamente.
- **Atomicidad:** Significa que una transacción se trata como una única unidad de trabajo (todas las operaciones dentro de la transacción se ejecutan exitosamente o ninguna de ellas).
- **Consistencia:** Garantiza que una transacción lleve la base de datos de un estado válido a otro
- **Aislamiento:** garantiza que cada transacción se ejecute aislada de las demás, lo que significa que las operaciones de una transacción no se vean afectadas por las operaciones de otra transacción.
- **Durabilidad:** garantiza que una vez que se confirma una transacción, seguirá siéndolo, incluso en caso de fallas o errores del sistema o cortes de energía.


Las transacciones se manejan mediante los comandos:
- **START TRANSACTION**
	- Inicia una nueva transacción en la base de datos.
	- Las modificaciones hechas a los datos dentro de la transacción no son visibles para otros usuarios o transacciones hasta que se realice un **`COMMIT`**.
	- Las operaciones realizadas dentro de la transacción no son permanentes hasta que se confirmen.
- **COMMIT**
	- Todos los cambios realizados dentro de la transacción se confirman y se vuelven permanentes.
	- Los cambios son visibles para otros usuarios y transacciones después de realizar un **`COMMIT`**.
	- Una vez ejecutado, no se puede deshacer.
- **ROLLBACK**
	- Deshace todos los cambios realizados durante la transacción actual, volviendo la base de datos a su estado previo.
	- Los cambios no se confirman y no son visibles para otros usuarios.
	- Útil en caso de errores o condiciones no esperadas durante la ejecución de la transacción.
- **AUTOCOMMIT**
	- Permite controlar manualmente cuándo se confirman los cambios en la base de datos.
	- Cuando **`autocommit = 0`**, las transacciones no se confirman automáticamente y se requiere un **`COMMIT`** explícito.
	- Se puede reactivar el autocommit usando **`SET autocommit = 1;`**.
- **SAVEPOINT y "RELEASE SAVEPOINT"**
	- Permite dividir una transacción en partes, haciendo que sea más fácil deshacer parcialmente algunos cambios sin afectar toda la transacción.
	- Los **`SAVEPOINTS`** son útiles cuando se quiere aplicar una lógica de deshacer específica durante la ejecución de una transacción.
- **Niveles de Aislamiento**
	**Niveles disponibles:**
	- **READ UNCOMMITTED:** Permite leer datos no confirmados.
	- **READ COMMITTED:** Permite leer solo datos confirmados.
	- **REPEATABLE READ:** Garantiza que las lecturas repetidas dentro de la misma transacción devuelvan los mismos resultados.
	- **SERIALIZABLE:** Asegura que las transacciones se ejecuten de manera secuencial, evitando interferencias.
	**Características:**
	- El nivel de aislamiento define el comportamiento de las transacciones concurrentes y cómo pueden influirse entre ellas.
	- A mayor nivel de aislamiento (como **SERIALIZABLE**), menor es la probabilidad de errores de concurrencia, pero también disminuye el rendimiento.
## Características:

### 1. **Uso de COMMIT y ROLLBACK:**

- **Control explícito de transacciones:** MySQL permite iniciar transacciones con el comando `START TRANSACTION`, y su finalización puede ser controlada con `COMMIT` (para confirmar los cambios) o `ROLLBACK` (para revertirlos). Esto da control explícito sobre cuándo se deben realizar los cambios en la base de datos.

### 2. **Motores de almacenamiento con soporte para transacciones:**

- No todos los motores de almacenamiento en MySQL soportan transacciones. El motor **InnoDB** es el más comúnmente utilizado porque soporta todas las características de las transacciones, mientras que otros motores, como **MyISAM**, no soportan transacciones, por lo que su uso es limitado en este contexto.

### 3. **Bloqueos (Locks):**

- MySQL utiliza bloqueos para evitar problemas de concurrencia, asegurando que los datos no sean modificados por otras transacciones hasta que la transacción actual se complete. Esto ayuda a mantener la integridad de los datos.
    - **Bloqueo de filas:** Las transacciones solo bloquean las filas que están siendo modificadas.
    - **Bloqueo de tablas:** En algunos casos, se puede bloquear una tabla completa para evitar que otras transacciones la modifiquen.

### 4. **Control de errores:**

- En caso de fallos dentro de una transacción, se puede usar `ROLLBACK` para deshacer todos los cambios realizados desde el inicio de la transacción, lo que permite una recuperación controlada ante errores.

### 5. **Autocommit:**

- MySQL tiene una característica llamada **autocommit**, que, por defecto, está activada. Cuando está habilitada, cada instrucción de SQL se trata como una transacción independiente que se confirma automáticamente después de ejecutarse. Al desactivarlo (`SET autocommit=0`), se requiere el uso explícito de `COMMIT` para confirmar las transacciones.

### 6. **Consistencia y recuperación ante fallos:**

- MySQL asegura la consistencia y recuperación ante fallos gracias al **Log de Transacciones** (Transaction Log) que guarda los cambios en un archivo temporal hasta que la transacción es confirmada. En caso de fallo, este log permite restaurar el estado de la base de datos hasta el último `COMMIT`.
## Ventajas
- **ACID (Atomicidad, Consistencia, Aislamiento, Durabilidad)**
- **Manejo de Errores**
- **Control de concurrencia**
## Desventajas
- **Sobrecarga de Rendimiento**
- **Bloqueos**
- **Complejidad en el código**
- **Uso elevado de recursos**
- **No todas las tablas soportan transacciones**