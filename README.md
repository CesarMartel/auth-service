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

