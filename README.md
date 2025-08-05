# Ultralam - Sistema de Control de Inventarios

##  Descripción
Sistema ERP web que automatiza el control de inventarios de láminas y materiales de remodelación. Reemplaza un sistema manual en Excel por una solución digital con control de cortes, fragmentos y visualización en tiempo real.

##  Problema identificado
La empresa usaba hojas de cálculo para registrar ventas y fragmentos, dificultando saber qué materiales estaban realmente disponibles para su venta o reutilización.

##  Solución
Se desarrolló una plataforma web que permite:
- Registrar cortes personalizados
- Controlar fragmentos restantes
- Visualizar inventario actualizado
- Administrar usuarios y roles

##  Arquitectura
- **Backend:** Java EE (JPA + Servlets + REST)
- **Frontend:** JSP, HTML, CSS
- **Base de datos:** MySQL
- **Servidor de aplicaciones:** GlassFish 7
- **CI/CD:** Travis CI (opcional)
- **Control de versiones:** GitHub

##  Tabla de Contenidos
- [Descripción](#descripción)
- [Problema identificado](#problema-identificado)
- [Solución](#solución)
- [Arquitectura](#arquitectura)
- [Requerimientos](#requerimientos)
- [Instalación](#instalación)
- [Configuración](#configuración)
- [Uso](#uso)
- [Contribución](#contribución)
- [Roadmap](#roadmap)
## ⚙️ Instalación

Consulta el archivo [`INSTALL.md`](./INSTALL.md) para ver los pasos detallados de instalación local y configuración de GlassFish, base de datos y despliegue en Heroku.

---

## 🛠️ Configuración

Asegúrate de configurar:
- Variables de entorno de conexión a la base de datos.
- El archivo `web.xml` con los servlets necesarios.
- El archivo de despliegue en Heroku (si aplica).

---

## 👨‍💻 Uso del Sistema

1. Inicia sesión con tu cuenta.
2. Registra nuevas láminas de inventario.
3. Realiza cortes personalizados y registra fragmentos.
4. Consulta el inventario útil.
5. Exporta reportes.

---

## 📂 Estructura del Proyecto

```text
Ultralam-inventario/
│
├── src/                         # Código fuente Java
│   ├── controller/              # Servlets
│   ├── model/                   # Clases del Modelo (entidades)
│   ├── dao/                     # Acceso a la BD
│
├── web/                         # Archivos JSP
│   ├── login.jsp
│   ├── dashboard.jsp
│   ├── registro.jsp
│
├── resources/                   # Archivos de configuración
├── INSTALL.md                   # Guía de instalación
├── README.md                    # Este documento

