# Grupo 10		
## Corrección		
	Tag o commit corregido:	lab-3
		
### Entrega y git		100.00%
	Commits de cada integrante	100.00%
	Commits frecuentes y con nombres significativos	100.00%
	En tiempo y con tag correcto	100.00%
### Informe		98.00%
	Informe escrito en Markdown, correctamente formateado, aprovechando las facilidades del lenguaje (numeración, itemización, código, títulos).	100.00%
	Diagrama de jerarquía básico completo (jpeg, ascii, etc.),	100.00%
	Justificación de la jerarquía utilizada (redacción coherente).	100.00%
	Protocolo de mensajes detallado correctamente, y denotando qué mensajes ocurren entre qué actores.	100.00%
	Descripción de responsabilidades de los actores.	100.00%
	Justificación del patrón de interacción escogido.	100.00%
	Pregunta: ¿Por qué es necesario el uso de este patrón de interacción (request/response)?	100.00%
	Pregunta: ¿Qué parte de la arquitectura deberían modificar para soportar el conteo de entidades nombradas?	100.00%
	Pregunta: Para exportar los datos, ¿Qué tipo de patrón de interacción les sirve?	100.00%
	Pregunta: ¿Dónde deberían utilizar dicho patrón para juntar los datos totales? ¿Y por sitio?	100.00%
	Pregunta: ¿Qué problema trae implementar esto de manera síncrona?	80.00%
	Pregunta: ¿Qué les asegura el sistema de pasaje de mensajes y como se diferencia de un semáforo/mutex?	100.00%
### Funcionalidad		67.00%
	Se implementó correctamente `readSubscriptions` y se hace uso para devolver la lista de subscripciones.	100.00%
	El sistema carga todas las subscripciones mediante el pasaje de un mensaje con la lista de subscripciones que devuelve `readSubscriptions`	0.00%
	Se crea un actor "manager" por sitio y un actor por feed.	100.00%
	Se puede hacer request de un feed de un solo sitio en particular mediante el sistema de mensajes.	40.00%
	Se puede hacer request de todos los feeds de un solo sitio mediante el sistema de mensajes.	100.00%
	El request de todos los feeds de un sitio hace uso del request de un sitio en particular mediante un pasaje de mensajes del actor a si mismo.	0.00%
	Para obtener el feed utilizan algún patrón de interacción de request-response.	100.00%
	El contenido de todos los feeds es impreso a nivel sitio/supervisor (i.e. no imprimen a nivel feed).	100.00%
### Modularización y diseño		88.00%
	Los actores se trabajan en archivos separados.	100.00%
	Los protocolos se escriben en el Object Companion de cada actor. Están trabajado utilizando `case class` o `case object` para facilitar el *pattern matching*.	100.00%
	El protocolo de mensajes se hace con herencia entre mensajes de la misma índole (i.e. mensajes del tipo `Request` heredan de un mismo `trait` y lo mismo con mensajes del tipo `Response`).	100.00%
	Hacen *pattern matching* para lidiar con pasaje de mensajes entre actores.	100.00%
	Respetan la jerarquía y el protocolo dado en el informe, no comunican cosas que no tiene sentido que se comuniquen.	100.00%
	Los `var` son usados sólo en el caso de que no hay otra opción (i.e. en caso de colecciones mutable, utilizan la estructura de datos adecuada pero sobre un `val`, no están constatemente sobreescribiendo).	80.00%
	Hacen uso de construcciones de lenguaje funcional (`map`, `filter` y eventualmente `fold`/`reduce` y `flatMap`). Evitan el uso de `flatten`.	100.00%
	No se utiliza la sentencia `try { ... } catch { ... }` y se resuelven las excepciones mediante el uso de la mónada `scala.util.Try` y *pattern matching*.	0.00%
	Las excepciones capturadas mediante *pattern matching* en un `receive` son avisadas a los actores padres de la jerarquía mediante el uso del protocolo de mensajes y no devueltas simplemente como un error.	100.00%
	Cualquier librería "extra" fue correctamente agregada a `build.sbt`/ `project/build.properties` y los plugins están en `project/plugins.sbt`.	100.00%
### Calidad de código		96.00%
	Ninguna línea sobrepasa los 100 caracteres, y sólo unas pocas los 80.	100.00%
	El código es legible, está correctamente indentado (con espacios, no tabs), y con espacios uniformes (i.e. no hay más de dos saltos de línea en ningún lado).	80.00%
	Hacen uso comprensivo de comentarios y documentan partes que sean complejas.	100.00%
	No hay código spaghetti, no utilizan variables *flags* (i.e. variables que guarden valores temporales para ser utilizadas más adelante como un booleano).	100.00%
	Evitan el uso de `return` en las funciones.	100.00%
### Opcionales		
	Punto estrella: Subscripción a Reddit/Json	100.00%
	Punto estrella: Conteo de entidades nombradas	0.00%
	Punto estrella: Guardar datos a disco	0.00%
	Punto estrella: Esperar proceso de datos	0.00%
	Punto estrella: Rest API	0.00%
		
# Nota Final		9.154
		
		
# Comentarios		
	Originalmente habían implementado el mensaje para pedir sólo un feed, pero luego decidieron sacarlo y justificaron por qué en el informe	

