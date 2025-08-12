# Boxels Backend (FastAPI)

Backend en Python (FastAPI) con autenticación JWT y SQLite para integrarse con el frontend Boxels.

## Instalación y ejecución (desarrollo)

```bash
cd boxels-backend-fastapi
python -m venv .venv
source .venv/bin/activate   # Linux/Mac
.venv\Scripts\activate    # Windows (PowerShell)
pip install -r requirements.txt
uvicorn app.main:app --reload --port 8000
```

## Endpoints principales

- POST /api/auth/register  -> { username, email, password, role }
- POST /api/auth/token     -> form-data (username, password)  (retorna access_token)
- GET  /api/users/me       -> info del usuario (autenticado)
- GET  /api/users          -> lista usuarios (admin only)
- GET  /api/items          -> lista items (público)
- POST /api/items          -> crea item (autenticado)
- GET  /api/items/me       -> items del usuario (autenticado)
