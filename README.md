# 🏛️ Título del Proyecto: Sistema de Gestión Institucional y Atención Ciudadana
**Proyecto PNFI en Informática:** Sistema de Base de Datos para la Alcaldía de Pampán, Estado Trujillo.

---

## 📝 Descripción General
Es una plataforma web que digitaliza y automatiza los trámites internos y la atención al público en la alcaldía. Resuelve los retrasos, el uso excesivo de papel y la falta de información, ofreciendo una comunicación rápida y transparente entre los ciudadanos y las oficinas.

---

## 🎯 Objetivo Principal
Modernizar la gestión municipal con un canal digital único que acelere las respuestas, asegure los datos y permita auditar todas las acciones del personal.

---

## 👥 Usuarios Clave (Roles)

* **👤 Ciudadano:** Se registra, inicia trámites, sube documentos y consulta el estado de su solicitud en tiempo real.
* **💼 Operador (Funcionario):** Revisa los requisitos de su departamento, procesa las solicitudes y actualiza sus estados.
* **👔 Jefe de Departamento (Director):** Supervisa al personal y aprueba los trámites de alta prioridad.
* **⚙️ Superadministrador / Auditor:** Registra al personal, controla los accesos y vigila el comportamiento de todos los usuarios para evitar alteraciones.

---

## 🚀 Funcionalidades Principales (Alcance)

* **🔐 Registro y Control de Acceso:** Creación de cuentas ciudadanas con cédula/correo y restricción de pantallas según el rol del usuario.
* **🛡️ Seguridad y Bloqueos:** Bloqueo temporal de cuenta tras 5 intentos fallidos de clave y cierre de sesión por inactividad a los 20 minutos.
* **📂 Gestión de Trámites:** Envío de solicitudes con código de seguimiento único y enrutamiento automático al departamento correcto.
* **🔄 Control de Estados:** Actualización del trámite (En revisión, Subsanación, Aprobado o Rechazado). Al aprobarse o rechazarse, el estado no se puede volver a cambiar.
* **🚨 Alertas y Escalabilidad:** Alerta automática al Jefe si un trámite pasa 48 horas sin atender y retención de casos especiales hasta recibir autorización del Director General.
* **👁️ Auditoría Permanente (Bitácora):** Registro automático e imborrable de cada acción crítica (usuario, fecha, hora y equipo) para la supervisión del Auditor.
