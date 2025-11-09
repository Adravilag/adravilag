# 🚀 Portafolio de Proyectos

Una colección detallada de mis proyectos más destacados, organizados por categoría y stack tecnológico.

---

## 📑 Índice

- [🛍️ E-commerce & Full Stack](#️-e-commerce--full-stack)
- [🤖 IoT & Hardware](#-iot--hardware)
- [🏥 Aplicaciones Empresariales](#-aplicaciones-empresariales)
- [📚 Proyectos de Aprendizaje](#-proyectos-de-aprendizaje)

---

## 🛍️ E-commerce & Full Stack

### [Teslo Shop - Backend API](https://github.com/Adravilag/teslo-shop-nest)

<div align="center">
<img src="https://img.shields.io/badge/NestJS-E0234E?style=for-the-badge&logo=nestjs&logoColor=white" alt="NestJS"/>
<img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript"/>
<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL"/>
<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker"/>
<img src="https://img.shields.io/badge/Socket.io-010101?style=for-the-badge&logo=socketdotio&logoColor=white" alt="Socket.io"/>
</div>

#### 📋 Descripción
Backend completo de una tienda de e-commerce con todas las funcionalidades necesarias para una aplicación en producción. Incluye autenticación, gestión de productos, carga de imágenes y comunicación en tiempo real.

#### ✨ Características Principales
- **Autenticación completa**
  - JWT con refresh tokens
  - Roles y permisos (admin, user)
  - Guards personalizados con Passport
  - Hash de contraseñas con bcrypt

- **Gestión de Productos**
  - CRUD completo con validaciones
  - Relaciones entre entidades (productos, usuarios, imágenes)
  - Paginación y filtros avanzados
  - Búsqueda por múltiples criterios
  - Slugs únicos automáticos

- **Upload de Archivos**
  - Multer para gestión de archivos
  - Validación de tipos y tamaños
  - Almacenamiento local y servido estático
  - Integración con productos (múltiples imágenes)

- **WebSockets en Tiempo Real**
  - Socket.IO para chat
  - Notificaciones de usuarios conectados
  - Sincronización de estado entre clientes

- **Documentación API**
  - Swagger/OpenAPI completo
  - Ejemplos de requests/responses
  - Autenticación JWT en Swagger UI
  - DTOs documentados

#### 🏗️ Arquitectura
```
src/
├── auth/                    # Módulo de autenticación
│   ├── decorators/          # Decoradores personalizados
│   ├── guards/              # Guards de autenticación
│   ├── strategies/          # Estrategias Passport
│   └── dto/                 # DTOs de auth
├── products/                # Módulo de productos
│   ├── entities/            # Entidades TypeORM
│   ├── dto/                 # DTOs de productos
│   └── pipes/               # Pipes personalizados
├── files/                   # Módulo de archivos
│   ├── helpers/             # Validadores y helpers
│   └── filters/             # Filtros de archivos
├── messages-ws/             # WebSockets
│   ├── gateways/            # Socket.IO gateways
│   └── dto/                 # DTOs de mensajes
├── common/                  # Módulos compartidos
│   ├── decorators/          # Decoradores globales
│   ├── filters/             # Exception filters
│   └── pipes/               # Validation pipes
└── seed/                    # Seeders de datos
```

#### 📊 Estadísticas del Proyecto
- **Líneas de código**: ~5,000+
- **Endpoints**: 30+
- **Módulos**: 6
- **Entidades**: 5
- **Tests**: Unit + Integration
- **Documentación**: 8 guías completas

#### 🔧 Stack Técnico
- **Backend**: NestJS 10, TypeScript 5
- **Database**: PostgreSQL 16, TypeORM 0.3
- **Auth**: Passport, JWT, bcrypt
- **Files**: Multer
- **Real-time**: Socket.IO
- **Docs**: Swagger/OpenAPI
- **Validation**: class-validator, class-transformer
- **Config**: @nestjs/config, Joi
- **Dev**: Docker, Docker Compose
- **Deploy**: Render + Neon DB

#### 📚 Documentación Disponible
1. [Configuración Inicial](https://github.com/Adravilag/teslo-shop-nest/blob/main/docs/01-setup.md)
2. [Variables de Entorno](https://github.com/Adravilag/teslo-shop-nest/blob/main/docs/02-environment.md)
3. [Base de Datos](https://github.com/Adravilag/teslo-shop-nest/blob/main/docs/03-database.md)
4. [Autenticación](https://github.com/Adravilag/teslo-shop-nest/blob/main/docs/04-authentication.md)
5. [Carga de Archivos](https://github.com/Adravilag/teslo-shop-nest/blob/main/docs/05-file-upload.md)
6. [API Documentation](https://github.com/Adravilag/teslo-shop-nest/blob/main/docs/06-api-documentation.md)
7. [WebSockets](https://github.com/Adravilag/teslo-shop-nest/blob/main/docs/07-websockets-socketio.md)
8. [Deployment](https://github.com/Adravilag/teslo-shop-nest/blob/main/docs/08-deployment-render.md)

#### 🚀 Demo & Links
- [📦 Backend Repo](https://github.com/Adravilag/teslo-shop-nest)
- [📖 API Docs](https://nest-teslo-shop-q0ko.onrender.com/api)

---

### [Teslo Shop - Frontend Angular](https://github.com/Adravilag/teslo-shop-angular)

<div align="center">
<img src="https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white" alt="Angular"/>
<img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript"/>
<img src="https://img.shields.io/badge/TailwindCSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white" alt="TailwindCSS"/>
<img src="https://img.shields.io/badge/DaisyUI-5A0EF8?style=for-the-badge&logo=daisyui&logoColor=white" alt="DaisyUI"/>
</div>

#### 📋 Descripción
Frontend moderno de e-commerce construido con Angular 20+, utilizando las últimas características como Signals, Resource API y standalone components.

#### ✨ Características Principales
- **Arquitectura Moderna**
  - Standalone components (sin NgModules)
  - Signals para reactive state
  - Resource API para data fetching
  - Change Detection OnPush

- **Autenticación & Guards**
  - Login/Register con formularios reactivos
  - Auth guards para protección de rutas
  - Interceptores HTTP para tokens
  - Gestión de roles (admin/user)

- **Gestión de Productos**
  - Lista de productos con paginación
  - Filtros por género y categoría
  - Vista detallada de productos
  - Carrusel de imágenes con Swiper

- **Panel de Administración**
  - Dashboard para administradores
  - CRUD de productos
  - Upload de imágenes múltiples
  - Validaciones en formularios

- **UI/UX Premium**
  - Diseño responsive con TailwindCSS
  - Componentes DaisyUI
  - Animaciones suaves
  - Loading states y error handling

#### 🏗️ Arquitectura
```
src/
├── app/
│   ├── auth/                # Módulo de autenticación
│   │   ├── guards/          # Route guards
│   │   ├── interceptors/    # HTTP interceptors
│   │   └── services/        # Auth service
│   ├── admin-dashboard/     # Panel admin
│   │   ├── layouts/         # Admin layout
│   │   └── pages/           # Admin pages
│   ├── store-front/         # Tienda pública
│   │   ├── layouts/         # Store layout
│   │   ├── pages/           # Store pages
│   │   └── components/      # Store components
│   ├── products/            # Módulo de productos
│   │   ├── components/      # Product components
│   │   ├── services/        # Product service
│   │   └── interfaces/      # TypeScript interfaces
│   └── shared/              # Componentes compartidos
│       ├── components/      # Shared components
│       ├── interceptors/    # Global interceptors
│       └── pipes/           # Custom pipes
└── environments/            # Environment configs
```

#### 🔧 Stack Técnico
- **Framework**: Angular 20
- **Language**: TypeScript 5
- **Styling**: TailwindCSS + DaisyUI
- **State Management**: Signals + RxJS
- **Forms**: Reactive Forms
- **HTTP**: HttpClient with interceptors
- **Routing**: Angular Router with guards
- **Images**: Swiper for carousels

#### 📊 Características Técnicas
- Lazy loading de módulos
- Route guards (auth, admin)
- HTTP interceptors (auth token)
- Custom pipes (product images)
- Form validations
- Error handling global
- Responsive design
- SEO optimized

#### 🚀 Demo & Links
- [🎨 Frontend Repo](https://github.com/Adravilag/teslo-shop-angular)
- [🌐 Live Demo](https://adavilag-portfolio.vercel.app/)

---

## 🤖 IoT & Hardware

### [Motion Detector - Arduino + Raspberry Pi](https://github.com/Adravilag/Motion-Detector)

<div align="center">
<img src="https://img.shields.io/badge/Arduino-00979D?style=for-the-badge&logo=arduino&logoColor=white" alt="Arduino"/>
<img src="https://img.shields.io/badge/Raspberry_Pi-A22846?style=for-the-badge&logo=raspberrypi&logoColor=white" alt="Raspberry Pi"/>
<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
<img src="https://img.shields.io/badge/Mule_ESB-00A1E0?style=for-the-badge" alt="Mule ESB"/>
</div>

#### 📋 Descripción
Sistema IoT que integra sensores de movimiento con Arduino, procesamiento en Raspberry Pi y gestión de eventos mediante Mule ESB Standalone.

#### ✨ Características Principales
- **Detección de Movimiento**
  - Sensor PIR (Passive Infrared)
  - Lectura en tiempo real
  - Debouncing para evitar falsos positivos

- **Procesamiento de Datos**
  - Raspberry Pi como hub central
  - Scripts Python para lógica de negocio
  - Comunicación serial con Arduino

- **Integración Empresarial**
  - Mule ESB para procesamiento de eventos
  - API REST para consultas
  - Notificaciones y alertas

- **Monitoreo**
  - Dashboard de estado
  - Logs de eventos
  - Histórico de detecciones

#### 🏗️ Arquitectura
```
┌─────────────┐      Serial      ┌──────────────┐
│   Arduino   │ ←──────────────→ │ Raspberry Pi │
│   + PIR     │    USB/UART      │   + Python   │
└─────────────┘                  └──────┬───────┘
                                        │
                                   HTTP/REST
                                        │
                                  ┌─────▼─────┐
                                  │  Mule ESB │
                                  │  Standalone│
                                  └───────────┘
```

#### 🔧 Stack Técnico
- **Hardware**: Arduino Uno, Raspberry Pi 3 Model B+
- **Sensores**: PIR Motion Sensor
- **Programming**: Arduino C++, Python 3
- **Integration**: Mule ESB Standalone
- **Communication**: Serial (UART), HTTP REST

#### 📊 Casos de Uso
- Seguridad en el hogar
- Control de acceso
- Automatización de luces
- Monitoreo de espacios

#### 🚀 Links
- [🔗 Repositorio](https://github.com/Adravilag/Motion-Detector)

---

## 🏥 Aplicaciones Empresariales

### [MediQ Demo - Gestión Médica](https://github.com/Adravilag/MediQ-Demo)

#### 📋 Descripción
Aplicación demo para gestión de citas médicas y pacientes en el sector salud.

#### ✨ Características
- Gestión de citas médicas
- Registro de pacientes
- Panel de administración
- Reportes básicos

#### 🔧 Stack Técnico
(Información básica - proyecto demo)

#### 🚀 Links
- [🔗 Repositorio](https://github.com/Adravilag/MediQ-Demo)

---

## 📚 Proyectos de Aprendizaje

### Otros Proyectos (54 repositorios)

Además de los proyectos principales, tengo más de **54 repositorios** en GitHub que incluyen:

#### Backend Practice
- REST APIs con diferentes stacks
- Microservicios con NestJS
- GraphQL servers
- Authentication systems
- File upload services

#### Frontend Practice
- Angular applications
- React components
- Vue.js experiments
- UI/UX prototypes

#### Full Stack
- MEAN/MERN stack apps
- Real-time applications
- Chat applications
- Social media clones

#### DevOps & Tools
- Docker configurations
- CI/CD pipelines
- Deployment scripts
- Automation tools

---

## 📈 Estadísticas Generales

### Por Tecnología
```
NestJS Projects:      8
Angular Projects:     5
IoT Projects:         2
Full Stack Apps:      10
Learning Projects:    20+
Open Source:          54 repos
```

### Por Complejidad
```
Production Ready:     3 ⭐⭐⭐⭐⭐
Advanced:            5 ⭐⭐⭐⭐
Intermediate:        15 ⭐⭐⭐
Learning:            31 ⭐⭐
```

---

## 🎯 Proyectos en Desarrollo

### En Progreso
- 🔄 **Microservices Architecture** - Sistema distribuido con NestJS
- 🔄 **GraphQL Gateway** - API Gateway con Apollo Server
- 🔄 **Real-time Dashboard** - Dashboard con WebSockets y Charts

### Planificados
- 📅 **Mobile App (Ionic/React Native)** - App móvil para e-commerce
- 📅 **Blockchain Integration** - Smart contracts básicos
- 📅 **AI/ML Integration** - Recomendaciones de productos con ML

---

## 🏆 Proyectos Destacados por Habilidad

### Best Practices & Architecture
- ⭐ **Teslo Shop Backend** - Clean architecture, SOLID principles
- ⭐ **Auth Microservice** - JWT, OAuth, role-based access

### UI/UX Design
- ⭐ **Teslo Shop Frontend** - Modern Angular with TailwindCSS
- ⭐ **Admin Dashboard** - Responsive admin panel

### Real-time Features
- ⭐ **Chat Application** - Socket.IO real-time messaging
- ⭐ **Live Notifications** - WebSocket notifications

### IoT & Hardware
- ⭐ **Motion Detector** - Arduino + Raspberry Pi integration
- ⭐ **Smart Home System** - Home automation prototype

---

## 📞 Colaboraciones

¿Interesado en colaborar en algún proyecto? ¡Contáctame!

- 📧 Email: [tu-email@gmail.com](mailto:tu-email@gmail.com)
- 🐦 Twitter: [@davSaged](https://twitter.com/davSaged)
- 💼 Portfolio: [adavilag-portfolio.vercel.app](https://adavilag-portfolio.vercel.app/)

---

<div align="center">

**🌟 Todos los proyectos están disponibles en mi [GitHub](https://github.com/Adravilag)**

[← Volver al README principal](README.md)

</div>
