# PESTAÑA PRINCIPAL 
## Push & Pull 7_Trabajo Divergente_

Iniciamos el segundo de los ejercicios asignados, que, como podemos ver, recibe el nombre de _trabajo divergente_. Antes de proceder con su desarrollo, y como de costumbre, realicemos una introducción al ejercicio para ponernos en contexto:

Esta es la ventana inicial con la cual la web comienza la practica:

![Alt text](introduccion1.jpg)

Como podemos leer, una vez entendidos los conceptos asociados al pull de commits y el pusheo de los mismos, el ejercicio va a orientarnos respecto a que tipo de recursos o herramientas podemos utilizar si en un momento dado el desarrollador o los integrantes que están realizando el proyecto tiene puntos o eventos de desarrollo que pueden dar lugar a conflicto con la linea principal de trabajo.

Pero todo este concepto vemos que estará englobado desde el punto de vista organizativo de repositorios, el cómo podemos gestionarlos para tratar lo menos posible o evitar cambios indeseados de trabajo ya desarrollado.

Aún así, vamos a continuar con esta parte introductoria para ver que nos pretende enseñar la plataforma, si hacemos click al boton de 'siguiente' :

![Alt text](introduccion2.jpg)

Aqui podemos entender mucho mejor el contexto en el que nos encontramos.

Cuando un desarrollador, partiendo de un repositorio base trabajo, realiza el conjunto de tareas que se le han sido asignados puede ocurrir que, paralelamente, al ser proyectos que generalmente son grupales, exista un equipo que haya modificado, creado o incluso eliminado parte del codigo o trabajo que este desarrollador ha tenido que realizar por ser su tarea trabajo. 

No porque haya hecho mal su trabajo (que puede ser) sino por la mera evolucion temporal del proyecto que, como sabemos, está sujeto día si y día tambien a continuos cambios y actualizaciones por su propio desarrollo mismo.

Todo este conjunto de modificaciones y entregas de proyecto han hecho que el trabajo del desarrollador, por asi decirlo, carezca de validez a nivel de desarollo, ya que, en comparación a los ultimos cambios que se han ido realizando, éste ya ha quedado desactualizado.

¿Como responde GIT ante estas situaciones? Esto es lo que nos pregunta la plataforma.

Fuera de toda duda, lo primero que uno puede percibir es que existirá una gran desorganización a nivel de repositorios entre el trabajo que el desarrollador ha realizado, el que ha sido modificado ajenamente, y hasta incluso el entregado paralelamente, etc...

Como vemos, GIT _NO NOS PERMITIRÍA_ entregar el trabajo que seguramente nos haya costado realizar, sino que nos obligaría a adaptarnos a la situacion mas actual del repositorio que tomamos como base para poder asi, si queremos, integrar el codigo que éste ha desarrollado.

Cualquier persona puede ver que esto sería un nido de conflictos de archivos y código, entre lo que uno ha hecho como parte de su trabajo y lo que se ha realizado paralelamente si no se ha tenido un feedback correcto entre ambas partes.

Aun así, hagamos click en siguiente para ver que más nos tiene que enseñar la web:

![Alt text](introduccion3.jpg)

¡Pero bueno, si pasamos ya a la acción!

Continuemos pues a ver este concepto en accion:

Si hacemos click al boton siguiente de la anterior imagen, podemos apreciar que nuestro commit, (c3), GIT lo ha rechazado por que, como nuestro commit está vinculado al commit remoto c1, al haberse éste ultimo actualizado (a c2), nuestra entrega es automáticamente rechazada por hacer referencia, como deciamos, a una entrega desactualizada.

![Alt text](introduccion4.jpg)

Esto tiene muy facil arreglo, y la web nos los enseña a continuación:

![Alt text](introduccion5.jpg)




