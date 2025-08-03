# AI Engineer Challenge Frontend

A modern, responsive chat interface built with Next.js that integrates with the FastAPI backend to provide a seamless experience for chatting with OpenAI GPT models.

## Features

- 🎨 **Modern UI/UX**: Clean, responsive design with smooth animations
- 💬 **Real-time Chat**: Streaming responses from OpenAI models
- ⚙️ **Configurable Settings**: Customize model, system message, and API key
- 🔒 **Secure**: Password field for API key input
- 📱 **Responsive**: Works on desktop and mobile devices
- 🎯 **User-friendly**: Intuitive interface with clear visual feedback

## Prerequisites

- Node.js 18+ installed
- The FastAPI backend running on `http://localhost:8000`
- An OpenAI API key

## Installation

1. Navigate to the frontend directory:
   ```bash
   cd frontend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

## Running the Application

1. **Start the backend first** (from the `api` directory):
   ```bash
   cd ../api
   python -m uvicorn app:app --reload --host 0.0.0.0 --port 8000
   ```

2. **Start the frontend** (in a new terminal, from the `frontend` directory):
   ```bash
   npm run dev
   ```

3. Open your browser and navigate to `http://localhost:3000`

## Usage

1. **Configure Settings**: Click the settings icon to configure your OpenAI API key, model selection, and system message
2. **Start Chatting**: Type your message and press Enter or click Send
3. **View Responses**: Watch as the AI responds in real-time with streaming text
4. **Clear Chat**: Use the "Clear Chat" button to start a new conversation

## Technology Stack

- **Framework**: Next.js 14 with App Router
- **Styling**: Tailwind CSS
- **Icons**: Lucide React
- **Language**: TypeScript
- **Deployment**: Vercel-ready

## Project Structure

```
frontend/
├── app/
│   ├── globals.css          # Global styles and Tailwind config
│   ├── layout.tsx           # Root layout component
│   └── page.tsx             # Main chat interface
├── package.json             # Dependencies and scripts
├── next.config.js           # Next.js configuration
├── tailwind.config.js       # Tailwind CSS configuration
├── tsconfig.json            # TypeScript configuration
└── README.md                # This file
```

## Deployment

This frontend is configured for easy deployment on Vercel:

1. Push your code to GitHub
2. Connect your repository to Vercel
3. Deploy with the default settings

The `next.config.js` includes API rewrites to handle backend communication in production.

## API Integration

The frontend communicates with the FastAPI backend through:
- **Chat Endpoint**: `/api/chat` for sending messages and receiving streaming responses
- **Health Check**: `/api/health` for backend status verification

## Contributing

Feel free to enhance the interface with additional features like:
- Message history persistence
- Multiple chat sessions
- File upload capabilities
- Voice input/output
- Custom themes