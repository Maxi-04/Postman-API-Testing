<h1 align="left">Proyecto de pruebas de API usando Postman 🧪</h1>

###

<h2 align="left">Este repositorio contiene una colección de Postman que implementa una suite de pruebas automatizadas para la API de Trello. El objetivo es validar la funcionalidad, integridad de los datos y el manejo de errores de los endpoints clave, siguiendo un enfoque de flujo de trabajo de usuario final (end-to-end).<br><br>Índice<br><br>1. Requisitos<br>2. Configuración del Entorno<br>3. Estructura del Proyecto<br>4. Ejecución de las Pruebas<br>5.Casos de Prueba</h2>

###

<p align="left">1. Requisitos 📝<br><br>Para ejecutar esta suite de pruebas, necesitas:<br><br>● Postman Desktop App<br>● Credenciales de la API de Trello:<br>● Key (Clave de desarrollador)<br>● Token (Token de usuario)<br><br>Puedes obtenerlas en la página de desarrolladores de Trello.</p>

###

<h2 align="left"></h2>

###

<p align="left">2. Configuración del Entorno ⚙<br><br>● Descarga e importa la colección de Postman (Test Suite.postman_collection.json) en tu aplicación Postman.<br>● Crea un nuevo entorno en Postman con el nombre que prefieras <br>● Agrega las siguientes variables a tu entorno, rellenando los valores iniciales y actuales con tus credenciales y datos de prueba:</p>

###

<p align="left"></p>

###

<div align="left">
</div>

###

<div align="center">
  <img height="450" src="https://i.postimg.cc/cCn4CXPV/chrome-Ky-TO6-Vy-Gm3.png"  />
</div>

###

<p align="left">Reemplaza los valores con los datos correspondientes de tu propio tablero de Trello.</p>

###

<p align="left">3. Estructura del Proyecto 📈<br><br>La colección está organizada en las siguientes carpetas, cada una con un propósito específico:<br><br>● Flujo E2E - Tarjeta Trello: Contiene una serie de peticiones encadenadas que simulan un flujo de usuario completo: crear, validar, editar, mover y eliminar una tarjeta.<br><br>● Validaciones de Datos JSON: Incluye casos de prueba más complejos, como la verificación de respuestas de error (casos negativos).<br><br>● Pruebas de Poke API: Ejemplos de pruebas funcionales y de validación de datos en una API pública, que demuestran la capacidad de trabajar con diferentes APIs.</p>

###

<p align="left">4. Ejecución de las Pruebas 🚀<br><br>Para ejecutar la suite completa:<br><br>✔ Abre el Runner de Postman.<br><br>✔ Selecciona la colección Test Suite y el entorno Trello API Environment.<br><br>✔ Haz clic en Run.<br><br>Postman ejecutará cada petición en orden, y los resultados de las pruebas se mostrarán en un reporte detallado.</p>

###

<p align="left">5. Casos de Prueba ✔<br><br>A continuación, se detallan los principales casos de prueba incluidos en la colección:<br><br>📌 Flujo E2E - Tarjeta Trello<br> <br>Crear Card | Verificar la creación exitosa de una tarjeta | Estatus 200, id de tarjeta guardado en variable de entorno.<br>Validar Creación | Asegurar que la tarjeta creada existe y está en la lista correcta | Estatus 200, nombre de tarjeta correcto, idList de la Lista A. <br>Editar Card | Cambiar el nombre de la tarjeta | Estatus 200, el nombre de la tarjeta se actualizó correctamente <br>Mover a Lista B | Mover la tarjeta a una nueva lista | Estatus 200, el idList de la tarjeta corresponde a la Lista B<br>Eliminar Card | Eliminar la tarjeta creada. | Estatus 200<br>Validar Eliminación | Confirmar que la tarjeta fue eliminada | Estatus 404 Not Found<br><br>📌 Validaciones de Datos JSON<br><br>Validar Esquema de Card | Confirmar que la estructura de la respuesta de la API es la esperada |<br>Validar Card Inexistente | Verificar el manejo de errores de la API | Estatus 404 Not Found | Validar propiedades de un objeto | Buscar propiedades y valores <br><br>📌 Pruebas de Poke API <br><br>Practica Pokemon | Validar la integridad de los datos de un endpoint | Estatus 200, nombre del Pokémon correcto, validación de propiedades booleanas, y validación de arrays</p>

###
