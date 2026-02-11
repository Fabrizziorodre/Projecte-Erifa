```markdown
# Erifa E-Commerce Platform

## Descripción
Plataforma de e-commerce modular construida con microservicios, diseñada para escalabilidad y mantenibilidad.

## Quick Start
1. Clona el repositorio:
   ```bash
   git clone https://github.com/tu-org/erifa.git
   cd erifa
   ```
2. Instala dependencias:
   ```bash
   npm install
   cd frontend && npm install
   cd ../backend && npm install
   ```
3. Configura variables de entorno:
   ```bash
   cp .env.example .env
   # Edita .env con tus credenciales
   ```
4. Inicia los servicios:
   ```bash
   npm run dev          # Desarrollo
   npm run build        # Producción
   npm run test         # Tests
   ```

## Arquitectura
- **Frontend**: React/Next.js con TypeScript
- **Backend**: Node.js/Express con TypeScript
- **Base de datos**: PostgreSQL con Redis para caché
- **Autenticación**: JWT con refresh tokens
- **Pagos**: Stripe integration
- **File Storage**: AWS S3
- **Queue**: Bull Queue con Redis
- **Monitoring**: Prometheus + Grafana

## Estructura del Proyecto
```
erifa/
├── frontend/          # Aplicación Next.js
├── backend/           # API REST
├── shared/            # Tipos y utilidades compartidas
├── docs/              # Documentación técnica
├── scripts/           # Scripts de despliegue
└── docker/            # Configuraciones Docker
```

## Variables de Entorno
```bash
# Database
DATABASE_URL=postgresql://user:pass@localhost:5432/erifa
REDIS_URL=redis://localhost:6379

# Auth
JWT_SECRET=your-secret
JWT_REFRESH_SECRET=your-refresh-secret

# Payments
STRIPE_SECRET_KEY=sk_test_...
STRIPE_WEBHOOK_SECRET=whsec_...

# Storage
AWS_ACCESS_KEY_ID=...
AWS_SECRET_ACCESS_KEY=...
AWS_S3_BUCKET=erifa-uploads
```

## Endpoints Principales
- `POST /api/auth/login` - Inicio de sesión
- `POST /api/auth/register` - Registro
- `GET /api/products` - Listado de productos
- `POST /api/orders` - Crear orden
- `GET /api/orders/:id` - Detalles de orden

## Desarrollo
```bash
# Frontend
cd frontend
npm run dev          # http://localhost:3000

# Backend
cd backend
npm run dev          # http://localhost:8000

# Base de datos
npm run db:migrate   # Ejecutar migraciones
npm run db:seed      # Poblar datos de prueba
```

## Tests
```bash
npm run test         # Todos los tests
npm run test:unit    # Tests unitarios
npm run test:e2e     # Tests end-to-end
```

## Despliegue
### Docker
```bash
docker-compose up -d
```

### Producción
```bash
npm run build
npm run start
```

## Contribuyendo
1. Fork del repositorio
2. Crear rama de feature: `git checkout -b feature/nueva-funcionalidad`
3. Commits descriptivos: `git commit -m "feat: agregar checkout de Stripe"`
4. Push: `git push origin feature/nueva-funcionalidad`
5. Pull Request con template completo

## Code Style
- ESLint + Prettier configurados
- Commits convencionales (Conventional Commits)
- TypeScript strict mode activado

## Soporte
- 📧 Email: support@erifa.com
- 💬 Discord: [invitación]
- 📖 Docs: https://docs.erifa.com
``` [1](#1-0) 

- Las secciones de testing y code style aseguran calidad y consistencia en el código base [3](#1-2) .

### Citations

