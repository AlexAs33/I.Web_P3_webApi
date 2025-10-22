# Lab 3 Complete a Web API -- Project Report

## Description of Changes  
Se completaron los tests unitarios en el fichero `ControllerTests.kt` correspondientes a los métodos del API REST `EmployeeController`.  
Se añadieron los bloques **SETUP** y **VERIFY** para los métodos `POST`, `GET`, `PUT` y `DELETE`, utilizando las configuraciones y verificaciones proporcionadas en las instrucciones del laboratorio.  
En concreto:  
- Para `POST`, se simuló la creación de empleados con IDs diferentes para comprobar que no es idempotente.  
- Para `GET`, se simuló la recuperación de empleados existentes y no existentes, verificando que la operación es segura e idempotente.  
- Para `PUT`, se configuró el repositorio para devolver primero vacío y luego el empleado creado, validando su idempotencia.  
- Para `DELETE`, se permitió la llamada a `deleteById` y se verificó que la operación es idempotente pero no segura.  

## Technical Decisions  
Se decidió seguir estrictamente los bloques de configuración (`every`, `andThenAnswer`, `justRun`) y verificación (`verify`) proporcionados en el enunciado, evitando cualquier modificación adicional de la lógica.  
También se mantuvo el uso de **MockK** para simular el comportamiento del repositorio, y se utilizaron las herramientas estándar de **Spring Boot Test** y **MockMvc** para realizar las peticiones HTTP simuladas.  
Esta decisión permitió garantizar la coherencia con las pruebas automáticas del laboratorio y mantener la trazabilidad entre la teoría (métodos seguros e idempotentes) y la práctica (comportamiento del API).  

## Learning Outcomes  
- Comprendí la diferencia entre **operaciones seguras** y **operaciones idempotentes** en una API REST.  
- Aprendí a utilizar **MockK** para simular respuestas del repositorio y verificar interacciones específicas.  
- Reforcé el uso de **MockMvc** para probar controladores REST sin necesidad de levantar un servidor real.  
- Entendí cómo las pruebas automáticas pueden validar conceptos teóricos de diseño web (seguridad e idempotencia) a través de código práctico.  

## AI Disclosure  

### AI Tools Used  
- ChatGPT (modelo GPT-5 de OpenAI)

### AI-Assisted Work  
- La IA me orientó sobre cómo aplicar correctamente los bloques de código proporcionados en las instrucciones del laboratorio.  
- Me ayudó a estructurar el contenido de los métodos de prueba (`SETUP` y `VERIFY`), respetando las reglas del ejercicio. 
- Las modificaciones y adaptaciones finales del código fueron realizadas manualmente, ajustando la sintaxis y comprobando la coherencia con el proyecto.  

### Original Work  
- La integración del código, las ejecuciones de prueba y la comprensión del funcionamiento del controlador REST fueron realizadas de forma independiente.  
- Analicé el comportamiento esperado de cada operación (POST, GET, PUT, DELETE) y confirmé que las pruebas reflejan correctamente los conceptos de seguridad e idempotencia.  
- Este proceso me permitió afianzar la relación entre teoría REST y la práctica en **Spring Boot con Kotlin**.
