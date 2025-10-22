# 🔐 Microservicio de Autenticación (auth-service)

## 📋 Descripción
Microservicio de autenticación desarrollado con tecnologías modernas para proporcionar una solución robusta y escalable de gestión de usuarios y autenticación.

## 🚀 Tecnologías Principales
- **Framework**: Django + Django REST Framework
- **Autenticación**: JWT (JSON Web Tokens)
- **Base de Datos**: PostgreSQL
- **Caché**: Redis
- **Contenedorización**: Docker & Docker Compose

## ✨ Características Principales
- Autenticación JWT con tokens de acceso y refresco
- Modelo de usuario personalizado y extensible
- Almacenamiento persistente en PostgreSQL
- Sistema de caché optimizado con Redis
- Arquitectura containerizada
- API RESTful completa

## 🛠️ Estructura del Proyecto
```
auth-service/
├── app/
│   ├── auth_service/
│   │   ├── settings.py
│   │   ├── urls.py
│   │   └── wsgi.py
│   ├── users/
│   │   ├── models.py
│   │   ├── serializers.py
│   │   ├── views.py
│   │   └── urls.py
│   └── manage.py
├── docker-compose.yml
├── Dockerfile
├── requirements.txt
└── README.md
```

## 📦 Requisitos Previos
- Docker
- Docker Compose

## 🚀 Instalación y Ejecución

```bash
# Clonar el repositorio
git clone https://github.com/tu-usuario/auth-service.git

# Navegar al directorio
cd auth-service

# Construir los contenedores
docker-compose build

# Iniciar los servicios
docker-compose up -d
```

## 🔗 Endpoints API

| Método | Endpoint | Descripción |
|--------|----------|-------------|
| POST | `/api/auth/register/` | Registro de usuarios |
| POST | `/api/auth/login/` | Inicio de sesión |
| POST | `/api/auth/refresh/` | Renovación de token |
| GET | `/api/auth/profile/` | Perfil de usuario |

## 📝 Documentación API
El servicio está disponible en `http://localhost:8000`

Para acceder a la documentación interactiva de la API:
- Swagger UI: `http://localhost:8000/api/docs/`
- ReDoc: `http://localhost:8000/api/redoc/`

## 🔒 Variables de Entorno
Crea un archivo `.env` en la raíz del proyecto:

```env
DEBUG=True
SECRET_KEY=tu_clave_secreta
POSTGRES_DB=auth_db
POSTGRES_USER=auth_user
POSTGRES_PASSWORD=auth_password
REDIS_HOST=redis
REDIS_PORT=6379
```

## 👥 Contribución
1. Fork el repositorio
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## 📄 Licencia
Distribuido bajo la licencia MIT. Ver `LICENSE` para más información.
