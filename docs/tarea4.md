# Investigación Técnica: Arquitectura de Software

## 1. Métodos HTTP Semánticos

Los métodos HTTP permiten indicar la acción que se desea realizar sobre un recurso dentro de una API REST.

* **GET:** Se utiliza para consultar o recuperar información sin modificar los datos existentes.
* **POST:** Se utiliza para crear nuevos recursos o enviar información al servidor para su procesamiento.
* **PUT:** Se utiliza para actualizar completamente un recurso existente.
* **DELETE:** Se utiliza para eliminar un recurso del sistema.

Estos métodos ayudan a mantener una comunicación clara y estandarizada entre clientes y servidores.

---

## 2. Estructura JSON

JSON significa **JavaScript Object Notation**. Es un formato ligero de intercambio de datos basado en pares clave-valor.

Ejemplo:

```json
{
  "nombre": "Alfredo",
  "edad": 25
}
```

JSON se convirtió en un estándar de la industria porque es más sencillo de leer y escribir que XML, ocupa menos espacio y es compatible con la mayoría de los lenguajes de programación modernos. Además, facilita el intercambio de información entre aplicaciones web y servicios.

---

## 3. Códigos de Error HTTP

Los códigos HTTP permiten identificar el resultado de una petición.

* **4xx:** Errores del cliente (Front-End).
* **5xx:** Errores del servidor (Back-End).

### Error 400 Bad Request

Ocurre cuando la solicitud enviada contiene datos incorrectos o tiene un formato inválido.

### Error 404 Not Found

Ocurre cuando el recurso solicitado no existe o no puede encontrarse en el servidor.

### Error 503 Service Unavailable

Ocurre cuando el servidor está temporalmente fuera de servicio o no puede atender la solicitud debido a problemas internos o sobrecarga.

---

## 4. Especificación OpenAPI (Swagger)

OpenAPI es un estándar utilizado para documentar APIs REST. Su objetivo principal es describir de manera clara los endpoints disponibles, los parámetros que reciben, las respuestas que generan y los posibles errores.

Esta documentación funciona como un plano técnico que facilita la comunicación entre analistas, desarrolladores y equipos de pruebas.

---

## 5. Contratos de Interfaz

En programación orientada a objetos, una interfaz es un conjunto de métodos que una clase debe implementar obligatoriamente.

Se considera un contrato porque define qué operaciones deben existir sin especificar cómo se implementarán. Esto permite desacoplar componentes del sistema y facilita el mantenimiento y la sustitución de implementaciones sin afectar al resto de la aplicación.

---

## 6. Manejo de Excepciones y Resiliencia

Un Stacktrace es el registro detallado de errores generado por una aplicación cuando ocurre una excepción. Muestra la secuencia de llamadas y la ubicación exacta donde ocurrió el fallo.

Nunca debe mostrarse directamente al usuario porque puede revelar información sensible del sistema, como rutas internas, nombres de clases, consultas a bases de datos o detalles de configuración. En su lugar, el sistema debe registrar el error internamente y mostrar mensajes claros y controlados para el usuario.

---

# Análisis del Caso de Estudio

El escenario que más se asemeja a la estructura de contenedores C4 desarrollada para el proyecto de Control de Citas Médicas es el Escenario 1: Cajero Web o Distribuido. Esto se debe a que nuestro sistema está compuesto por diferentes contenedores que se comunican entre sí, como la interfaz web utilizada por los usuarios, la aplicación backend encargada de la lógica de negocio y la base de datos donde se almacena la información. La comunicación entre estos componentes se realiza mediante solicitudes y respuestas, siguiendo una arquitectura similar a la utilizada por las APIs REST que intercambian información utilizando HTTP y JSON.

Además, en el diagrama de contenedores elaborado previamente se identificó una separación clara entre la interfaz de usuario, la lógica de negocio y el almacenamiento de datos. Esta organización coincide con el modelo distribuido mostrado en el caso del cajero automático, donde cada componente tiene responsabilidades específicas y se comunica mediante contratos bien definidos. Gracias a esta separación es posible mejorar la mantenibilidad, escalabilidad y seguridad del sistema, características fundamentales dentro de una arquitectura moderna de software.
