## Tipos de usuario

- Se identifica por un número único de usuario, User ID, UID
- Pertenecen a un grupo principal de usuario, identificado también por un número único de grupo, Group ID, GID

### Root

- Super usuario
- Única cuenta con privilegios en todo el sistema
- Acceso total a todos los archivos y directorios
- Administración de cuentas de usuario
- Puede detener el sistema
- Instala software
- Puede modificar el kernel

### Usuarios especiales

- Cuentas del sistema
- No tienen contraseñas
- Dependiendo de la cuenta asumen distintos privilegios de root
- Cuentas de “no inicio de sesión”
- Creados automáticamente al momento de la instalación del sistema operativo o aplicación
- Generalmente se les asigna un UID entre 1 y 100 (definido en /etc/logs/)

### Usuarios normales

- Se usan para usuarios individuales
    
- Cada usuario dispones de un directorio de trabajo ubicado generalmente en /home/
    
- Cada usuario puede personalizar su entrono de trabajo
    
- En las distros actuales de Linux se les asigna generalmente…
    
- Creación de usuario
    

```powershell
/useradd
```

- Modificación de usuario

```powershell
/usermod
```

- Eliminación de usuarios

```powershell
/userdel
```

- Creación de grupos

```powershell
/groupadd
```

- Modificación de grupos:

```powershell
/groupmod
```