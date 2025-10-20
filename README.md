# Microservicio de Autenticación (auth-service)

Este proyecto implementa un **microservicio de autenticación** desarrollado con **Django**, **Django REST Framework**, **JWT (JSON Web Tokens)**, **PostgreSQL** y **Redis**.  
El servicio gestiona usuarios, registro, inicio de sesión y renovación de tokens JWT, siguiendo una arquitectura modular y escalable uwu.

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


---
```
![Imagen de WhatsApp 2025-10-19 a las 02 03 36_87436436](https://github.com/user-attachments/assets/088faeab-7118-46e9-8026-3621878ad2b7)

<img width="1514" height="893" alt="Captura de pantalla 2025-10-19 015422" src="https://github.com/user-attachments/assets/d8902a43-8b46-41c9-bf1b-6e53ac972796" />

<img width="1237" height="697" alt="Captura de pantalla 2025-10-19 015838" src="https://github.com/user-attachments/assets/e9945148-3a46-4b72-9889-239219bcf324" />

<img width="1506" height="686" alt="Captura de pantalla 2025-10-19 020038" src="https://github.com/user-attachments/assets/62118a08-e8b7-4cd5-a445-4ec60416bf82" />





