## Rendimiento del sistema

- Cantidad de memoria disponible = Manera en que se optimiza mientras se procesan los trabajos

## Funciones Principales

- El SO asigna memoria a los procesos.
- Utiliza diferentes métodos u operaciones que se encargan de obtener la máxima utilidad de la memoria.
- Organiza de forma física y lógica los procesos y programas para aprovechar de la mejor manera la memoria
- Lleva a la memoria los procesos para que luego las ejecute el procesador

# Esquemas de asignación de memoria

Algoritmos, como hace el administrador para asignar memoria

## Sistemas de usuarios únicos

### Esquema continuo de usuario único

- Cada programa se iba cargando en su totalidad en la memoria y se le asignaba tanto espacio continuo como fuese necesario
- Era ineficaz porque solo una tarea ejecutaba a la vez, lo que implica un único usuario por computadora
- Requería un registro para la dirección base y un acumulador
- Utilizado entre la década de 1950-1960

## Particiones fijas

- Conocidos como particiones estáticas
- Cada partición puede usarse solo por un programa
- Consiste en asignar una partición para cada trabajo
- Se agrega la protección para las particiones
- Permite que varios programas estén al mismo tiempo en la memoria
- Fragmentación interna: desaprovechamiento de la memoria

## Particiones dinámicas

- La mejor partición cumple con los requerimientos
- Desventaja: busca primero en toda la tabla

### Asignación del primer ajuste

1. Primera partición que cumple con los requerimientos

## MMU

- Encargada de verificar que un proceso no tenga acceso a leer o modificar los datos de otros
- Verifica los espacios en memoria

## Memoria Caché

- Provee de un empuje adicional en tiempo y ahorro de recursos al sistema
- Guarda copias de las páginas que van siendo accesadas

### Memoria RAM

- Tipo de memoria operativa donde se ejecuta la mayor parte del software, desde el propio sistema operativo hasta el software de aplicación
- Permite grabar o recuperar información sin necesidad de un orden secuencial
- Memoria de libre acceso, a la que se accede de forma rápida y ágil
- Forma de memoria temporal a corto plazo, al apagar o reiniciar el sistema, vuelve a estar en blanco

## Tipos de Memoria RAM

### SRAM

- Capaz de mantener los datos sin necesidad de circuitos de refrescamiento
- No expandible por el usuario
- Dedicada al procesador del sistema

### DRAM

- Requieren de un circuito de refrescamiento que revisa su carga y la repone
- Inventada a finales de 1960, más utilizada actualmente
- Permite crear módulos de alta velocidad de trabajo

### SDR

- Es capaz de procesar una única operación de lectura o escritura

### DDR

- Es capaz de procesar dos operaciones de lectura o escritura
- La más empleada en las computadoras comerciales

## Memoria ROM (Read-Only Memory)

- Tipo de almacenamiento empleado en computadoras y otros dispositivos
    
- Únicamente de acceso para lectura y nunca para escritura
    
- Se le puede recuperar pero no modificar
    
    ### Almacenamiento de Software
    
    Se utiliza para instalar el software de arranque o de funcionamiento más básico (BIOS y SETUP)
    
    ### Almacenamiento de datos
    
    Almacena los datos como tablas de consulta, operadores matemáticos o lógicos
    

## Asignación de la memoria paginada

- Divide cada trabajo de entrada en páginas del mismo tamaño
- Marcos de página sectores de la memoria
- Se divide en parte llamadas páginas
- No es necesario cargarlo en bloques adyacentes

## Pasos que el administrado de memoria realiza antes de ejecutar programas

1. Determina el número de páginas del programa
    
2. Localiza diferentes marcos de página en la memoria principal
    
3. Carga todas las páginas del programa en éste
    
    ### Ventajas
    
    - RAM puede usarse de manera más eficiente porque el marco de una página vacía puede ser usado por cualquier página de cualquier trabajo
    - No hay fragmentación externa entre los marcos de las páginas
    
    ### Desventajas
    
    - Existe la fragmentación interna
    - Agranda el tamaño y la complejidad del software

## Paginación por demanda

- Para procesar el programa solamente carga una parte en la memoria
    
- Elimina la restricción de tener todo el trabajo en la memoria
    
- Los trabajos residen en un principio e el almacenamiento secundario
    
- Los trabajos se siguen dividiendo en paginas del mismo tamaño
    
    ### Ventajas
    
    - Las páginas se cargan a medida que se solicita cada una
    - Hizo factible la memoria virtual
    - Los trabajos se ejecutan con menos memoria RAM

## Manejador de fallo de página

- La página esta en el almacenamiento secundario y no en la memoria
- Este determina copiar desde el almacenamiento secundario de inmediato la pagina solicitada a la memoria si hay macros de páginas vacíos

## Thrashing

## FIFO (First In, First Out)

- Retira las páginas que han permanecido el mayor tiempo en la memoria

## LRU

- Menos usada recientemente
- Cambia hacia afuera las páginas que muestran la menor cantidad de actividad reciente
- Utiliza la política de reemplazo de páginas de reloj

## ¿Qué asignación de memoria utilizan los sistemas operativos?

### Windows

- **Memoria Virtual**:
    - **Segmentación**: Divide la memoria en segmentos de diferentes tamaños según las necesidades del programa. Cada segmento puede contener un tipo diferente de datos, como código, datos o pila.
    - **Paginación**: Divide la memoria física y virtual en bloques del mismo tamaño llamados páginas. Facilita la gestión de memoria y la protección entre procesos.
- **Asignación Contigua**:
    - **Particiones Fijas**: La memoria se divide en particiones de tamaño fijo. Es simple pero puede llevar a fragmentación interna.
    - **Particiones Dinámicas**: La memoria se divide en bloques de tamaño variable según la demanda. Minimiza la fragmentación interna, pero puede causar fragmentación externa.
- **Algoritmos de Asignación de Memoria**:
    - **First-Fit**: Asigna el primer bloque de memoria disponible que sea lo suficientemente grande.
    - **Best-Fit**: Busca el bloque de memoria más pequeño que sea lo suficientemente grande para minimizar el espacio desperdiciado.
    - **Worst-Fit**: Asigna el bloque más grande disponible para maximizar el tamaño de los bloques restantes.
- **Swapping (Intercambio)**:
    - Traslada temporalmente los procesos entre la memoria principal y el almacenamiento secundario para liberar memoria física para otros procesos.
- **Memoria Compartida**:
    - Permite que múltiples procesos accedan a una misma región de memoria, facilitando la comunicación y reducción de duplicación de datos.
- **Memoria Caché**:
    - Utiliza niveles de caché (L1, L2, L3) para almacenar datos e instrucciones más frecuentemente utilizados, acelerando el acceso a la memoria principal.
- **Garbage Collection (Recolección de Basura)**:
    - En lenguajes de programación con gestión automática de memoria (como Java o Python), el sistema operativo o el entorno de ejecución libera automáticamente la memoria que ya no es utilizada por el programa.
- **NUMA (Non-Uniform Memory Access)**:
    - En sistemas multiprocesador, se optimiza la memoria para que cada procesador tenga acceso preferente a una región de memoria específica, reduciendo latencias.

---

### Linux

- **Memoria Virtual**:
    - **Paginación**: Linux usa un esquema de paginación, donde la memoria se divide en pequeñas unidades llamadas páginas (generalmente de 4 KB). Cada proceso tiene su propio espacio de direcciones virtuales, que se mapea a las páginas físicas mediante tablas de páginas.
    - **Segmentación**: Aunque Linux usa segmentación para algunas cosas, la mayor parte de la gestión de memoria se realiza a través de la paginación. En las arquitecturas x86, la segmentación se usa principalmente para separar el espacio del kernel del espacio del usuario.
- **Asignación Contigua**:
    - **Buddy System**: Linux utiliza un sistema de asignación de memoria contigua llamado "buddy system" para gestionar grandes bloques de memoria. Este sistema divide la memoria en bloques de tamaño variable que son potencias de dos. Esto ayuda a minimizar la fragmentación.
- **Memoria de Intercambio (Swap)**:
    - Linux utiliza espacio de intercambio (swap) en el disco duro para ampliar la memoria física disponible. Si la memoria RAM se llena, las páginas de memoria menos utilizadas se trasladan al espacio de intercambio, liberando RAM para otros usos.
- **Memoria Caché**:
    - **Page Cache**: Linux usa una caché de páginas para almacenar en memoria las páginas de archivos que se han leído o escrito recientemente, mejorando el rendimiento del sistema al reducir el acceso al disco.
    - **Slab Allocator**: Utilizado para la asignación eficiente de objetos de kernel de tamaño fijo. Optimiza la reutilización de memoria y minimiza la fragmentación.
- **Algoritmos de Asignación de Memoria**:
    - **First-Fit**: El algoritmo first-fit se usa comúnmente para encontrar el primer bloque de memoria libre que sea lo suficientemente grande para una solicitud.
    - **Best-Fit y Worst-Fit**: Aunque estos no se utilizan directamente en el kernel de Linux, las estrategias similares pueden implementarse en la gestión específica de ciertos recursos.
- **Transparent Huge Pages (THP)**:
    - Para optimizar el rendimiento, Linux puede usar páginas de memoria grandes (huge pages), que son múltiples de las páginas estándar (por ejemplo, 2 MB en lugar de 4 KB). THP permite el uso automático de estas páginas grandes sin intervención del usuario.
- **Control de Memoria**:
    - **Control Groups (cgroups)**: Permite la asignación y limitación de recursos de memoria entre grupos de procesos, proporcionando un control fino sobre la cantidad de memoria que un grupo de procesos puede usar.
- **NUMA (Non-Uniform Memory Access)**:
    - En sistemas multiprocesador, Linux soporta NUMA, optimizando la asignación de memoria para que cada procesador acceda preferentemente a su región de memoria local, reduciendo la latencia.

## Asignación de memoria segmentada

- Las instrucciones están ordenadas secuencialmente dentro de los segmentos

## Utiliza 3 tablas

- Tabla de trabajo
    
- Tabla de mapa de segmentos
    
- Tabla de mapa de la memoria
    
    ### Desventajas
    
    Fragmentación externa, por lo que hay que volver a compactar la memoria
    

## Diferencia con la paginación

### Las páginas (físico)

Son unidades físicas que son indivisibles para el programa del usuario constan de tamaño físico

### Los segmentos (lógico)

Unidades lógicas