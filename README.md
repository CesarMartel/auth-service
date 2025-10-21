# 🛡️ Microservicio de Autenticación (Auth-Service)

Este repositorio contiene la implementación del microservicio de autenticación, desarrollado como parte del Laboratorio de Microservicios. Este servicio es completamente independiente y utiliza **Django REST Framework (DRF)** para manejar el registro de usuarios, el *login* y la emisión/renovación de **Tokens JWT**.

## 🎯 Objetivo del Microservicio

El objetivo principal es construir un servicio autónomo que maneje toda la lógica de seguridad y usuarios, incluyendo:
* Gestión de usuarios con un modelo de usuario personalizado.
* Autenticación sin estado (stateless) mediante JWT.
* Persistencia de datos en **PostgreSQL**.
* Cacheo y sesiones con **Redis**.
* Despliegue y orquestación con **Docker Compose**.

## ⚙️ Tecnologías Utilizadas

| Componente | Tecnología | Propósito |
| :--- | :--- | :--- |
| **Backend** | Python, Django, DRF | Lógica de negocio y *endpoints* API. |
| **Autenticación** | `djangorestframework-simplejwt` | Generación y gestión de tokens JWT. |
| **Base de Datos** | PostgreSQL (v13/15) | Persistencia de datos de usuarios. |
| **Cache/Sesiones** | Redis (v6/7-alpine) | Almacenamiento rápido de cache y sesiones. |
| **Contenerización** | Docker y Docker Compose | Entorno de desarrollo aislado y orquestación. |

---

## 🏗️ Estructura del Proyecto

El microservicio `auth-service` se encuentra contenido en su propia carpeta y utiliza archivos de configuración a nivel raíz para Docker Compose.
auth-services
|
├── .env.example               # Plantilla de variables de entorno (no versionar)
├── README.md                  # Documentación del proyecto
├── docker-compose.yml         # Orquestación: auth, postgres, redis
├── auth-service/              # Directorio para construir la imagen Docker del servicio
│   ├── Dockerfile             # Instrucciones para la imagen (ej. Python 3.11)
│   ├── manage.py              # Script de gestión de Django
│   ├── requirements.txt       # Dependencias Python (pip)
│   ├── auth_service/          # Proyecto Django principal
│   │   ├── __init__.py
│   │   ├── asgi.py
│   │   ├── settings.py        # Configuración (DB, Redis, JWT, apps, CORS, etc.)
│   │   ├── urls.py            # Rutas globales (incluye rutas de 'users' y JWT)
│   │   └── wsgi.py
│   └── users/                 # App Django 'users' (autenticación / usuarios)
│       ├── __init__.py
│       ├── admin.py
│       ├── apps.py
│       ├── migrations/        # Migraciones de la app
│       ├── models.py          # Modelo de usuario personalizado (email único)
│       ├── serializers.py     # Serializers para User, Register, etc.
│       ├── urls.py            # Rutas de la app (register, me, etc.)
│       ├── views.py           # Lógica de registro y endpoints
│       └── tests.py
└── .gitignore                 # Ignorar .env, __pycache__, etc.
