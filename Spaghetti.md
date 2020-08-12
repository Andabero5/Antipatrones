
  - [Causas](#causas)
  - [Consecuencias](#consecuencias)
  - [Posibles soluciones](#posibles-soluciones)
  
# ANTIPATRON CODIGO SPAGHETTI

Spaghetti Code aparece como un programa o sistema que contiene muy poca estructura de software. La codificación y las extensiones progresivas comprometen la estructura del software hasta tal punto que la estructura carece de claridad, incluso para el desarrollador original, si él o ella está lejos del software durante cualquier período de tiempo.

Si se desarrolla utilizando un lenguaje orientado a objetos, el software puede incluir un pequeño número de objetos que contienen métodos con implementaciones muy grandes que invocan un único flujo de proceso multietapa.

Además, los métodos de objeto se invocan de una manera muy predecible y hay un grado insignificante de interacción dinámica entre los objetos del sistema. El sistema es muy difícil de mantener y ampliar, y no hay oportunidad de reutilizar los objetos y módulos en otros sistemas similares.

## Causas

- Inexperiencia con tecnologías de diseño orientadas a objetos.
  
- No hay tutoría en su lugar; revisiones de código ineficaces.
- No hay diseño antes de la implementación.
- Con frecuencia es resultado de los desarrolladores que trabajan de forma aislada.

## Consecuencias

- Después de observar el código, solo algunas partes de objetos y métodos parecen adecuadas para su reutilización. Analizar código espagueti a menudo puede ser una mala inversión.
  
- Los métodos están muy orientados a los procesos; con frecuencia, de hecho, los objetos se nombran como procesos.
- El flujo de ejecución viene determinado por la implementación del objeto, no por los clientes de los objetos.
- Existen relaciones mínimas entre objetos.
Muchos métodos de objeto no tienen parámetros y utilizan variables globales o de clase para el procesamiento.
- El patrón de uso de objetos es muy predecible.
- El código es difícil de reutilizar, y cuando lo es, a menudo es a través de la clonación. En muchos casos, sin embargo, el código nunca se considera para su reutilización.
- El talento orientado a objetos de la industria es difícil de retener.
- Se pierden los beneficios de la orientación del objeto; herencia no se utiliza para extender el sistema; polimorfismo no se utiliza.
- Los esfuerzos de mantenimiento de seguimiento contribuyen al problema.
- El software alcanza rápidamente un punto de rendimientos decrecientes; el esfuerzo que implica mantener una base de código existente es mayor que el costo de desarrollar una nueva solución desde cero.

## Posibles soluciones

Mas que soluciones para el codigo spaghetti existen metodos de prevencion, como lo son:

- Realizar una limpieza de codigo cada hora o cada vez que se agreguen funcionalidades al programa.

- Obtenga acceso abstracto a las variables miembro de una clase mediante funciones de descriptor de acceso. Escriba código nuevo y refactorado para utilizar las funciones de acceso.
- Convierta un segmento de código en una función que se pueda reutilizar en futuros esfuerzos de mantenimiento y refactorización. Es vital resistirse a la implementación del AntiPattern Cut-and-Paste. En su lugar, utilice la solución refactorizada Cut-and-Paste para reparar implementaciones anteriores de La AntiPattern de cortar y pegar.
- Reordene los argumentos de función para lograr una mayor coherencia en toda la base de código. 
- Elimine partes del código que pueden volverse, o ya son, inaccesibles. El error repetido de identificar y eliminar partes obsoletas del código es uno de los principales contribuyentes a Lava Flow.
- Cambie el nombre de clases, funciones o tipos de datos para que se ajusten a una entidad empresarial o estándar del sector. La mayoría de las herramientas de software proporcionan soporte para el cambio de nombre global.