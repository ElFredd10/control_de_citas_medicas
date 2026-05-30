# Tarea 1 - Atributo de Calidad

## Proyecto

Control de Citas Médicas

## Funcionalidad Seleccionada

Agendamiento de citas médicas.

## Atributo de Calidad

Seguridad (Confidencialidad).

## Justificación

El sistema almacena información personal de los pacientes, incluyendo datos de identificación y detalles relacionados con sus citas médicas. Debido a la naturaleza sensible de esta información, es necesario garantizar que únicamente los usuarios autorizados puedan acceder a ella, protegiendo la privacidad de los pacientes y evitando accesos no autorizados.

## Escenario de Calidad

**Estímulo:** Un usuario no autorizado intenta acceder a la información de las citas médicas sin contar con credenciales válidas.

**Respuesta:** El sistema debe rechazar el acceso, registrar el intento en un archivo de auditoría y proteger la información mediante mecanismos de autenticación y control de acceso.

**Métrica:** El 100% de los intentos de acceso no autorizados deben ser bloqueados y registrados por el sistema.
