# Casos de uso (v1.0)
## CU-001: Iniciar sesión (cubre REQ-003)
**- Actor:** Usuaio (Administrador, Cajero, Encargado del almacén)
**- Flujo principal:**
      1. Se ingresa nombre de usuario y contraseña.
      2. El sistema valida que los datos sean correctos.
      3. El sistema redirige al usuario a su respectiva interfaz (Segun rol).
**-Flujo de excepcion:**
      1. El sistema permite un máximo de 3 intentos de ingreso.
      2. El sistema bloquea el acceso al usuario una vez sobrepasada los 3 intentos.

