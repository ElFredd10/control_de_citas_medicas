# Avance 1 - Propuesta Inicial de Arquitectura de Software

## 1. Descripción del Sistema y Objetivos Esenciales

### Contexto del Negocio

Muchas clínicas pequeñas continúan gestionando sus citas médicas mediante agendas físicas o registros manuales. Este método puede generar errores de programación, pérdida de información y duplicidad de citas. Para resolver esta problemática se propone el desarrollo de un Sistema de Control de Citas Médicas que permita administrar de forma digital el registro de pacientes, médicos y citas.

### Objetivo General del MVP

Desarrollar un sistema web que permita registrar pacientes, registrar médicos, programar citas y consultar información relacionada con las mismas. El Producto Mínimo Viable (MVP) demostrará la funcionalidad básica necesaria para administrar citas médicas de manera eficiente.

### Expectativas del Usuario

Los usuarios principales serán el personal administrativo de la clínica y los médicos. El personal administrativo espera poder registrar y consultar citas rápidamente, mientras que los médicos requieren acceder a la información de sus citas programadas de forma organizada y confiable.

---

## 2. Matriz de Atributos de Calidad Prioritarios

### Seguridad

#### Definición e Impacto

La seguridad es fundamental debido a que el sistema almacena información personal de pacientes y médicos. Es necesario proteger los datos contra accesos no autorizados.

#### Escenario de Arquitectura

Si un usuario intenta acceder a información sin autenticarse correctamente, el sistema deberá bloquear el acceso y registrar el intento para auditoría.

---

### Disponibilidad

#### Definición e Impacto

El sistema debe permanecer disponible para que las citas puedan registrarse y consultarse durante el horario de operación de la clínica.

#### Escenario de Arquitectura

Si la base de datos MySQL pierde conexión durante 10 minutos, el sistema mostrará un mensaje de indisponibilidad temporal y evitará operaciones que puedan comprometer la integridad de los datos hasta restablecer la conexión.

---

### Rendimiento

#### Definición e Impacto

Las consultas y registros de citas deben ejecutarse rápidamente para evitar retrasos en la atención de los usuarios.

#### Escenario de Arquitectura

Una búsqueda de citas por paciente deberá responder en pocos segundos aun cuando existan cientos de registros almacenados.

---

### Mantenibilidad

#### Definición e Impacto

El sistema debe permitir futuras mejoras y correcciones sin afectar significativamente el funcionamiento existente.

#### Escenario de Arquitectura

La incorporación de nuevos módulos, como expedientes clínicos o reportes avanzados, deberá realizarse con cambios mínimos en la estructura principal del sistema.

---

## 3. Propuesta de Estilo y Patrón Arquitectónico

### Estilo Arquitectónico Seleccionado

Se propone una arquitectura Cliente-Servidor implementada mediante un Monolito en Capas.

### Justificación de Ingeniería

La arquitectura Cliente-Servidor permite separar la interfaz de usuario, la lógica de negocio y la base de datos. Esta organización facilita el mantenimiento, mejora la seguridad y permite administrar adecuadamente las operaciones relacionadas con pacientes, médicos y citas.

Además, el uso de un Monolito en Capas resulta adecuado para un MVP debido a que simplifica el desarrollo, despliegue y administración del sistema. Las llamadas entre capas se realizan localmente dentro de la aplicación, reduciendo la complejidad asociada a arquitecturas distribuidas y permitiendo una implementación más rápida dentro del tiempo disponible para el proyecto.

La propuesta también favorece atributos de calidad como mantenibilidad, rendimiento y disponibilidad, ya que cada capa posee responsabilidades claramente definidas y puede evolucionar de manera controlada conforme el sistema crezca.

---

## Conclusión

La propuesta arquitectónica presentada proporciona una base sólida para el desarrollo del Sistema de Control de Citas Médicas. La combinación de una arquitectura Cliente-Servidor con un modelo Monolítico en Capas permite satisfacer los requerimientos funcionales del MVP, manteniendo un equilibrio adecuado entre simplicidad, rendimiento, seguridad y facilidad de mantenimiento.
