  - [**Antecendentes**](#antecedentes)
  - [**Síntomas y consecuencias**](#sintomas-y-consecuencias)
  - [**Solucion**](#solucion)
  

**Nombre antipatrón**: Lava Flow

**También conocido como**: Dead Code

**Escala más frecuente**: aplicación.

**Nombre de la solución refactorizado**: Gestión de la configuración arquitectónica.

**Tipo de solución refactorizada**: proceso.

**Causas principales**: avaricia, codicia, pereza.

**Fuerzas desequilibradas**: gestión de la funcionalidad, rendimiento, complejidad.

# **ANTECEDENTES**


En una expedición de minería de datos, se comenzó a buscar información para desarrollar una interfaz estándar o base para un tipo particular de sistema. El sistema que se estaba extrayendo era muy similar a los que que se esperaba eventuualmente que admitiera el la interfaz en la cual se había trabajado. También era un sistema de investigación y muy complejo,se realizaron entrevistas a muchos de los desarrolladores sobre ciertos componentes de la enorme cantidad de páginas de código impresas para el trabajo que se estaba realizando.

Los desarrolladores siempre respodían que no sabían para que se usaba una determinada clase y que estaba modulada incluso antes de que el desarrollador empezara a trabajar en el proyecto. Gradualmente se dieron cuenta de que entre el 30 y el 50 por ciento del código real que comprendía este complejo sistema no era entendido ni documentado por nadie que trabajara en él.

Además se llego a la conclusión de que el código cuestionable realmente no tenía ningún propósito en el sistema actual; más bien, estaba allí de intentos o enfoques anteriores de desarrolladores que se habían ido. El personal actual, aunque muy inteligente, se mostraba reacio a modificar o eliminar el código que no escribían o no conocían el propósito, por temor a romper algo y no saber por qué o cómo solucionarlo.

En este punto,se comenzó a llamar a esas manchas de código "lava", refiriéndonos a la naturaleza fluida en la que se originaron en comparación con la dureza del basalto y la dificultad para eliminarlo una vez que se solidificó. Es allí en donde se identifica y se reconoce un nuevo antipatrón , incluso casi un año después, y después de varias expediciones de minería de datos y esfuerzos de diseño de interfaces, varios desarrolladores se habían encontrado con el mismo patrón con tanta frecuencia que habitualmente se referían a él como  Lava Flow en todo el departamento.

# **SÍNTOMAS Y CONSECUENCIAS**

- Variables injustificables frecuentes y fragmentos de código en el sistema.
- Funciones, clases o segmentos complejos indocumentados que parecen importantes y que no se relacionan claramente con la arquitectura del sistema.
- Arquitectura de sistema muy flexible y "en evolución".
- Bloques completos de código comentado sin explicación ni documentación.
- Muchas áreas de código "en proceso de cambio" o "por reemplazar".
- Código no utilizado (muerto), recién dejado.
- Interfaces no utilizadas, inexplicables u obsoletas ubicadas en archivos de encabezado.
- Si no se elimina el código de Lava Flow existente, puede continuar proliferando a medida que el código se reutiliza en otras áreas.
- Si no se controla el proceso que conduce a Lava Flow, puede haber un crecimiento exponencial ya que los desarrolladores sucesivos, demasiado apresurados o intimidados para analizar los flujos originales, continúan produciendo nuevos flujos secundarios mientras tratan de trabajar alrededor de los originales. el problema.
- A medida que los flujos se componen y endurecen, rápidamente se vuelve imposible documentar el código o comprender su arquitectura lo suficiente como para realizar mejoras.

# **SOLUCIÓN**


Solo hay una forma infalible de prevenir este antipatrón: 

- Asegurarse de que la arquitectura de sonido precede al desarrollo del código de producción. Esta arquitectura debe estar respaldada por un proceso de administración de configuración que garantice el cumplimiento de la arquitectura y se adapte a la "misión lenta" (requisitos cambiantes).

- Si la consideración de la arquitectura no se modifica por adelantado, en última instancia, se desarrolla un código que no es parte de la arquitectura de destino y, por lo tanto, es redundante o está muerto. Con el tiempo, el código muerto se vuelve problemático para el análisis, la prueba y la revisión.

- En los casos en los que Lava Flow ya existe, la cura puede ser dolorosa. Un principio importante es evitar cambios de arquitectura durante el desarrollo del proyecto. En particular, esto se aplica a la arquitectura computacional, las interfaces de software que definen la solución de integración de sistemas. La gerencia debe posponer el desarrollo hasta que se haya definido una arquitectura clara y se haya difundido a los desarrolladores.

  La definición de la arquitectura puede requerir una o más actividades de descubrimiento del sistema. El descubrimiento del sistema es necesario para localizar los componentes que realmente se utilizan y son necesarios para el sistema. El descubrimiento del sistema también identifica aquellas líneas de código que se pueden eliminar de forma segura. Esta actividad es tediosa; puede requerir las habilidades de investigación de un detective de software experimentado.

- A medida que se elimina el código muerto sospechoso, se introducen errores. Cuando esto suceda, resista la tentación de corregir inmediatamente los síntomas sin comprender completamente la causa del error. Estudie las dependencias. Esto le ayudará a definir mejor la arquitectura de destino.

- Para evitar Lava Flow, es importante establecer interfaces de software a nivel de sistema que sean estables, bien definidas y claramente documentadas. La inversión inicial en interfaces de software de calidad puede producir grandes dividendos a largo plazo en comparación con el costo de eliminar los glóbulos endurecidos del código Lava Flow.

  Herramientas como el sistema de control de código fuente (SCCS) ayudan en la gestión de la configuración. SCCS se incluye con la mayoría de los entornos Unix y proporciona una capacidad básica para registrar historiales de actualizaciones en archivos controlados por configuración.