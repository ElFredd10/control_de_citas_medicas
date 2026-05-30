# Tarea 2 - Estilo Arquitectónico

## Proyecto

Control de Citas Médicas

## Funcionalidad Seleccionada

Agendamiento de citas médicas.

## Estilo Macro

Arquitectura en Capas.

## Estilo Interno

Modelo Vista Controlador (MVC).

## Boceto del Flujo Crítico

Paciente
↓
Interfaz de Usuario
↓
Controlador de Citas
↓
Servicio de Agendamiento
↓
Base de Datos

## Justificación

Se eligió la Arquitectura en Capas porque permite dividir el sistema en componentes con responsabilidades específicas, facilitando el mantenimiento y la escalabilidad.

Como estilo interno se seleccionó MVC, ya que separa la interfaz de usuario, la lógica de negocio y el acceso a datos, permitiendo una mejor organización del código.

Esta arquitectura contribuye al atributo de calidad de Seguridad definido en la Tarea 1, ya que centraliza las validaciones de acceso y protege la información de los pacientes mediante controles adecuados en cada capa.


