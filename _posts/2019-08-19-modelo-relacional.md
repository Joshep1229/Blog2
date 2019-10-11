---
title: ¿Porqué un modelo relacional es mejor que múltiples buscarv para analizar la información?
---
![Test](/emerald/img/img-test.png "Test")

Este artículo será el inicio de una serie de artículos que explorarán la importacia de Seleccionar (1), ordenar/(2) manipular , (3)visualizar y analizar los datos, todo ello con ejemplos prácticos y sencillos, en la fase inicial exploraré la importancia de seleccionar las fuentes de información adecuadas para tener un modelo de datos sostenible y significante.

Un modelo perfecto de información (que incluya IMPORT, TIDY, TRANSFORM, VISUALIZE, AND MODEL DATA, dados en el libro de R for data science de Hadley Wickam) fallará si en la fase de selección escogemos datos que luego no puedan ser actualizados y contrastados constantemente.

En la fase de selección nos damos cuenta que estas bases de datos son muy distintas a las disponibles que Kaggle y que el hecho de seleccionar la data es retador, y preguntas como ¿con qué datos quieres trabajar?, ¿son de fácil acceso y actualización? son muy importantes, y si sabes seleccionar las bases podrás introducir nuevos datos al modelo sin afectarlo y esto te permitirá que este viva a través del tiempo.

Un modelo con las fuentes de datos correctamente seleccionadas será la base para conexiones relacionales que nos permitan ver varias dimensiones de los datos, esto evitará por ejemplo hacer múltiples "buscarv" -cada x días- entre un archivo de excel de ventas y otro de clientes para saber si se vieron influenciados por el gasto en publicidad, en su lugar solo tendrás que actualizar la información y esperar que el modelo te dé los resultados (lo puedes hacer en softwares como DataStudio, PowerBI o Tableau, etc). Herramientas como estas nos permitirán aumentar el tiempo de análisis y disminuir el de procesamiento.

Voy a poner un ejemplo de lo que lograrías si sabes escoger los datos correctos, en este caso voy a hacer el ejemplo en PowerBI, pero también lo podrás hacer en herramientas ya seleccionadas.

¿Cómo seleccionar los datos en PowerBI?

En este caso vamos a tener dos carpetas, una con los archivos de las ventas registradas de la compañía X y otro de la inversión de publicidad de la misma, la importancia de la selección de datos es clave para que todo el trabajo de cargar y conectar las relaciones entre las bases, pueda ayudarnos através del tiempo.

Vamos a abrir el programa y le damos click en obtener datos, allí verás un panel.
No hay texto alternativo para esta imagen
No hay texto alternativo para esta imagen
En este punto podrás ver todas las fuentes disponibles que puedes conectar, hay infinidad de bases como las de Google analytics, excel o carpeta, vamos enfocarnos en esta última.

Cabe aclarar que en este caso solamente nos servirá para cosas que tengamos en nuestro computador, aún así, si tus datos se guardan en la nube puedes optar por la opción de carpeta de sharepoint. Al seleccionar la opción , te pedirá que la busques tal como exportas una foto en facebook

No hay texto alternativo para esta imagen
Luego al seleccionarla, esta leerá la estructura de los archivos y te preguntará si los quieres combinar, esto es especialmente útil cuando tienes múltiples base de datos que mantienen la misma estructura, así podrás guardar los archivos en la misma carpeta y el el programa los leerá de forma automática, esto evita que tengamos que tener un arhivo madre que tenga un montón de información que generalmente se va pegando en excel y va acumulando errores de tipeo perdiendo así información valiosa.

Aquí le damos combinar y cargar, luego de ello seleccionamos la hoja referencia, que es la base paramantener la estructura de datos.

No hay texto alternativo para esta imagen


Luego de estos dos pasos, ya tendremos nuestra primera base cargada.

Finalmente repetimos la acción con otro archivo que tendrá los datos de publicidad, cuya llave será el departamento, esto nos permitirá resolver preguntas como ¿cuánto es el ROI de la publicidad en general y por departamentos de la compañía?.

Luego debemos repetir el proceso con otra carpeta que contiene los archivos de gastos de publicidad y darle click al botón en la parte izquierda de la imágen nos aparecerán las bases cargadas por el sistema y las relaciones o las ausencias de estas..


Estas relaciones tienen una cardinalidad que revisa si es varios a uno (una base de datos con valores únicos y otra con valores múltiples), uno a uno (únicos registros en las dos tablas) o varios a varios (no necesitas valores únicos que en general, es la mas recomendada).

Finalmente la cardinalidad es cómo se filtran los datos de la tabla, generalmente funciona bien dejando "ambas", pero hay particularidades para dejarla en "única", en este archivo se explica al detalle.

Esta base conectada, equivale a tener una tabla que tiene tanto el gasto de publicidad como el monto gastado y que se podrá actualizar fácil y rápidamente (solamente pegando los archivos nuevos a la carpeta ya existente).

Luego de esta relación podremos pasar a ordenar los datos en las bases (ordenar categorías de interés, manipular las columnas para filas personalizadas de datos de nuestro interés etc) esto nos ayudará a visualizar información importantes de múltiples fuentes en un solo tablero, este será el foco detalle de los siguientes posts.

Un saludo.



