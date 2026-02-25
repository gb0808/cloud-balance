# Cloud Balance Project
Full-Stack App (React + Express + PostgreSQL)

Cloud Balance is a lightweight cloud project management dashboard built as a full-stack application.

## Features

- Authentication (Register / Login)

- Dashboard overview

- Create new project

- Account management
  
- Logout(session-based authentication)

## Tech Stack
### Frontend

- React (Vite)

- React Router

- Custom CSS (SaaS-style UI)

### Backend

- Node.js

- Express.js

- PostgreSQL

- express-session (cookie-based auth)
## Prereqs
- Node.js 18+ (or 20+)
- Docker Desktop (recommended, for Postgres)

## Quick Start (recommended)
### 1) Start Postgres
```bash
cd server
docker compose up -d
```

### 2) Configure environment
```bash
cp .env.example .env
```
(Defaults are already correct for the docker-compose Postgres.)
### Update .env if needed:

```bash
PORT=5001
CLIENT_ORIGIN=http://localhost:5173
PGHOST=localhost
PGPORT=5432
PGUSER=cloudbalance
PGPASSWORD=cloudbalance
PGDATABASE=cloudbalance
SESSION_SECRET=your_secret
```


### 3) Install + run server
```bash
cd server
npm install
npm run db:init
npm run dev
```

Server runs at: http://localhost:5000

### 4) Install + run client
Open a new terminal:
```bash
cd client
npm install
cp .env.example .env
npm run dev
```
### Update .env if needed:

```bash
VITE_API_BASE=http://localhost:5001
```

Client runs at: http://localhost:5173

## Test Accounts
Create an account on /auth, then log in.

## Authentication

- Session-based authentication (HTTP-only cookies)

- Projects are scoped to logged-in user

## Development Notes

- Backend API routes: /auth, /projects

- Database schema located in: server/src/db/schema.sql

- API wrapper located in: client/src/api.js

## Future Improvements

- Edit & delete projects

- Real-time monitoring

- Role-based access

- Production deployment setup
