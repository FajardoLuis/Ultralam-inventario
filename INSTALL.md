#  Guía de instalación y configuración del sistema de control de inventario - Ultralam

Este documento describe los pasos necesarios para instalar, configurar y ejecutar correctamente el sistema web de control de inventario desarrollado para Ultralam.

---

##  Requisitos del sistema

Asegúrate de tener instaladas las siguientes herramientas antes de comenzar:

- Java Development Kit (JDK) 17 o superior
- Apache NetBeans 20 o superior
- Servidor GlassFish 7 o superior
- MySQL Server 8.0 o PostgreSQL
- Navegador web moderno (Google Chrome, Firefox, Edge)
- Git (opcional pero recomendado)

---

##  Instrucciones de instalación

### 1. Clonar el repositorio

Si tienes Git instalado, puedes clonar el proyecto:

```bash
git clone https://github.com/FajardoLuis/Ultralam-inventario.git

---

### 2. Abrir el proyecto en NetBeans

1. Inicia NetBeans.
2. Haz clic en **File > Open Project**.
3. Busca y selecciona la carpeta `Ultralam-inventario`.
4. Espera a que NetBeans cargue todas las dependencias.

---

### 3. Configurar el servidor GlassFish

1. Ve al panel **Services** (Servicios).
2. Haz clic derecho sobre **Servers > Add Server**.
3. Elige **GlassFish Server**, da clic en **Next**.
4. Selecciona la carpeta donde tienes GlassFish instalado.
5. Configura el usuario como `admin`, puerto HTTP como `8080`.
6. Finaliza y asegúrate de que el servidor esté en línea.

---

### 4. Configurar la base de datos

1. Abre MySQL Workbench o tu cliente de base de datos favorito.
2. Ejecuta el siguiente script para crear la base de datos:

```sql
CREATE DATABASE ultralam_inventario;
```

3. Dentro del proyecto, localiza la clase `DBConnection.java` o similar.
4. Asegúrate de configurar las credenciales de conexión:

```java
String url = "jdbc:mysql://localhost:3306/ultralam_inventario";
String user = "root";
String password = "tu_contraseña";
```

5. El conector JDBC debe estar correctamente añadido en las librerías del proyecto (`mysql-connector-j-8.x.jar`).

---

### 5. Desplegar la aplicación en GlassFish

1. Haz clic derecho sobre el proyecto en NetBeans.
2. Selecciona **Deploy**.
3. Espera a que se despliegue correctamente en el servidor.
4. Abre tu navegador y accede a:

```
http://localhost:8080/Ultralam-inventario
```

---

##  Uso del sistema

Una vez desplegado, puedes usar el sistema para:

- Registrar láminas y cortes personalizados
- Controlar y rastrear fragmentos sobrantes
- Ver el historial de movimientos
- Administrar usuarios y roles
- Visualizar reportes y estadísticas de inventario

---

##  Solución de problemas comunes

| Problema | Solución |
|---------|----------|
| Puerto 8080 en uso | Cierra otras aplicaciones que usen ese puerto o cambia el puerto en GlassFish |
| Error al conectar con base de datos | Verifica el usuario, contraseña y URL en `DBConnection.java` |
| Error de despliegue en GlassFish | Revisa que el dominio esté iniciado y que no haya errores en la consola |
| Faltan librerías JDBC | Asegúrate de tener `mysql-connector-j.jar` agregado al proyecto |

---

##  Contacto

Desarrollado por: **Luis Felipe Fajardo Sánchez**  
 Correo: rexta24@gmail.com  
 Profesional: Al03047899@tecmilenio.com  

---

**¡Gracias por usar el sistema de inventario de Ultralam!**
