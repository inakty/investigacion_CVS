#Características

1. Arquitectura cliente-servidor: 
	* El servidor guarda la(s) versión(es) actual(es) del proyecto y su historial (una version consolidada del proyecto). 
	* El cliente o estacion de trabajo hace modificaciones al codigo y realiza las pruebas necesarias para satisfacer los requerimientos. Los clientes se conectan al servidor para sacar una copia completa del proyecto, esto se hace eventualmente para que puedan trabajar con esa copia y más tarde ingresar sus cambios.
	* Debe exitir comunicacion entre cliente y el servidor al realizar operaciones CVS como checkins o actualizaciones, pero si se quiere editar o manipular las versiones actuales de los archivos los clientes pueden bajar una copia y realizar las operaciones disponibles a nivel local.

2. Mantiene el registro de la historia de las versiones del programa de un proyecto solamente con desarrolladores locales.

3. Originalmente, el servidor utilizaba un sistema operativo similar a Unix, aunque en la actualidad existen versiones de CVS en otros sistemas operativos como Windows.

4. Si se actualizan modificaciones, el servidor trata de acoplar las diferentes versiones. *(Si esto falla, por ejemplo debido a que dos clientes tratan de cambiar la misma línea en un archivo en particular, entonces el servidor deniega la segunda actualización e informa al cliente sobre el conflicto, que el usuario deberá resolver manualmente.)* Si la operación de ingreso tiene éxito, entonces los números de versión de todos los archivos implicados se incrementan automáticamente, y el servidor CVS almacena información sobre la actualización, que incluye:

5. Descripción suministrada por el usuario
	* Fecha 
	* Nombre del autor
	* Archivos de registro (log) del autor.

6. CVS también puede mantener distintas "ramas" *(revisiones paralelas de un modulo para efectuar cambios sin tocar la evolucion principal. Se suele emplear para pruebas o para mantener cambios en versiones viejas)* de un proyecto. Por ejemplo, una versión difundida de un proyecto de programa puede formar una rama y ser utilizada para corregir errores. Todo esto se puede llevar a cabo mientras la versión que se encuentra actualmente en desarrollo y posee cambios mayores con nuevas características se encuentre en otra línea formando otra rama separada.

7. Cada archivo tiene un numero de revision independiente, este numero registra el numero de cambios hechos al archivo y no tiene ninguna relacion con algun numero de version del proyecto completo. 

8. En los casos en que varios desarrolladores o equipos requieran una versión de los archivos y, debido a la geografía o la política no puedan adquirirlo; pueden importar una versión de otro equipo **(incluso si no utilizan CVS)**, y luego CVS puede combinar los cambios de la rama de proveedor con los últimos archivos si eso es lo que se desea.

9. Proporciona una base de datos de módulos flexibles que ofrece una correspondencia simbólica de los nombres a los componentes de una distribución de software más grande, (esto se aplica a las colecciones nombres de directorios y archivos, ***UN SOLO COMANDO PUEDE MANIPULAR TODA LA COLECCION.***)

10. Los clientes pueden
	* Comparar diferentes versiones de archivos.
	* Solicitar una historia completa de los cambios.
	* Sacar una "foto" histórica del proyecto tal como se encontraba en una fecha determinada o en un número de revisión determinado. 
	* Utilizar la orden de actualización con el fin de tener sus copias al día con la última versión que se encuentra en el servidor (esto elimina la necesidad de repetir las descargas del proyecto completo).
	* Funcionar en cualquiera de los sistemas operativos más difundidos.
	* Sacar copias YOU del proyecto al mismo tiempo.
	* Sacar y comparar versiones sin necesidad de teclear una contraseña en proyectos de código abierto *("acceso de lectura anónimo")*.Solamente el ingreso de cambios requiere una contraseña en estos casos.


# Limitaciones de CVS
1. Los archivos en el repositorio sobre la plataforma CVS no pueden ser renombrados, estos deben ser agregados con otro nombre y luego eliminados.

2. El protocolo CVS no provee una manera de que los directorios puedan ser eliminados o renombrados, cada archivo en cada subdirectorio debe ser eliminado y re-agregado con el nuevo nombre. 

3. Soporte limitado para archivos Unicode con nombres de archivo no ASCII.

4. Actividades como la planificacion, los releases, etc, quedan fuera de su ambito de trabajo y deben ser abordadas por las personas y otras herramietnas complementarias
