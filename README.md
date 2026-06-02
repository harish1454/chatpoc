# ChatPOC

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/harish1454/chatpoc/pulls)

> **This project is currently in the planning phase.** No application source code has been implemented yet. The sections below describe the intended goals and direction.

---

## About

ChatPOC is a proof-of-concept project exploring real-time messaging capabilities using WebSockets. The goal is to build a lightweight, functional chat application that demonstrates core real-time communication patterns including instant messaging, presence detection, room-based conversations, and typing indicators.

This project serves as a learning tool and foundation for understanding how real-time web applications work under the hood.

---

## Planned Features

- Real-time messaging via WebSockets (with HTTP long-polling fallback)
- Room-based chat (create, join, and leave chat rooms)
- User presence indicators (online/offline status)
- Typing indicators
- Message history within a session
- Read receipts
- Responsive UI for desktop and mobile browsers

---

## Tech Stack

- **Runtime:** Node.js (v18+)
- **Framework:** Express.js
- **Real-time:** Socket.IO
- **Frontend:** Vanilla HTML / CSS / JavaScript
- **Storage:** In-memory (database integration planned for later)

---

## Roadmap

1. **Foundation** - Project scaffolding, Express server, basic HTML/CSS interface
2. **Real-time Core** - Socket.IO integration, basic message send/receive, user nicknames
3. **Chat Rooms** - Room creation, join/leave, room-scoped messaging
4. **Persistence and Features** - Message history, typing indicators, presence, read receipts
5. **Polish** - Responsive UI, error handling, reconnection logic, tests, deployment guide

---

## Contributing

Contributions are welcome! This project is in its early stages, so there are many opportunities to help shape its direction.

1. Fork the repository
2. Create a feature branch from `master`
3. Commit your changes using conventional commit messages
4. Push your branch and open a Pull Request against `master`

---

## License

This project is licensed under the [MIT License](LICENSE).
