# Diccionario de Datos

## Sistema de Control de Citas Médicas

### Tabla: Pacientes

| Campo            | Tipo de Dato | Llave | Descripción                      |
| ---------------- | ------------ | ----- | -------------------------------- |
| id_paciente      | INT          | PK    | Identificador único del paciente |
| nombre           | VARCHAR(100) |       | Nombre completo del paciente     |
| telefono         | VARCHAR(15)  |       | Número telefónico                |
| correo           | VARCHAR(100) |       | Correo electrónico               |
| fecha_nacimiento | DATE         |       | Fecha de nacimiento              |

---

### Tabla: Medicos

| Campo        | Tipo de Dato | Llave | Descripción                    |
| ------------ | ------------ | ----- | ------------------------------ |
| id_medico    | INT          | PK    | Identificador único del médico |
| nombre       | VARCHAR(100) |       | Nombre completo del médico     |
| especialidad | VARCHAR(100) |       | Especialidad médica            |
| telefono     | VARCHAR(15)  |       | Número de contacto             |

---

### Tabla: Citas

| Campo       | Tipo de Dato | Llave | Descripción                    |
| ----------- | ------------ | ----- | ------------------------------ |
| id_cita     | INT          | PK    | Identificador único de la cita |
| fecha_cita  | DATETIME     |       | Fecha y hora de la cita        |
| motivo      | VARCHAR(200) |       | Motivo de consulta             |
| estado      | VARCHAR(20)  |       | Estado de la cita              |
| id_paciente | INT          | FK    | Referencia al paciente         |
| id_medico   | INT          | FK    | Referencia al médico           |

---

## Relaciones

* Un paciente puede tener muchas citas.
* Un médico puede atender muchas citas.
* Una cita pertenece a un único paciente.
* Una cita pertenece a un único médico.
