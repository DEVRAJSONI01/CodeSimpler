# CodeSimpler

An AI-powered code explanation tool that helps developers understand code snippets in simple terms. Built with React (Vite) frontend and Express.js backend, powered by Nebius AI.

## Features

- 🤖 AI-powered code explanations
- 💻 Support for multiple programming languages (JavaScript, Python, Java, C++, Go, Rust)
- 🎨 Clean and modern UI with Tailwind CSS
- 🔒 Security features (Helmet, CORS, Rate Limiting)
- ⚡ Fast and responsive

## Tech Stack

### Frontend
- React 18 with Vite
- Tailwind CSS
- React Markdown with GitHub Flavored Markdown support

### Backend
- Node.js with Express
- OpenAI SDK (configured for Nebius AI)
- Security middleware (Helmet, CORS, Rate Limiting)

## Project Structure

```
Project/
├── codesimpler/          # React frontend
│   ├── src/
│   │   ├── components/   # React components
│   │   ├── actions/      # Server actions
│   │   └── ...
│   └── package.json
├── server/               # Express backend
│   ├── server.js         # Main server file
│   └── package.json
└── README.md
```

## Prerequisites

- Node.js (v18 or higher)
- npm or yarn
- Nebius AI API Key

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/DEVRAJSONI01/CodeSimpler.git
cd CodeSimpler
```

### 2. Set up the Backend

```bash
cd server
npm install
```

Create a `.env` file in the `server` directory:

```env
NEBIUS_API_KEY=your_nebius_api_key_here
FRONTEND_URL=http://localhost:5173
PORT=3001
```

### 3. Set up the Frontend

```bash
cd ../codesimpler
yarn install
# or
npm install
```

Create a `.env` file in the `codesimpler` directory:

```env
VITE_API_BASE_URL=http://localhost:3001
```

## Running the Application

### Start the Backend Server

```bash
cd server
npm run dev
```

The server will start on `http://localhost:3001`

### Start the Frontend

Open a new terminal window:

```bash
cd codesimpler
yarn dev
# or
npm run dev
```

The frontend will start on `http://localhost:5173`

## Usage

1. Open your browser and navigate to `http://localhost:5173`
2. Select the programming language from the dropdown
3. Paste your code in the textarea
4. Click "Explain Code"
5. Wait for the AI to generate a simple explanation

## API Endpoints

### POST `/api/explain-code`

Explains the provided code snippet.

**Request Body:**
```json
{
  "code": "console.log('Hello World');",
  "language": "JavaScript"
}
```

**Response:**
```json
{
  "explanation": "Detailed explanation of the code...",
  "language": "JavaScript"
}
```

## Security Features

- **Helmet**: Secures HTTP headers
- **CORS**: Configured for cross-origin requests
- **Rate Limiting**: 100 requests per 15 minutes per IP

## Environment Variables

### Backend (`server/.env`)
- `NEBIUS_API_KEY`: Your Nebius AI API key
- `FRONTEND_URL`: Frontend URL for CORS (default: `http://localhost:5173`)
- `PORT`: Server port (default: `3001`)

### Frontend (`codesimpler/.env`)
- `VITE_API_BASE_URL`: Backend API URL (default: `http://localhost:3001`)

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the ISC License.

## Author

**Devraj Soni**
- GitHub: [@DEVRAJSONI01](https://github.com/DEVRAJSONI01)

## Acknowledgments

- Powered by [Nebius AI](https://nebius.com/)
- Built with [Vite](https://vitejs.dev/)
- Styled with [Tailwind CSS](https://tailwindcss.com/)

---

Made with ❤️ by Devraj Soni
