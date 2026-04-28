# ChatPOC

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Node.js](https://img.shields.io/badge/Node.js-18%2B-green.svg)](https://nodejs.org/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/harish1454/chatpoc/pulls)

> A proof-of-concept chat application exploring real-time messaging with modern web technologies.

---

## Table of Contents

- [Overview](#overview)
- [Planned Features](#planned-features)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Project Structure](#project-structure)
- [Roadmap](#roadmap)
- [Contributing](#contributing)
- [License](#license)

## Overview

**ChatPOC** is a proof-of-concept project designed to explore and validate real-time messaging patterns for chat applications. The goal is to build a lightweight, functional chat system that can serve as a foundation for more complex communication platforms.

This project focuses on understanding the core mechanics of real-time communication, including message delivery, connection management, and scalable architecture.

## Planned Features

- **Real-time messaging** -- instant message delivery between connected users
- **WebSocket support** -- persistent, bidirectional communication channels
- **Multiple chat rooms** -- ability to create and join different conversation spaces
- **User presence indicators** -- see who is online and active
- **Message history** -- persist and retrieve previous conversations
- **Typing indicators** -- real-time feedback when another user is composing a message
- **Read receipts** -- confirmation that messages have been seen

## Tech Stack

| Layer       | Technology                          |
|-------------|-------------------------------------|
| Runtime     | [Node.js](https://nodejs.org/) 18+  |
| Framework   | Express.js (planned)                |
| Real-time   | Socket.IO / WebSockets (planned)    |
| Database    | MongoDB or SQLite (TBD)             |
| Frontend    | HTML/CSS/JS or React (TBD)          |

> **Note:** The tech stack is subject to change as the project evolves. Decisions will be documented in future updates.

## Getting Started

### Prerequisites

Before you begin, make sure you have the following installed:

- **Node.js** (v18 or higher) -- [Download here](https://nodejs.org/)
- **npm** (comes with Node.js) or an alternative package manager (yarn, pnpm)
- **Git** -- [Download here](https://git-scm.com/)

### Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/harish1454/chatpoc.git
   cd chatpoc
   ```

2. **Install dependencies:**

   ```bash
   npm install
   ```

3. **Set up environment variables** (if applicable):

   ```bash
   cp .env.example .env
   ```

   Update the `.env` file with your configuration values.

### Running the Application

Start the development server:

```bash
npm start
```

The application will be available at `http://localhost:3000` (default port).

## Project Structure

```
chatpoc/
├── README.md          # Project documentation
├── LICENSE            # MIT license
└── ...                # Source files (coming soon)
```

> **Note:** This section will be updated as the project structure takes shape. Planned directories include `src/` for server-side code, `public/` for static assets, and `tests/` for test suites.

## Roadmap

The following milestones outline the planned development path:

- [ ] **Phase 1 -- Foundation**
  - Project scaffolding and initial setup
  - Basic Express.js server
  - Static file serving

- [ ] **Phase 2 -- Real-time Core**
  - WebSocket integration with Socket.IO
  - Basic one-on-one messaging
  - Connection and disconnection handling

- [ ] **Phase 3 -- Chat Rooms**
  - Multi-room support
  - Room creation and joining
  - User presence per room

- [ ] **Phase 4 -- Persistence**
  - Database integration for message storage
  - Message history retrieval
  - User session management

- [ ] **Phase 5 -- Polish**
  - Typing indicators and read receipts
  - Improved UI/UX
  - Error handling and reconnection logic
  - Performance testing

## Contributing

Contributions are welcome and appreciated! Here is how you can get involved:

### How to Contribute

1. **Fork** the repository
2. **Create a feature branch** from `master`:
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. **Make your changes** and commit with a clear message:
   ```bash
   git commit -m "feat: add your feature description"
   ```
4. **Push** to your fork:
   ```bash
   git push origin feature/your-feature-name
   ```
5. **Open a Pull Request** against the `master` branch

### Branch Naming Convention

| Prefix       | Purpose                    |
|--------------|----------------------------|
| `feature/`   | New features               |
| `fix/`       | Bug fixes                  |
| `docs/`      | Documentation changes      |
| `refactor/`  | Code refactoring           |
| `test/`      | Adding or updating tests   |

### Commit Message Format

Use [Conventional Commits](https://www.conventionalcommits.org/) style:

- `feat:` -- a new feature
- `fix:` -- a bug fix
- `docs:` -- documentation only changes
- `refactor:` -- code change that neither fixes a bug nor adds a feature
- `test:` -- adding or correcting tests

### Guidelines

- For **major changes**, please open an issue first to discuss what you would like to change.
- Make sure your code follows the existing style and conventions.
- Include tests for new functionality when applicable.
- Keep pull requests focused -- one feature or fix per PR.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

<p align="center">
  Built with curiosity and caffeine.
</p>
