# Administración del riesgo
El análisis y la administración del riesgo son acciones que ayudan al equipo de software a entender y manejar la incertidumbre.
Un riesgo es un problema potencial: puede ocurrir, puede no ocurrir. Pero, sin importar el resultado, se debe identificarlo, valorar su probabilidad de ocurrencia, estimar su impacto y establecer un plan de contingencia.

# Pasos para la administración de riesgos
## Identificación
Consiste en asumir que los riesgos existen, e identificar cuales son los posibles riesgos del proyecto de software.
## Análisis de probabilidad e impacto
Consiste en determinar la probabilidad de que ocurra un riesgo y valorar el daño que causaría
# Clasificación y plan de manejo de riesgos
Consiste en clasificar los riesgos según su probabilidad e impacto. Se desarrolla un plan de manejo de riesgos.

# Pauta iniciales
## Estrategias reactivas

## Estrategias proactivas

# Planificar para evitar

# Riesgo del proyecto de Software
Son situaciones que amenazan el plan del proyecto. Identifican potenciales problemas de presupuesto, calendario, personal, recursos y complejidad
### Riesgos técnicos
### Riesgos Empresariales

# Identificación de riesgos
Consiste en identificar las amenazas al plan del Proyecto de software.
- Riesgo genéricos
- Riesgos Específicos

# Categorías para identificar riesgos
- Impacto empresarial
- Características de los participantes
- Tamaño del producto
- Definición del proceso
- Entorno de Desarrollo
- Experiencia y tamaño del personal

# Componentes o categorías de riesgos
- Riesgo de rendimiento
- Riesgo de costo
- Riesgo de apoyo
- Riesgo de calendario

# Pasos para la proyección del riesgo
1. Establecer una escala para la probabilidad de los riesgos
2. Delimitar las consecuencias de los riesgos
3. Estimar el impacto del riesgo sobre el proyecto
4. Valorar la certeza de la proyección del riesgo

|                                                       Riesgos                                                        |   Categoría   | Probabilidad | Impacto |                                                         RMMM                                                          |
| :------------------------------------------------------------------------------------------------------------------: | :-----------: | :----------: | :-----: | :-------------------------------------------------------------------------------------------------------------------: |
|           No existe comunicación con las autoridades de la universidad para retroalimentación del sistema            |     Apoyo     |     40%      |    3    |                                                                                                                       |
| Pérdida de datos por fallo en la base de datosPoca o nula capacitación hacia el personal para el manejo del programa |  Desarrollo   |     40%      |    2    |                    Implementar copias de seguridad automáticas diarias. Usar replicación de datos.                    |
|                                  Errores en la generación del calendario del torneo                                  |  Desarrollo   |     60%      |    1    | Realizar pruebas con diferentes escenarios antes del despliegue. Incluir validaciones en la lógica de emparejamiento. |
|                             Problemas de seguridad (inyección SQL, acceso no autorizado)                             |  Desarrollo   |     80%      |    1    |   Implementar **parametrización de consultas**, cifrado de contraseñas y control de acceso basado en roles (RBAC).    |
|                                        Saturación del servidor en horas pico                                         |  Desarrollo   |     60%      |    2    |                  Usar balanceo de carga y optimizar consultas SQL para reducir tiempos de respuesta.                  |
|                                     Falta de adopción por parte de los usuarios                                      | Participantes |     50%      |    3    |                    Proporcionar capacitaciones y guías de uso a los administradores y estudiantes.                    |
|                              Problemas de compatibilidad con navegadores o dispositivos                              |  Desarrollo   |     60%      |    2    |                   Realizar pruebas en diferentes navegadores y dispositivos antes del lanzamiento.                    |
|                              Manipulación de datos por parte de usuarios no autorizados                              |  Desarrollo   |     70%      |    1    |                    Implementar control de acceso con autenticación segura y auditoría de cambios.                     |
|                          Cambios en los criterios del torneo (reglas, formato, puntuación)                           |    Proceso    |     80%      |    1    |     Diseñar el sistema con flexibilidad para modificar parámetros sin alterar la estructura de la base de datos.      |
|                                 Baja disponibilidad del sistema (caídas inesperadas)                                 |  Desarrollo   |   <br>40%    |    1    |            Monitorear el sistema en tiempo real y utilizar servidores en la nube con alta disponibilidad.             |
|                                                                                                                      |               |              |         |                                                                                                                       |

# Plan de Mitigación, Monitoreo y Manejo del Riesgo
Este plan puede estar compuesto por hojas de información de riesgos
#### Mitigación del Riesgo
Es una actividad que busca evitar el problema
#### Monitoreo del riesgo
Valora si los riesgos ocurren o no y verifca que tan eficaz es.