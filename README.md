# Pretch

Sistema de gestión de gimnasios construido como monorepo. Incluye una app mobile para clientes y un dashboard web para gimnasios, conectados a un backend común.

## Stack tecnológico

| Capa | Tecnología |
|---|---|
| App Mobile | React Native |
| Dashboard Web | Next.js |
| Backend | NestJS |
| Base de datos | PostgreSQL |
| ORM | Prisma |

## Estructura del repositorio
```
gym-saas/
├── .github/                         # Configuración de GitHub
│   ├── PULL_REQUEST_TEMPLATE.md     # Template para pull requests
│   └── ISSUE_TEMPLATE/              # Templates para issues
│       ├── bug_report.md            # Reporte de bugs
│       └── feature_request.md       # Solicitud de features
├── apps/
│   ├── mobile/                      # App mobile en React Native
│   ├── frontend/                         # Dashboard web en Next.js
│   └── backend/                         # Backend en NestJS
├── packages/
│   └── shared/                      # Código compartido entre apps
├── docker-compose.yml               # Base de datos local
├── .gitignore
└── package.json                     # Configuración del monorepo
```

## Ramas

| Rama | Descripción |
|---|---|
| `main` | Producción, solo recibe merges desde `develop` |
| `develop` | Integración, rama principal de desarrollo |
| `feature/nombre` | Nueva funcionalidad |
| `fix/nombre` | Corrección de bug |

## Flujo de trabajo

1. Crear rama desde `develop`
2. Desarrollar y commitear siguiendo las convenciones
3. Abrir PR hacia `develop` con el template correspondiente
4. Esperar aprobación de al menos 1 reviewer
5. Mergear a `develop`

## Configuración local

### Requisitos
- Node.js
- Docker

### Pasos
1. Clonar el repositorio
```bash
git clone https://github.com/nombre-org/gym-saas.git
```

2. Instalar dependencias
```bash
npm install
```

3. Levantar la base de datos
```bash
docker compose up -d
```

4. Configurar variables de entorno
```bash
cp .env.example .env
```

## Equipos

| Equipo | Responsabilidad |
|---|---|
| Backend | NestJS, Prisma, PostgreSQL |
| Frontend | Next.js, dashboard web |
| Mobile | React Native, app del cliente |
| Design & Marketing | Diseño y contenido |
