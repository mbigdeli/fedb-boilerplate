# Boiler Plate for NestJS and React(Vite) 
A full-stack application with React frontend and NestJS backend

## Tech Stack

### Frontend
- React with TypeScript
- Vite
- Docker support
- Hot reload enabled

### Backend
- NestJS
- PostgreSQL with TypeORM
- JWT Authentication
- Docker support with Nodemon hot reload

### Development Tools
- Docker & Docker Compose
- Adminer for database management
- Environment configuration
- TypeScript

## Getting Started

### Prerequisites
- Docker and Docker Compose
- Node.js (for local development)

### Environment Setup
1. Copy the example environment files:
```bash
cp .env.example .env
cp backend/.env.example backend/.env
cp frontend/.env.example frontend/.env
```

2. Update the environment variables as needed

### Running with Docker
```bash
# Start all services
docker compose up

# Rebuild if needed
docker compose up --build

# Stop all services
docker compose down
```

### Access Points
- Frontend: http://localhost:3001
- Backend API: http://localhost:3000
- Adminer (Database Management): http://localhost:8080
- PostgreSQL: localhost:5432

## Development

### Frontend Development
The frontend runs on Vite with hot reload enabled. Any changes to the frontend code will automatically reflect in the browser.

### Backend Development
The backend uses Nodemon for development, providing automatic restart on code changes.

### Database
PostgreSQL is used as the database, with Adminer providing a web interface for database management.

## Project Structure
```
.
├── frontend/                # React frontend
│   ├── src/                # Source files
│   ├── public/             # Public assets
│   └── Dockerfile         # Frontend Docker configuration
├── backend/                # NestJS backend
│   ├── src/               # Source files
│   ├── test/              # Test files
│   └── Dockerfile        # Backend Docker configuration
├── docker-compose.yml     # Docker compose configuration
└── .env                   # Root environment variables
``` 