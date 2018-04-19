# SITEMAS-OPERATIVOS-1-INDICE
trabajos de clases 

## SITEMAS OPERATIVOS UNIDAD 3 
# DEFINICIONES 

**CARGA**
* El cargador sitúa él módulo de carga en la memoria principal, comenzando en la posición X. En general, se pueden aplicar tres métodos.
  * Carga absoluta
  * Carga reubicable
  * Carga dinámica en tiempo de ejecución

**CARGA ABSOLUTA**
* La carga absoluta necesita al módulo de carga ocupe siempre la misma posición en la memoria principal. La asignación de direcciones a la memoria de un programa la puede realizar tanto el programador como en compilador o el ensamblador.
  
**CARGA DINAMICA EN TIEMPO DE EJECUCION**
*  El cálculo de direcciones dinámicas proporciona una completa flexibilidad. Un programa puede cargarse en cualquier región de la Memoria Principal. Mas tarde, la ejecución de programa puede interrumpirse y el programa ser descargado de la Memoria Principal para ser posteriormente cargado en una posición diferente.

**CARGAS REUBICABLES**
* En la carga reubicable el ensamblador o el compilador no genera direcciones reales de Memoria Principal, sino direcciones relativas a algún punto conocido (como el comienzo de un programa). Al comienzo del módulo de carga se le asigna la dirección relativa “ 0 ” y todas las demás dentro se expresan con relación al comienzo del módulo.

**COMPACTACION**
* El proceso de compactación son unas instancias particulares del problema de asignación de memoria dinámica, y esta se  refiere a satisfacer  una necesidad de tamaño (N) en una lista de huecos libres. Entre tantas posibilidades existe una que determina el hueco más indicado en el momento de asignar.

**COMPARTICION**
* Se refiere a la flexibilidad que varios procesos compartan la misma porción de memoria principal y estroctura de datos sin entrar en conflicto con la proteccion.

**DIRECCION FISICA**
* Una dirección que identifica una posición de memoria principal.

**DIRECCION LOGICA**
* La memoria lógica es el espacio de direcciones, asignado a una partición lógica, que el sistema operativo percibe como su almacenamiento principal. Para una partición lógica que utiliza memoria compartida (en adelante denominada partición de memoria compartida), se hace una copia de seguridad de un subconjunto de la memoria lógica en el almacenamiento principal físico y el resto de la memoria lógica se mantiene en un almacenamiento auxiliar.

**DIRECCION RELATIVA**
* Las rutas relativas señalan la ubicación de un archivo o directorio a partir de el directorio actual del sistema operativo en el sistema de archivos.

  * Ejemplo en Linux de una ruta relativa: si el directorio actual es /home/usuario la ruta relativa dir1/arc1.fil señala al archivo arc1.fil dentro del directorio dir1.
   * Ejemplo en Windows de una ruta relativa: si el directorio actual es c:\windows la ruta relativa para acceder a arc2.dll sería system32\arc2.dll
   
**EDITOR DE ENLACES**
* Es el que establece la combinación de programas mencionada y también crea una imagen de carga a memoria, que resguarda en el almacenamiento secundario (disco), para usos futuros.

**ENLAZADO**
* El enlazado permite al programador y al propio sistema operativo dividir un programa en varios archivos llamados módulos, que pueden ensamblarse por separado y enlazarse en una ocasión posterior, el enlace puede ser de naturaleza estática o dinámica.

**FRAGMENTACION EXTERNA**
* Este tipo de fragmentación aparece como consecuencia de las distintas políticas de
ajuste de bloques que tiene un sistema de ficheros, o al utilizar asignaciones dinámicas de
bloques en el caso de la memoria.

**FRAGMENTACION INTERNA**
* La fragmentación interna es la pérdida de espacio en disco debido al hecho de que el
tamaño de un determinado archivo sea inferior al tamaño del cluster, ya que teóricamente el
archivo estaría obligado a ser referenciado como un cluster completo.

**GESTION DE MEMORIA**
* La administración de memoria representa un vínculo delicado entre el rendimiento (tiempo de acceso) y la cantidad (espacio disponible). Siempre se busca obtener el mayor espacio disponible en la memoria, pero pocas veces existe la predisposición para comprometer el rendimiento. 

**ORGANIZACION LOGICA**
* Normalmente en un sistema informático la memoria principal está organizada de forma lineal como una secuencia de posiciones de memoria. Del mismo modo la memoria secundaria se puede ver como una secuencia de bloques. Esta organización física no se corresponde con la visión del programador que estructura su programa en diferentes módulos. El sistema gestor de memoria debe permitir organizar lógicamente partes de la memoria para acercarse a la visión del programador. La técnica que más fácilmente sastisface esta necesidad es la segmentación.

**ORGANIZACION FISICA**
* Físicamente la memoria está organizada en dos espacios claramente diferenciados:
  * Memoria principal rápida, volátil y escasa 
  * Memoria secundaria lenta, persistente y abundante
* De manera que el SO debe gestionar el trasvase de información entre los dos espacios descargando al programador de esta tarea.

**PAGINACION**
* La paginación es una estrategia de organización de la memoria física que consiste en dividir la memoria en porciones de igual tamaño. A dichas porciones se las conoce como páginas físicas o marcos. La división de la memoria en páginas facilita la gestión de la memoria física.

**PARTICIONAMIENTO**
* Una partición es una división lógica de una unidad de almacenamiento de datos, que actuará como si se tratase de un dispositivo independiente, es decir, nos permite dividir una unidad de almacenamiento en diversas partes.

**PARTICIONAMIENTO FIJO**
* la memoria principal se deivide en particiones estaticas en tiempo de generacion del sistema. 
Un proceso se pude cargar en una particion de igual o superior tamaño.

**PARTICIONAMIENTO DINAMICO**
* las particiones se crean de forma dinamica, de tal forma que cada proceso se carga en una particion del mismo tamaño que el proceso.

**PAGINACION SENCILLA**
* la memoria principal se divide en marcos del mismo tamaño. cada proceso se divide en paginas del mismo tamaño que los marcos. un proceso se carga atraves de la carga de todas sus paginas en marcos disponibles, no nesesariamente continuos.

**SEGMENTACION SENCILLA**
* la memoria principal se divide del mismo tamoño. cada proceso se divide en paginas del mismo tamaño.

**PROTECCION**
* Son los permisos que tiene un proceso para protegerse de terceros (ya sean otros procesos o ususarios).

**REUBICASION**
* Se refiere al termino con el cual se pueden intercambiar los procesos en la memoria principal y no es regresado a la misma ubicasion en la memoria.

**SEGMENTACION**
* La segmentación es una técnica de gestión de memoria que divide dinámicamente la memoria en diferentes segmentos.
Un segmento:
  * Tiene un tamaño que se ajusta a lo que va a contener. Cada segmento puede tener un tamaño diferente.
  * Es un área contigua de memoria, tiene una dirección de inicio (base) y determinado tamaño (número de posiciones de memoria que ocupa).
*Cuando se utiliza segmentación:
  *No existe la fragmentación interna, pero sí hay fragmentación externa. Pueden ser necesarias operaciones de compactación.
  *El segmento se adapta a la visión del programador. Un módulo se corresponde con un segmento.
  *Es fácil compartir datos entre procesos. A cada segmento se le puede asignar unos permisos diferentes, de manera similar a      como se realiza la compartición de información en el sistema de ficheros.

**TABLA DE PAGINAS**
* La tabla de página es una Estructura de datos usada por el sistema de memoria virtual, en un sistema operativo para almacenar la relación entre una dirección virtual en la memoria y la direcciones físicas.


