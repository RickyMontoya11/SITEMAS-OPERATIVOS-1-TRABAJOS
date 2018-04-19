# SITEMAS-OPERATIVOS-1-INDICE
trabajos de clases 

# Sistemas Operativos 1, Unidad 3 Administracion de la memoria
## Definiciones

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


# Sistemas Operativos 1, Unidad 4 Administracion de Entrada/Salida 

**Asignación de fichero**

**Asignación con índices (indexada)**
* En este esquema se guarda en el directorio un bloque de índices para cada archivo, con apuntadores hacia todos sus bloques constituyentes, de manera que el acceso directo se agiliza notablemente, a cambio de sacrificar varios bloques para almacenar dichos apuntadores. Cuando se quiere leer un archivo o cualquiera de sus partes, se hacen dos accesos: uno al bloque de índices y otro a la dirección deseada. Este es un esquema excelente para archivos grandes pero no para pequeños, porque la relación entre bloques destinados para índices respecto a los asignados para datos es incosteable.

**Asignación contigua**
* Cada directorio contiene la los nombres de archivos y la dirección del bloque inicial de cada archivo, así como el tamaño total de los mismos.

**Asignación encadenada**
* Con este criterio los directorios contienen los nombres de archivos y por cada uno de ellos la dirección del bloque inicial que compone al archivo. Cuando un archivo es leído, el brazo va a esa dirección inicial y encuentra los datos iniciales junto con la dirección del siguiente bloque y así sucesivamente. Con este criterio no es necesario que los bloques estén contiguos y no existe la fragmentación externa, pero en cada "eslabón" de la cadena se desperdicia espacio con las direcciones mismas. En otras palabras, lo que se crea en el disco es una lista ligada.

**Base de Datos**
* Base de Datos: es un conjunto de información relacionada que se encuentra agrupada o estructurada. Un archivo por sí mismo no constituye una base de datos, sino más bien la forma en que está organizada la información es la que da origen a la base de datos.
Base de Datos: colección de datos organizada para dar servicio a muchas aplicaciones al mismo tiempo al combinar los datos de manera que aparezcan estar en una sola ubicación

**Bloque**
* En los dispositivos de almacenamiento secundario (discos duros, por ejemplo), la información se agrupa en bloques. Cada archivo está compuesto por 1 o varios bloques, y a su vez cada bloque está ubicado en un número de sectores.
La elección del tamaño del bloque es importante, ya que los bloques siempre se asignan completos, por lo que la parte sobrante no se puede utilizar.

**Campo**


**Campo clave**


**Directorio**
*  El directorio contiene información sobre los archivos, incluyendo atributos, ubicación y propietario. El directorio es propiamente un archivo poseído por el sistema operativo y accesible a través de diversas rutinas de gestión de archivos. Aunque parte de la información de los directorios está disponible para los usuarios y aplicaciones, ésta la proporcionan, generalmente de un modo indirecto, las rutinas del sistema.

**Directorio actual**
* El directorio actual es el primer directorio en el que el sistema operativo busca los programas y archivos y almacena los archivos temporales y la salida. Cuando se solicita una operación sobre un objeto, como por ejemplo un archivo, el sistema busca el objeto en el directorio actual a menos que se especifique una vía de acceso de directorio distinta. 

**Fichero**
* Un archivo es una colección de información relacionada con nombre que se guarda en almacenamiento secundario.

**Fichero de acceso directo o hash**
* Aprovecha la capacidad de los discos para entrar a cualquier bloque de dirección que se va a utilizar y eso requiere de un campo clave para cada registro como los métodos anteriores. A diferencia que su ordenamiento no es secuencial.

**Fichero indexado**
* Posee varias características que el archivo secuencial ya que se organizan en campos. Este método supera las desventajas del otro método. Este tiene un índice del archivo que permite llegar rápidamente a un registro deseado, esto se le llama archivo de desbordamiento, y se ejecuta a través de la dirección de punteros donde están ubicados en los registros deseados.

**Fichero secuencial**
* Los registros se almacenan por posición, cada registro tiene el mismo tamaño y el mismo número de campos. El primero de cada registro de un campo se lee como campo clave, para leer un archivo el sistema comienza al principio del archivo y lee un registro a la vez hasta llegar al registro deseado. 

**Fichero secuencial indexado**
* Los registros se organizan en una secuencia basada en un campo clave presentando dos características, un índice del archivo para soportar los accesos aleatorios y un archivo de desbordamiento. El índice proporciona una capacidad de búsqueda para llagar rápidamente al registro deseado y el archivo de desbordamiento es similar al archivo de registros usado en un archivo secuencial, pero está integrado de forma que los archivos de desbordamiento se ubiquen siguiendo un puntero desde su registro predecesor. 

**Métodos de acceso**
* Para poder utilizar la información almacenada en un archivo, las aplicaciones deben acceder a la misma y almacenarla en memoria. Hay distintas formas de acceder a un archivo. Para una aplicación, elegir adecuadamente la forma de acceder a un archivo suele ser un aspecto importante de diseño, ya que, en muchos casos, el método de acceso tiene un impacto significativo en el rendimiento de la misma.

Dependiendo de que se pueda saltar de una posición a otra de un archivo, se distinguen dos métodos de acceso principales: acceso secuencial y acceso directo.

Cuando se usa el método de acceso secuencial, lo único que se puede hacer es leer los bytes del archivo en orden, empezando por el principio. No puede saltar de una posición del archivo a otra o leerlo desordenado. Si se quiere volver atrás, hay que volver al principio y releer todo el archivo hasta el punto deseado. Las operaciones más comunes son lecturas y escrituras.

Con la llegada de los dispositivos de acceso directo (como los discos magnéticos), surgió la forma de acceso directo, o aleatorio, a un archivo. El archivo se considera como un conjunto de registros, cada uno de los cuales puede ser un byte. Se puede acceder al mismo desordenadamente moviendo el apuntador de acceso al archivo a uno u otro registro. Esta forma de acceso se basa en un modelo de archivo almacenado en disco, ya que se asume que el dispositivo se puede mover aleatoriamente entre los distintos bloques que componen el archivo.

**Nodo-i**
* Un archivo posee varios componentes: un nombre, contenido e información administración como permiso y fechas de modificación. La información administrativa esta almacenada en el “ nodo-i ”( en ingles muchas veces se usa inodo ( sin guión) en vez de i-nodo), junto con datos esenciales para el sistema tales como su longitud, la región del disco en la que se encuentra almacenado el contenido del archivo y otros elementos.

Existen tres fechas en un i-nodo: la fecha en la que se hizo la ultima modificación ( escrita ) al contenido del archivo, la fecha en la que dicho contenido fue usado ( leído o ejecutado ) por ultima vez y la fecha en la que el i-nodo fue alterado por ultima vez, por ejemplo, para definir los permisos.

**Nombre de fichero**
* Las reglas exactas para los nombres de archivos varían de sistema a sistema.
Algunos sistemas de archivos distinguen entre las letras mayúsculas y minúsculas, mientras que otros no.

Muchos S. O. utilizan nombres de archivo con dos partes, separadas por un punto:
La parte posterior al punto es la extensión de archivo y generalmente indica algo relativo al archivo, aunque las extensiones suelen ser meras convenciones.

**Pila**
* la mayoría del trabajo no se hace accediendo directamente a los objetos sino a los registros y a una útil herramienta llamada stack, como su nombre lo indica el stack es una pila (una lista apilada) donde los elementos se colocan uno sobre otro y solo es accesible de manera inmediata el elemento que esta en la cima de la pila.

**Registro**
* El registro del sistema es una base de datos la cual los SO usan para almacenar información sobre la configuración del equipo.

**Ruta del nombre**
* Cuando  el  sistema  de  archivos  está  organizado como  un  árbol  de  directorios  se  necesita  una forma de determinar los nombres de los archivos.  Los principales métodos para nombres de los archivos son:

 * Ruta de Acceso Absoluta
 * Ruta de Acceso Relativa

**Sistema de Gestión de Archivos**
* Es aquel conjunto de software del sistema que ofrece a los usuarios y aplicaciones, servicios relativos al empleo de archivos.
La única forma en que un usuario o aplicación puede acceder a los archivos es mediante el Sistema de Gestión de Archivos (File System).
Esto releva al usuario o programador de la necesidad de desarrollar software de propósito específico para cada aplicación y proporciona al sistema un medio de controlar su ventaja más importante.

**Tabla de asignación de disco**
* en cada uno de los cuales seguardan tantos números de bloques de disco como quepan. Con bloques de 1Kb y direcciones de 32bits, cada bloque de la  lista  librecontendrá  los  números  de  255  bloques  libres  (se  necesita  una  ranura  para  el  apuntador  al  siguiente  bloque).  

**Tabla de bits**
*  Un  disco  con  n  bloques  requiere  un  mapa  de  bits  con n  bits.  Los  bloqueslibres se marcan con 1 en el mapa y los libres con 0. El mapa de bits requiere menos espacio, puesto que usa un bit por bloque, en comparación con los 32 bits si se usa el modelo de lista enlazada. La elección depende de la cantidad de memoria principal para albergarla lista o el mapa de bits.
