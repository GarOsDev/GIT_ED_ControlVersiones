# PESTAÑA PRINCIPAL 
## Un poco de todo_EJERCICIO 5

En este quinto ejercicio, la plataforma tratará de enseñarnos un nuevo comando/concepto conocido como _git describe_

Y uno podrá preguntarse, ¿Qué es Git Describe?, bien, en primer lugar vamos a intentar describirlo con nuestras palabras, aunque luego enseñaré cómo trata de explicarnos la plataforma esta nueva utilidad de GIT.

## _ENTENDIENDO GIT DESCRIBE_

Partiendo de un proyecto ya comenzado, puede pasar que nos sintamos perdidos o no sepamos en que punto de desarrollo exacto éste se encuentre, o también, por que no, saber cada uno de los cambios que se han ido realizando a lo largo de su proceso de desarrollo.

Como recordaremos, cada vez que queramos remarcar un hecho o punto importante del proyecto, haremos uso de lo que conocemos como **tags**, gracias a estos, podremos situarnos rapidamente en aquellos cambios importantes que se han ido remarcando a lo largo del mismo.

Pues bien, GIT, a partir de este **hito** (tag) determinado, con el uso de >git describe< se proporcionará toda la información necesaria para saber en que punto del proyecto nos encontramos con respecto al tag mas cercano, para así nos resulte mucho mas facil "situarnos" durante el proceso de desarrollo. **Esto es especialmente util cuando nos hemos ido moviendo entre distintas entregas (commits)**. En lineas posteriores analizaremos en detalle cual será dicha información proporcionada.

A continuación muestro cómo trata de enseñarnos la web este concepto, y comenzaremos a realizar el ejercicio propuesto:

![Alt text](Fotografias/Introduccion.jpg)

## EJECUCION DE COMANDO _GIT DESCRIBE_

Una vez tenemos una idea aproximada sobre en qué consiste el comando _git describe_, tendremos que saber como usarlo correctamente en nuestro terminal GIT. En esta ocasión, vamos a mostrar como nos lo enseña la plataforma y posteriormente trataremos de razonar su funcionamiento:

![Alt text](Fotografias/Introduccion_funcionamiento.jpg)

Como podemos enteder, para poder hacer uso de este comando, necesitaremos proporcionar al comando un parámetro **<ref>** o referencia, que es el que tomará GIT para decirnos a cuantos commits nos encontramos del **tag** mas cercano. Nos informa la web que si no le proporcionamos ninguna referencia como parámetro, GIT automaticamente nos situará en el commit mas cercano.

Una vez resuelto el comando con referencia dada, la salida por consola mostrará el siguiente formato:

![Alt text](Fotografias/Introduccion_comandoSalida.jpg)

Donde **numCommits** será la cantidad de entregas que se han realizado **desde el tag mas cercano** hasta el commit de referencia con respecto al tag y el **hash** (una especie de "firma" hexadecimal abreviado) que está haciendo referencia al commit respectivo.

# ENTENDIENDO EJEMPLO PRÁCTICO 

Una vez hemos hecho la introducción teórica a este nuevo comando GIT, he decidido mostrar, antes de proceder a resolver el ejercicio propuesto, un ejemplo práctico que nos propone la plataforma, y es el siguiente:

![Alt text](Fotografias/ejemploPractico1.jpg)

Vemos como, para la evolución de proyecto mostrado, estamos en la branch side (por su asterisco). A continuación el programa nos muestra por consola el resultado del comando **git describe** aplicado a **main** y a la rama **side**:

![Alt text](Fotografias/ejemploPractico2.jpg)

Y aqui podemos ver claramente el funcionamiento y formato de este comando:

### main

Si escribimos por consola **git describe main** estaríamos situándonos en el ultimo commit de la rama master obteniendo el siguiente resultado: **v1_2_gC2**

¿Que significa cada valor?:

- v1: para main, v1 sería el **tag** o evento o "hito" mas cercano. Es por ello por lo que lo toma como referencia en la evolución de tipo jerárquica.
- 2: valor numérico 2, serían la cantidad de commits o "entregas" que existen en el rango hasta v1.
- gC2: para el commit C2 de main, su hash representativo.

### side

¿Y para la rama creada side? Vemos que obtenemos como resultado **v2_1_gC4**. Aplicando el razonamiento anterior, averigüemos que significa cada valor:

- v2: como podemos ver, basandonos en el diagrama, v2 sería el **tag** de referencia.
- 1: valor numerico 1, esto es el numero de entregas existentes desde el tag v2 hasta donde estamos c4 (side asterisco), que como podemos contar sería una única entrega.
- gc4: el hash del commit indicado, es decir el commit 4 de la rama side.

Y una vez mostrada esta pequeña introducción práctica, la web nos conduce a la resolución del ejercicio:

![Alt text](Fotografias/ejemploPracticoFinal.jpg)

# RESOLVIENDO EJERCICIO

- Comienzo el ejercicio propuesto partiendo desde la siguiente situación:

![Alt text](Fotografias/ResolEjercicio1.jpg)

Tal y como nos indica el cuadro de comandos, tendremos que hacer un commit de bugFix para finalizar el ejercicio, por ello escribimos **git commit**, para hacer una entrega del mismo:

![Alt text](Fotografias/ResolEjercicio2.jpg)

![Alt text](Fotografias/ResolEjercicio3.jpg)

Y sencillamente con este comando, la web nos indica que hemos resuelto el ejercicio exitosamente:

![Alt text](Fotografias/ResolEjercicioX.jpg)

Pero no nos quedemos aqui, para poder ver como aplicamos el comando que acabamos de aprender, voy a escribir por linea de comando un ejemplo para **git describe c7**. Obtenemos el siguiente resultado:

![Alt text](Fotografias/ResolEjercicioXY.jpg)

Obtenemos **v1_3_gC7**

- v1: para la rama bugFix, el tago o hito de referencia
- 3: número de commits desde el tag v1 hasta el punto en el que nos encontramos (c7), que como podemos contar serían 3.
- gC7: el hash del commit donde actualmente nos escontramos.

Con esto, hemos visto como el comando _git describe_ puede sernos muy util para saber un punto importante de las ramas de proyecto, sobre todo para saber procesos del desarrollo que se han considerado relevantes o también desde donde podríamos continuar nuestro trabajo. 

Un comando, sin duda, a tener muy en cuenta.