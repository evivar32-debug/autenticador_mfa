# Autenticador MFA (Multi-Factor Authentication)

Este proyecto es un sistema de autenticación de dos factores desarrollado con **Python** y **Django**. Proporciona una capa adicional de seguridad para el inicio de sesión de usuarios, integrando una base de datos **MySQL** y utilizando **Docker** para un despliegue rápido y consistente en cualquier entorno.

## 🚀 Características

* **Doble Factor de Autenticación (MFA):** Implementación de seguridad reforzada para el acceso de usuarios.
* **Backend Robusto:** Desarrollado con Django, aprovechando su sistema de seguridad nativo.
* **Persistencia de Datos:** Configurado para trabajar con una base de datos MySQL.
* **Contenerización:** Configuración completa con Docker y Docker Compose para facilitar la instalación.

## 🛠️ Tecnologías Utilizadas

* **Lenguaje:** Python
* **Framework Web:** [Django](https://www.djangoproject.com/)
* **Base de Datos:** [MySQL](https://www.mysql.com/)
* **Infraestructura:** [Docker](https://www.docker.com/) & Docker Compose

## 📋 Requisitos Previos

Asegúrate de tener instalados los siguientes componentes en tu sistema:

* **Docker** (Versión reciente)
* **Docker Compose**

## 🔧 Instalación y Configuración

Sigue estos pasos para poner en marcha el proyecto localmente:

1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com/evivar32-debug/autenticador_mfa.git
   cd autenticador_mfa

2. **Configurar el entorno:**
   Crea un archivo `.env` en la raíz del proyecto (o edita el existente) con las credenciales de tu base de datos y la `SECRET_KEY` de Django.

3. **Construir y levantar los contenedores:**
   ```bash
   docker-compose up --build
   
4. **Ejecutar migraciones:**
   Una vez que los contenedores estén corriendo, aplica las migraciones de la base de datos:
   ```bash
   docker-compose exec web python manage.py migrate

5. **Crear un superusuario (opcional):**
   Para acceder al panel de administración:
   ```bash
   docker-compose exec web python manage.py createsuperuser

##  🖥️ Uso

Una vez que el contenedor esté activo, puedes acceder a la aplicación en:
`http://localhost:8000`  
   
