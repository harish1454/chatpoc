# ChatPOC

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Node.js](https://img.shields.io/badge/Node.js-18%2B-green.svg)](https://nodejs.org/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/harish1454/chatpoc/pulls)

A proof-of-concept real-time chat application built with Node.js and Socket.IO.

---

## Table of Contents

- [About](#about)
- [Project Status](#project-status)
- [Planned Features](#planned-features)
- [Tech Stack](#tech-stack)
- [Planned Architecture](#planned-architecture)
- [Getting Started](#getting-started)
- [Configuration](#configuration)
- [Planned API / Socket Events](#planned-api--socket-events)
- [Roadmap](#roadmap)
- [Contributing](#contributing)
- [License](#license)

---

## About

ChatPOC is a proof-of-concept project exploring real-time messaging capabilities using WebSockets. The goal is to build a lightweight, functional chat application that demonstrates core real-time communication patterns: instant messaging, presence detection, room-based conversations, and typing indicators.

This project serves as a learning tool and foundation for understanding how real-time web applications work under the hood. It intentionally keeps the stack simple (vanilla frontend, in-memory storage) to focus on the WebSocket communication layer without the complexity of a full production framework.

> **Note:** This project is currently in its early planning and scaffolding phase. The repository does not yet contain application source code. Contributions and feedback on the planned architecture are welcome.

---

## Project Status

> **Status: Planning / Scaffolding**

This repository is in the initial setup stage. The planned architecture and feature set are documented below, but implementation has not yet begun. Check the [Roadmap](#roadmap) section for upcoming milestones.

---

## Planned Features

- Real-time messaging via WebSockets (with HTTP long-polling fallback)
- Room-based chat: create, join, and leave chat rooms
- User presence indicators (online/offline status)
- Typing indicators (see when others are typing)
- Message history within a session
- Read receipts for delivered messages
- Responsive UI that works on desktop and mobile browsers

---

## Tech Stack

| Layer        | Technology                              | Notes                                      |
| ------------ | --------------------------------------- | ------------------------------------------ |
| Runtime      | Node.js (v18+)                          | LTS version recommended                    |
| Framework    | Express.js                              | Serves static files and handles HTTP routes |
| Real-time    | Socket.IO                               | WebSocket with automatic fallback           |
| Frontend     | Vanilla HTML / CSS / JavaScript         | No framework dependency for the POC         |
| Storage      | In-memory                               | POC phase; database integration planned     |
| Dev tooling  | nodemon, ESLint                         | Live reload and code quality                |

---

## Planned Architecture

> **Note:** The following directory structure represents the **target layout** for this project. These files and folders do not exist yet.

```
chatpoc/
├── src/
│   ├── server.js          # Application entry point
│   ├── socket/
│   │   ├── handlers.js    # WebSocket event handlers
│   │   └── rooms.js       # Room management logic
│   └── config.js          # Server configuration
├── public/
│   ├── index.html         # Chat UI
│   ├── css/
│   │   └── styles.css     # Application styles
│   └── js/
│       └── client.js      # Client-side Socket.IO logic
├── tests/
│   └── ...                # Test suite
├── package.json
├── .env.example
├── LICENSE
└── README.md
```

---

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) v18 or higher
- npm, yarn, or pnpm
- [Git](https://git-scm.com/)

### Installation

```bash
# Clone the repository
git clone https://github.com/harish1454/chatpoc.git
cd chatpoc

# Install dependencies
npm install

# Copy environment configuration
cp .env.example .env

# Start the application
npm start
```

### Development Mode

For automatic restarts on file changes during development:

```bash
npm run dev
```

This uses [nodemon](https://nodemon.io/) to watch for changes and restart the server automatically.

> **Note:** These commands will work once the project scaffolding is in place. Currently, no `package.json` or source files exist in the repository.

---

## Configuration

| Variable   | Description                  | Default       |
| ---------- | ---------------------------- | ------------- |
| `PORT`     | Port the server listens on   | `3000`        |
| `NODE_ENV` | Application environment mode | `development` |

Configuration is loaded from a `.env` file in the project root. See `.env.example` (planned) for a full template.

---

## Planned API / Socket Events

> **Note:** These events represent the intended WebSocket interface. They will be implemented as part of the real-time core milestone.

### Client-to-Server Events

| Event          | Payload                          | Description                        |
| -------------- | -------------------------------- | ---------------------------------- |
| `join_room`    | `{ room: string, user: string }` | Join a specific chat room          |
| `leave_room`   | `{ room: string }`               | Leave the current chat room        |
| `send_message` | `{ room: string, text: string }` | Send a message to a room           |
| `typing`       | `{ room: string, user: string }` | Notify the room that user is typing |

### Server-to-Client Events

| Event          | Payload                                        | Description                              |
| -------------- | ---------------------------------------------- | ---------------------------------------- |
| `new_message`  | `{ user: string, text: string, time: string }` | Broadcast a new message to room members  |
| `user_joined`  | `{ user: string, room: string }`               | Notify room that a user joined           |
| `user_left`    | `{ user: string, room: string }`               | Notify room that a user left             |
| `user_typing`  | `{ user: string }`                             | Broadcast typing indicator to room       |
| `room_users`   | `{ users: string[] }`                          | Updated list of users in the room        |

---

## Roadmap

### Phase 1: Foundation

- [ ] Initialize project with `package.json`
- [ ] Set up Express.js server with static file serving
- [ ] Create basic HTML/CSS chat interface
- [ ] Add development tooling (nodemon, ESLint)

### Phase 2: Real-time Core

- [ ] Integrate Socket.IO on server and client
- [ ] Implement basic message send/receive
- [ ] Add user nickname selection on connect

### Phase 3: Chat Rooms

- [ ] Room creation and listing
- [ ] Join/leave room functionality
- [ ] Room-scoped messaging

### Phase 4: Persistence and Features

- [ ] In-memory message history
- [ ] Typing indicators
- [ ] User presence (online/offline)
- [ ] Read receipts

### Phase 5: Polish

- [ ] Responsive UI improvements
- [ ] Error handling and reconnection logic
- [ ] Unit and integration tests
- [ ] Documentation and deployment guide

---

## Contributing

Contributions are welcome! This project is in its early stages, so there are many opportunities to help shape its direction.

### How to Contribute

1. **Fork** the repository
2. **Create** a feature branch from `master`
3. **Commit** your changes using conventional commit messages
4. **Push** your branch to your fork
5. **Open** a Pull Request against `master`

### Branch Naming Conventions

| Type        | Pattern                | Example                    |
| ----------- | ---------------------- | -------------------------- |
| Feature     | `feat/<description>`   | `feat/add-typing-indicator`|
| Bug fix     | `fix/<description>`    | `fix/reconnect-logic`      |
| Docs        | `docs/<description>`   | `docs/update-readme`       |
| Refactor    | `refactor/<description>` | `refactor/socket-handlers` |
| Chore       | `chore/<description>`  | `chore/update-deps`        |

### Commit Message Format

This project follows [Conventional Commits](https://www.conventionalcommits.org/):

```
<type>: <short description>

[optional body]

[optional footer]
```

Types: `feat`, `fix`, `docs`, `style`, `refactor`, `test`, `chore`

Example:

```
feat: add room creation functionality

Implement the join_room and leave_room socket events.
Users can now create and switch between chat rooms.
```

---

## License

This project is licensed under the [MIT License](LICENSE).
