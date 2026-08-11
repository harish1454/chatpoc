# ChatPOC

A real-time messaging proof-of-concept application built with Node.js. This project explores core chat functionality including instant messaging, room-based conversations, and WebSocket communication patterns.

## Features

- Real-time bidirectional messaging via WebSockets
- Room-based chat (create, join, and leave rooms)
- User presence indicators (online/offline status)
- Message history and persistence
- Typing indicators
- Lightweight and minimal dependencies

## Tech Stack

| Layer      | Technology           |
|------------|----------------------|
| Runtime    | Node.js              |
| Transport  | WebSocket (Socket.IO)|
| Server     | Express.js           |
| Client     | HTML/CSS/JavaScript  |
| Storage    | In-memory (POC)      |

## Project Structure

```
chatpoc/
├── server/
│   ├── index.js          # Entry point, server setup
│   ├── socket.js         # WebSocket event handlers
│   └── rooms.js          # Room management logic
├── client/
│   ├── index.html        # Chat UI
│   ├── styles.css        # Styling
│   └── app.js            # Client-side socket logic
├── package.json
├── .env.example          # Environment variable template
├── LICENSE
└── README.md
```

## Prerequisites

- [Node.js](https://nodejs.org/) v16 or higher
- npm (included with Node.js) or yarn

 

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/harish1454/chatpoc.git
cd chatpoc
```

### 2. Install dependencies

```bash
npm install
```

### 3. Configure environment (optional)

Copy the example environment file and adjust values as needed:

```bash
cp .env.example .env
```

| Variable | Default | Description             |
|----------|---------|-------------------------|
| `PORT`   | `3000`  | Server listening port   |

### 4. Start the server

```bash
npm start
```

The application will be available at `http://localhost:3000`.

### 5. Development mode

For automatic restarts on file changes:

```bash
npm run dev
```

## Usage

1. Open `http://localhost:3000` in your browser.
2. Enter a username to join the chat.
3. Create a new room or join an existing one.
4. Start sending messages in real time.
5. Open multiple browser tabs to simulate multiple users.

## API / Socket Events

### Client to Server

| Event           | Payload                        | Description                    |
|-----------------|--------------------------------|--------------------------------|
| `join_room`     | `{ room, username }`           | Join a chat room               |
| `leave_room`    | `{ room }`                     | Leave a chat room              |
| `send_message`  | `{ room, message }`            | Send a message to a room       |
| `typing`        | `{ room, username }`           | Notify room that user is typing|

### Server to Client

| Event           | Payload                        | Description                    |
|-----------------|--------------------------------|--------------------------------|
| `new_message`   | `{ username, message, time }`  | Broadcast a new message        |
| `user_joined`   | `{ username }`                 | Notify room of new user        |
| `user_left`     | `{ username }`                 | Notify room that user left     |
| `user_typing`   | `{ username }`                 | Broadcast typing indicator     |
| `room_users`    | `[{ username, status }]`       | Current users in the room      |

## Scripts

| Command         | Description                            |
|-----------------|----------------------------------------|
| `npm start`     | Start the production server            |
| `npm run dev`   | Start with hot-reload (nodemon)        |
| `npm test`      | Run the test suite                     |
| `npm run lint`  | Run ESLint checks                      |

## Roadmap

- [ ] Persistent message storage (database integration)
- [ ] User authentication and authorization
- [ ] File and image sharing
- [ ] Message read receipts
- [ ] End-to-end encryption
- [ ] Deployment configuration (Docker, CI/CD)

## Contributing

Contributions are welcome! To get started:

1. Fork the repository.
2. Create a feature branch: `git checkout -b feature/your-feature`.
3. Commit your changes: `git commit -m "feat: add your feature"`.
4. Push to the branch: `git push origin feature/your-feature`.
5. Open a pull request.

For major changes, please open an issue first to discuss what you would like to change.

## License

This project is licensed under the [MIT License](LICENSE).
