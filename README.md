Reto Técnico para Analista de Automatización de Servicios

Este proyecto tiene como objetivo automatizar llamadas a la API del sitio web Reqres utilizando las siguientes tecnologías y herramientas:
Objetivo

Automatizar un conjunto de llamadas a la API mediante:

    RestAssured: Para consumir y validar las respuestas de los endpoints.
    Serenity BDD: Para generar reportes detallados de las pruebas.
    Patrón Screenplay: Para estructurar y organizar las pruebas.
    Cucumber: Para escribir pruebas en lenguaje natural utilizando Gherkin.
    Postman: Para mapear y probar los endpoints previamente.

Detalles del Proyecto
URL Base

https://reqres.in
Endpoints Implementados
Método	            URI	                        Descripción
GET	                /api/users?page=2	        Listar usuarios.
POST	            /api/users	                Registrar un nuevo usuario.
PUT	                /api/users/2	            Actualizar información de un usuario.
DELETE	            /api/users/2	            Eliminar un usuario.

Funciones Automatizadas

    GET: Validar que la respuesta contenga al menos un usuario.
    POST: Crear un nuevo usuario y validar la respuesta.
    PUT: Actualizar un usuario existente.
    DELETE: Eliminar un usuario y verificar la operación.

Tecnologías Utilizadas
Tecnología	        Versión
Java	            OpenJDK 17.0.13
Gradle	            8.4
Frameworks	        Serenity-Rest, Cucumber, Gherkin, JUnit
Diseño	            Screenplay
IDE	                IntelliJ IDEA Community Edition 2024.3


Pasos para la Ejecución
Opción 1: Ejecución desde la Consola

    Limpiar el proyecto y ejecutar todos los escenarios:

./gradlew clean test

Ejecutar un archivo específico de Runner (ejemplo: GetRunner):

./gradlew test --tests "co.com.screenplay.project.runners.GetRunner"

Ejecutar todos los Runners:

./gradlew test --tests "co.com.screenplay.project.runners"

Generar el reporte después de ejecutar los tests:

    El comando generará un archivo .html con el reporte.

./gradlew reports

Limpiar los reportes generados en la carpeta target:

    ./gradlew clearReports

Características del Proyecto

    Patrón Screenplay: Estructura el código para que sea fácil de mantener y leer.
    Serenity Reports: Genera reportes detallados con gráficos y estadísticas.
    Cucumber/Gherkin: Permite escribir pruebas legibles en lenguaje natural para facilitar la colaboración con el equipo.

Instrucciones Adicionales

    Asegúrate de tener configurado Gradle y Java en tu sistema.
    Puedes explorar los reportes generados navegando a:

build/reports/tests/test/index.html

Si tienes problemas con la configuración inicial, revisa los archivos build.gradle y serenity.properties.
