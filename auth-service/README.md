# Microservicio de Autenticación (auth-service)

Este proyecto implementa un **microservicio de autenticación** desarrollado con **Django**, **Django REST Framework**, **JWT (JSON Web Tokens)**, **PostgreSQL** y **Redis**.  
El servicio gestiona usuarios, registro, inicio de sesión y renovación de tokens JWT, siguiendo una arquitectura modular y escalable.

---

## Características

- **Autenticación con JWT:** Emisión y renovación de tokens de acceso y refresco.
- **Modelo de Usuario Personalizado:** Extiende el modelo por defecto de Django para una mayor flexibilidad.
- **Base de Datos PostgreSQL:** Almacenamiento persistente y seguro de los datos de usuario.
- **Sistema de Caché con Redis:** Optimización del manejo de sesiones y almacenamiento temporal.
- **Dockerizado:** Arquitectura completamente contenida en Docker para facilitar despliegue y portabilidad.
- **API RESTful:** Endpoints para registro, autenticación, renovación de tokens y gestión del perfil de usuario.

---

## Requisitos Previos

Antes de ejecutar el proyecto, asegúrate de tener instaladas las siguientes herramientas:

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

---

## Estructura del Proyecto

La estructura general del proyecto sigue el siguiente esquema:

auth-service/
├── app/
│ ├── auth_service/
│ │ ├── settings.py
│ │ ├── urls.py
│ │ └── wsgi.py
│ ├── users/
│ │ ├── models.py
│ │ ├── serializers.py
│ │ ├── views.py
│ │ └── urls.py
│ ├── manage.py
│ └── ...
├── docker-compose.yml
├── Dockerfile
├── requirements.txt
└── README.md


---

## Ejecución del Proyecto

Para construir y ejecutar el microservicio, utiliza los siguientes comandos:

```bash
# Construir los contenedores
docker-compose build

# Iniciar los servicios
docker-compose up

El servicio estará disponible en el puerto configurado en el archivo docker-compose.yml (por defecto http://localhost:8000).
Endpoints Principales
Método	Endpoint	Descripción
POST	/api/auth/register/	Registro de nuevos usuarios
POST	/api/auth/login/	Inicio de sesión y obtención de tokens
POST	/api/auth/refresh/	Renovación del token de acceso
GET	/api/auth/profile/	Consulta del perfil de usuario autenticado
Tecnologías Utilizadas

    Backend: Django, Django REST Framework

    Autenticación: JSON Web Tokens (JWT)

    Base de Datos: PostgreSQL

    Caché y Sesiones: Redis

    Contenedores: Docker y Docker Compose
