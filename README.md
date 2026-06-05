# 🏛️ Proyecto: Página Web para la Alcaldía

Este proyecto es una página web para que los habitantes del municipio puedan hacer sus trámites y solicitudes desde la computadora o el teléfono, sin necesidad de hacer largas colas en la alcaldía.

---

## 👥 1. ¿Quiénes usan la página? (Roles)

En el sistema existen tres tipos de usuarios:

*   **👤 El Ciudadano :** Es cualquier persona del municipio. Entra a la página para pedir una ayuda, reportar un problema de luz/agua, o solicitar un permiso.
*   **💼 Trabajador de la alcaldía:** Es la persona que trabaja en una oficina de la alcaldía (como Catastro o Desarrollo Social). Revisa lo que pidió el ciudadano y decide si lo aprueba o lo rechaza.
*   **⚙️ El Administrador (El técnico):** Es la persona encargada de que la página funcione. Crea las cuentas de los trabajadores y registra las oficinas.

---

## 🧠 2. ¿Cómo funciona el sistema? (Reglas de Negocio)

Para que todo funcione en orden, el software sigue estas reglas obligatorias:

### A. Al entrar a la página (Seguridad)
1.  **Cuentas únicas:** Para registrarse, el Ciudadano debe poner su cédula y su correo. El sistema no permite que dos personas usen la misma cédula o el mismo correo.

2.  **Contraseñas secretas:** Las contraseñas no se guardan tal cual como las escribe el usuario. El sistema las "encripta" (las transforma en un código secreto) para que nadie pueda robárselas.

3.  **Bloqueo por seguridad:** Si alguien intenta adivinar una contraseña y se equivoca 5 veces seguidas, el sistema bloquea esa cuenta por 15 minutos.

### B. Al pedir un trámite o ayuda (Procesos)

1.  **Ticket de soporte:** Cuando un Ciudadano pide un trámite, el sistema le da un **Número de Seguimiento** único para que pueda ver cómo va su solicitud.

2.  **Envío automático:** Si el ciudadano pide una ayuda social, el sistema se la envía directamente a la oficina de Desarrollo Social. Si pide algo de terrenos, se va a Catastro.

3.  **El camino del trámite:** El trabajador de la alcaldía recibe la solicitud y puede cambiar su estado a: `En revisión`, `Falta un documento`, `Aprobado` o `Rechazado`.

4.  **No hay vuelta atrás:** Una vez que el trabajador le da a "Aprobado" o "Rechazado", ese trámite se cierra y **nadie** lo puede volver a cambiar. Esto evita trampas.

### C. Control de los Jefes

1.  **Alerta de tardanza:** Si un trabajador deja una solicitud guardada por más de 2 días sin revisarla, el sistema le envía una alerta automática al **Jefe del Departamento** para avisarle que ese trabajador no está cumpliendo.

---
