# Docker

Postgres 16, Redis 7, y las imágenes de la API y la SPA.

Los tres repos viven como carpetas hermanas:

```
quierounsms/
  docker/
  backend/
  frontend/
```

## Todo el stack

```bash
docker compose up --build
```

- App: http://localhost:3000
- API: http://localhost:4000
- Postgres: `localhost:5432` (`quierounsms` / `quierounsms`)
- Redis: `localhost:6379`

El contenedor del backend aplica el esquema y carga los números de demostración al arrancar. Ese seed reinicia las sesiones.

## Solo bases de datos

Para desarrollar con recarga en caliente:

```bash
docker compose up -d postgres redis
```

Luego arranca `backend` y `frontend` con `npm run dev`, como indican sus README.
