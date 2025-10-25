# CodeSimpler

AI-powered code explanation tool. Paste your code and get simple explanations.

## Setup

### Backend
```bash
cd server
npm install
```

Create `server/.env`:
```env
NEBIUS_API_KEY=your_api_key_here
FRONTEND_URL=http://localhost:5173
PORT=3001
```

### Frontend
```bash
cd codesimpler
npm install
```

Create `codesimpler/.env`:
```env
VITE_API_BASE_URL=http://localhost:3001
```

## Run

```bash
# Terminal 1 - Backend
cd server
npm run dev

# Terminal 2 - Frontend
cd codesimpler
npm run dev
```

Open `http://localhost:5173`
