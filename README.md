
# Plataforma Web - Alcaldía del Municipio Pampán

> **Proyecto Universitario - PNFI**
# **Por :** *Jean Carlos Saavedra*
> Diseño, desarrollo e implementación de una plataforma web institucional para centralizar información, automatizar la gestión de trámites y optimizar la comunicación con los ciudadanos del Municipio Pampán.

---

## 📌 1. Objetivo del Proyecto
El objetivo principal de esta plataforma es transformar la gestión interna de la alcaldía y mejorar la atención ciudadana. El sistema busca:
*   Eliminar la burocracia y el uso excesivo de papel mediante la digitalización.
*   Centralizar las solicitudes en un único repositorio digital accesible.
*   Ofrecer transparencia a los ciudadanos permitiéndoles consultar el estado de sus trámites en tiempo real.

---

## 👥 2. Roles del Sistema (Actores)

Para garantizar la seguridad y el principio de menor privilegio, el sistema cuenta con tres niveles de acceso claramente definidos:

| Rol | Descripción | Permisos Clave |
| :--- | :--- | :--- |
| **👤 Ciudadano** | Habitante registrado del municipio. | Registrarse, iniciar trámites, adjuntar requisitos, consultar historial. |
| **💼 Operador (Funcionario)** | Personal asignado a un departamento específico. | Ver solicitudes del área, cambiar estados (Aprobado/Rechazado), añadir notas. |
| **⚙️ Administrador** | Personal de soporte técnico / informática. | Crear cuentas de operadores, gestionar departamentos, auditar bitácoras del sistema. |

---

## 🧠 3. Lógica de Negocio y Reglas del Software

El desarrollo del software se rige estrictamente por las siguientes reglas operativas:

### A. Autenticación y Seguridad
*   **Registro Público:** Los *Ciudadanos* se registran de forma autónoma. El sistema valida de forma única la **Cédula de Identidad** y el **Correo Electrónico** para evitar duplicados.
  
*   **Cuentas Institucionales:** Las cuentas de *Operadores* y *Administradores* no tienen registro público; son dadas de alta exclusivamente por el administrador para mitigar brechas de seguridad.
  
*   **Resguardo de Credenciales:** Ninguna contraseña se almacena en texto plano. Se implementará hashing mediante algoritmos seguros (ej. `bcrypt`) en la base de datos.

### B. Flujo de Control de Trámites

1.  **Creación:** Al iniciar un trámite, el sistema genera de forma automática un **Código de Seguimiento Único**.
2.  **Enrutamiento:** La solicitud se indexa automáticamente al **Departamento** correspondiente (Catastro, Desarrollo Social, etc.) basándose en la tipología del trámite.
3.  **Ciclo de Vida del Estado:** Los trámites inician en estado `Pendiente`. El operador puede cambiarlo a `En revisión`, `Subsanación` (espera de corrección del usuario), `Aprobado` o `Rechazado`.
4.  **Inmutabilidad Histórica:** Una vez que un trámite alcanza un estado terminal (`Aprobado` o `Rechazado`), **ningún usuario** (incluido el operador) puede revertir o modificar dicho estado para salvaguardar la integridad de la auditoría.

### C. Auditoría y Transparencia
*   Toda acción crítica (cambios de estado, asignaciones, creación de usuarios) genera un registro automático en una **tabla de auditoría (bitácora)** con la fecha, hora y el ID del usuario que realizó la acción.

---
