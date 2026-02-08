# OmniLLM Unified Hub

An integrated AI chat interface supporting multiple LLM providers (DeepSeek, Kimi/Nvidia) with a local proxy server for enhanced connectivity.

## Features

- **Multi-Model Support**: Chat with DeepSeek and Kimi (Nvidia) models.
- **Local Proxy Server**: Built-in Express proxy to handle API requests and manage SOCKS5 proxying.
- **Modern UI**: React-based interface with debug console and chat history.
- **Debug Mode**: Real-time request/response logging for development.

## Prerequisites

- Node.js (v16 or higher recommended)
- API Keys for DeepSeek and/or Kimi (Nvidia)

## Setup

1. **Install Dependencies**

   ```bash
   npm install
   ```

2. **Configure Environment Variables**

   Create a `.env.local` file in the root directory with your API keys:

   ```env
   # API Keys
   DEEPSEEK_API_KEY=your_deepseek_key_here
   KIMI_API_KEY=your_kimi_key_here
   GEMINI_API_KEY=your_gemini_key_here

   # Optional: Proxy Configuration (if needed)
   ALL_PROXY=socks5://127.0.0.1:12345
   ```

## Running the Application

This application requires both the backend proxy server and the frontend client to be running.

1. **Start the Backend Proxy Server** (Terminal 1)

   This server runs on port 3001 and handles API requests.

   ```bash
   node server.js
   ```

2. **Start the Frontend Development Server** (Terminal 2)

   This runs the React application on port 3000.

   ```bash
   npm run dev
   ```

3. **Access the App**

   Open your browser and navigate to `http://localhost:3000` (or the URL shown in your terminal).

## Project Structure

- `src/` - React frontend source code
- `server.js` - Express backend proxy server
- `vite.config.ts` - Vite configuration
