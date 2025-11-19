# Sistema de Agenda Personal de Citas (Caso Práctico 2)

[cite_start]Este repositorio alberga la documentación de ingeniería de software generada para la **Agenda Personal de Citas** [cite: 122][cite_start], una aplicación diseñada para gestionar de forma eficiente los compromisos personales del usuario[cite: 124].

## 1. Descripción y Objetivos

[cite_start]El objetivo principal es facilitar a un único usuario [cite: 134] [cite_start]la creación, modificación, eliminación y consulta de citas, además de recibir recordatorios automáticos[cite: 125].

* [cite_start]**Alcance:** Registro completo de citas, visualización por día/semana/mes, recordatorios por notificación/correo, y soporte para modo offline con sincronización[cite: 127, 128, 129].

## 2. Requerimientos Clave

| Código | Descripción del Requerimiento |
| :--- | :--- |
| **RF1/RF2** | [cite_start]Permitir crear, editar y eliminar citas con detalles como título, fecha, hora y ubicación[cite: 138]. |
| **RF7** | [cite_start]El sistema debe **advertir sobre solapamientos de horario** al crear o modificar citas[cite: 140, 147]. |
| **RNF3** | [cite_start]El sistema debe ser accesible **sin conexión a internet (modo offline)** y sincronizar automáticamente al recuperar la conexión[cite: 142]. |
| **RNF4** | [cite_start]El tiempo de respuesta al cambiar de vista (día/semana/mes) debe ser **inferior a 1 segundo**[cite: 142]. |

## 3. Pruebas Funcionales

Las pruebas se enfocaron en los puntos críticos de la agenda:

* **Detección de Solapamiento (RF7):** Se valida que el sistema alerte al usuario si intenta agendar dos citas en el mismo rango de tiempo.
* **Modo Offline (RNF3):** Se verifica que las citas creadas sin conexión se sincronicen correctamente al recuperar el acceso a la red.
* **Rendimiento (RNF4):** Se prueba que la visualización del calendario sea rápida, cumpliendo con el criterio de **respuesta en menos de 1 segundo**.

## 4. Estrategia de Mantenimiento Propuesta

El mantenimiento se enfocará en la **Evolución y Sostenibilidad**:

* **Tipo Dominante:** **Mantenimiento Adaptativo**. [cite_start]Es fundamental para la implementación del cambio funcional propuesto: la **sincronización en la nube** [cite: 74][cite_start], que requiere adaptar el sistema para trabajar con servicios externos (ej. Firebase/Supabase) y garantizar el acceso multiplataforma[cite: 75].
* [cite_start]**Mantenimiento Preventivo:** Optimizar las consultas a la base de datos para mantener el tiempo de respuesta rápido (RNF4) y revisar los mecanismos de seguridad y cifrado[cite: 72].

## 5. Reflexión sobre Control de Versiones (Git)

El uso de **Git** asegura la trazabilidad de la documentación. Cada artefacto (DRS, Plan de Pruebas, Propuesta de Mantenimiento) fue registrado en un *commit* separado, permitiendo **auditar la evolución** del proyecto. Esto es vital para un sistema que se adaptará a nuevas tecnologías y donde el cumplimiento de requerimientos no funcionales (como el modo *offline*) debe ser rastreable.

---

