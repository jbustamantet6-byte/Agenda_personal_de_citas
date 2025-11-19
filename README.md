# Sistema de Agenda Personal de Citas (Caso Práctico 2)

Este repositorio contiene la documentación técnica fundamental generada para la aplicación **Agenda Personal de Citas**, cuyo objetivo principal es la gestión eficiente, organizada y segura de los compromisos personales del usuario.

---

## 1. Alcance y Requerimientos Clave

### Descripción del Caso y Objetivos
El sistema debe permitir al usuario registrar, visualizar y organizar sus citas. El objetivo principal es garantizar que la información esté siempre accesible y que el usuario pueda evitar **solapamientos de horario** y utilizar la agenda incluso en **modo offline**.

### Requisitos Funcionales y No Funcionales (DRS)

| Código | Requerimiento Central | Tipo | Enfoque |
| :--- | :--- | :--- | :--- |
| **RF1, RF2** | Gestión de Citas (CRUD) | Funcional | Crear, editar y eliminar citas con detalles de tiempo y ubicación. |
| **RF7** | **Detección de Solapamiento** | Funcional | Advertir al usuario si intenta crear citas con conflicto de horario. |
| **RNF3** | **Modo Offline** | No Funcional | Permitir registrar datos sin conexión y sincronizar al reconectar. |
| **RNF4** | Rendimiento y Velocidad | No Funcional | El tiempo de respuesta al cambiar de vista debe ser **inferior a 1 segundo**. |

---

## 2. Resultados de las Pruebas y Estrategia de Mantenimiento

### Resumen del Plan de Pruebas
El Plan de Pruebas se enfocó en garantizar la **integridad de la información y el rendimiento**. Los casos de prueba clave validaron exitosamente:
* La **Detección de Solapamiento** (P-01) con la alerta correspondiente.
* El funcionamiento del **Modo Offline** (P-03), asegurando que las citas se **sincronicen** correctamente al restaurar la conexión a Internet.
* El **Rendimiento** (P-05), cumpliendo con el tiempo de carga de vistas inferior a 1 segundo.

### Tipo de Mantenimiento Propuesto

La estrategia de sostenibilidad se basa en el **Mantenimiento Adaptativo**.

* **Adaptativo:** Es el más crítico debido a la implementación del **DRS v2** (sincronización en la nube). Requiere adaptar la arquitectura para integrarse con servicios externos (ej., Firebase o Supabase) y gestionar la lógica de **resolución de conflictos** entre datos locales y remotos.
* **Preventivo:** Se enfoca en la **optimización trimestral de consultas** a la base de datos para mantener la promesa del RNF4 (<1s).

---

## 3. Reflexión sobre el Control de Versiones (Git)

El uso de **Git y GitHub** fue fundamental para este proyecto, ya que garantiza la **trazabilidad** y la **auditoría** de la documentación técnica. Al registrar el **Plan de Pruebas**, la **Propuesta de Mantenimiento**, y el **DRS** en *commits* separados, el repositorio se convierte en un registro histórico de las decisiones tomadas. Esto permite a cualquier desarrollador verificar la **evolución de los requisitos** (ej., la justificación del RNF4 y el RNF3) y minimiza el riesgo de conflictos al trabajar con archivos de documentación en formato de texto plano (`.md`).



