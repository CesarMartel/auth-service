# 🛡️ Microservicio de Autenticación (Auth-Service)

[cite_start]Este repositorio contiene la implementación del microservicio de autenticación, desarrollado como parte del Laboratorio de Microservicios[cite: 70]. [cite_start]Este servicio es completamente independiente y utiliza **Django REST Framework (DRF)** para manejar el registro de usuarios, el *login* y la emisión/renovación de **Tokens JWT**[cite: 97].

## 🎯 Objetivo del Microservicio

[cite_start]El objetivo principal es construir un servicio autónomo que maneje toda la lógica de seguridad y usuarios[cite: 97], incluyendo:
* [cite_start]Gestión de usuarios con un modelo de usuario personalizado[cite: 151, 152].
* [cite_start]Autenticación sin estado (stateless) mediante JWT[cite: 99].
* [cite_start]Persistencia de datos en **PostgreSQL**[cite: 97].
* [cite_start]Cacheo y sesiones con **Redis**[cite: 102].
* [cite_start]Despliegue y orquestación con **Docker Compose**[cite: 97].

## ⚙️ Tecnologías Utilizadas

| Componente | Tecnología | Propósito |
| :--- | :--- | :--- |
| **Backend** | Python, Django, DRF | Lógica de negocio y *endpoints* API. |
| **Autenticación** | `djangorestframework-simplejwt` | [cite_start]Generación y gestión de tokens JWT[cite: 141]. |
| **Base de Datos** | PostgreSQL (v13/15) | [cite_start]Persistencia de datos de usuarios[cite: 142, 134]. |
| **Cache/Sesiones** | Redis (v6/7-alpine) | [cite_start]Almacenamiento rápido de cache y sesiones[cite: 143, 135]. |
| **Contenerización** | Docker y Docker Compose | [cite_start]Entorno de desarrollo aislado y orquestación[cite: 55, 120]. |

---

## 🏗️ Estructura del Proyecto

El microservicio `auth-service` se encuentra contenido en su propia carpeta y utiliza archivos de configuración a nivel raíz para Docker Compose.
