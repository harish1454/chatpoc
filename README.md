# chatpoc

A proof-of-concept chat application demonstrating real-time messaging capabilities. This project explores core chat features such as sending and receiving messages, basic user identification, and live updates between connected clients.

## Overview

**chatpoc** is a lightweight proof-of-concept (POC) built to validate and demonstrate real-time chat functionality. The goal is to provide a minimal but functional implementation that can serve as a foundation for more complex messaging systems. It is intended for learning, prototyping, and evaluating technologies suitable for real-time communication.

## Features

- Real-time messaging between multiple connected users
- Simple user identification (username-based)
- Live updates pushed to all participants without page refresh
- Message history displayed on connection
- Minimalist user interface for sending and viewing messages
- Lightweight server with WebSocket support

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Runtime | Node.js |
| Real-time Communication | Socket.IO (WebSocket with fallback) |
| Frontend | Vanilla JavaScript / HTML / CSS |
| Data Store | In-memory (suitable for POC; no external database required) |

## Project Structure

```
chatpoc/
├── public/             # Static frontend assets
│   ├── index.html      # Chat UI
│   ├── style.css       # Styles
│   └── client.js       # Client-side Socket.IO logic
├── src/                # Server-side source code
│   └── chat.js         # Chat event handlers
├── server.js           # Application entry point
├── package.json        # Dependencies and scripts
├── .env.example        # Example environment variables
├── LICENSE             # MIT license
└── README.md           # Project documentation
```

## Configuration

The application can be configured using environment variables. Copy `.env.example` to `.env` and adjust as needed.

| Variable | Description | Default |
|----------|-------------|---------|
| `PORT` | Port the server listens on | `3000` |
| `NODE_ENV` | Environment mode (`development` or `production`) | `development` |

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) v16 or later
- npm (included with Node.js), yarn, or pnpm

### Installation

```bash
git clone https://github.com/harish1454/chatpoc.git
cd chatpoc
npm install
```

### Running the App

Start the server in production mode:

```bash
npm start
```

The application will be available at `http://localhost:3000` (or the port specified in your `.env` file).

## Development

Start the server in development mode with automatic restart on file changes:

```bash
npm run dev
```

This uses [nodemon](https://nodemon.io/) (or a similar file watcher) to detect changes in server-side files and restart the process automatically. Hot reload keeps the feedback loop short while iterating on features.

To run in development mode manually without a file watcher:

```bash
NODE_ENV=development node server.js
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m "feat: add your feature"`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a pull request

## License

[MIT](LICENSE)
