# CakeMail

A local email composer built with **Wails + React + Lexical**. Write and send emails from your desktop — requests are forwarded to your private API server securely over SSH.

> Built to learn — Wails, Lexical rich text editing, SSH tunneling, and Go/React integration.



## Stack

| Layer | Tech |
|-------|------|
| Desktop shell | [Wails v2](https://wails.io) |
| Editor | React + [Lexical](https://lexical.dev) |
| Backend | Go |
| Transport | SSH tunnel → your remote API |



## How it works

```
Wails desktop app
      ↓  direct Go binding (no HTTP)
Go backend
      ↓  SSH tunnel
Your remote API server
      ↓
AWS SES
```

React calls Go functions directly via Wails bindings — no ports, no CORS, no fetch.



## Development setup

### Prerequisites

- Go 1.22+
- Node.js 18+ and pnpm
- Wails CLI
- A Linux/macOS system (or WSL on Windows)

### Install Wails

```bash
go install github.com/wailsapp/wails/v2/cmd/wails@latest
wails doctor   # checks all dependencies
```

### Clone and install

```bash
git clone https://github.com/yourusername/cakemail
cd cakemail
pnpm install --prefix frontend
go mod tidy
```

### Run

```bash
wails dev
```

Opens the desktop app with hot reload.

### Build

```bash
wails build
```

Outputs a single native binary — no runtime dependencies.



## Project structure

```
cakemail/
├── frontend/        ← React + Lexical editor
│   └── src/
│       ├── components/
│       └── hooks/
├── internal/
│   └── ssh/         ← SSH tunnel to remote API
├── app.go           ← Go functions exposed to React
└── main.go
```

---

## Author

Suraj — learning by building real tools.
