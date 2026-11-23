<div align="center">

# 🚀 gotodo

**A fast, lightweight, and colorful task manager for people who live in the terminal.**

[![Go](https://img.shields.io/badge/Go-1.21+-00ADD8?style=for-the-badge&logo=go&logoColor=white)](https://go.dev)
[![License: MIT](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)
[![Platform](https://img.shields.io/badge/Platform-Linux%20%7C%20macOS%20%7C%20Windows-lightgrey?style=for-the-badge)](#)
[![golangci-lint](https://img.shields.io/badge/golangci--lint-clean-brightgreen?style=for-the-badge)](https://golangci-lint.run)

Forget the browser and heavy GUIs — `gotodo` keeps your tasks at your fingertips, right from the command line.

</div>

---

## 📖 Table of Contents

- [✨ Features](#-features)
- [📦 Installation](#-installation)
- [🚀 Quick Start](#-quick-start)
- [🛠️ Commands](#️-commands)
- [🎛️ Flags](#️-flags)
- [🗂️ Data Storage](#️-data-storage)
- [🧑‍💻 Development](#-development)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)

---

## ✨ Features

- ⚡ **Blazing fast** — a single Go binary, no dependencies, no background processes.
- 🎨 **Colorful output** — priorities and statuses are highlighted via ANSI codes (`fatih/color`).
- 💾 **Simple storage** — all tasks live in a single JSON file at `~/.gotodo/tasks.json`.
- 🏷️ **Priorities & deadlines** — keep track of what matters with `--priority` and `--due`.
- 🔍 **Smart filtering** — find what you need with `--filter`.
- 🧹 **Full task lifecycle** — from creation to removal and cleanup.

---

## 📦 Installation

```bash
go install github.com/YOUR_USERNAME/gotodo@latest
```

## 🚀 Quick Start

```bash
# Add a task with priority and due date
gotodo add "Write README" --priority high --due 2026-12-01

# List all tasks
gotodo list

# Filter by priority
gotodo list --filter high

# Mark a task as done
gotodo done 1

# Remove a task
gotodo rm 2

# Clear completed tasks
gotodo clear
```

## 🛠️ Commands

| Command  | Description                |
|----------|----------------------------|
| add      | Add a new task             |
| list     | Show the task list         |
| done     | Mark a task as completed   |
| rm       | Remove a task by ID        |
| clear    | Remove all completed tasks |

## 🎛️ Flags

Flag	Type	Description
--priority	string	Task priority: low, medium, high
--due	string	Due date in YYYY-MM-DD format
--filter	string	Filter for list: by priority or status

| Flag       | Type   | Description                            |
|------------|--------|----------------------------------------|
| --priority | string | Task priority: low, medium, high       |
| --due      | string | Due date in YYYY-MM-DD format          |
| --filter   | string | Filter for list: by priority or status |

## 🗂️ Data Storage

All tasks are stored locally at:

text
~/.gotodo/tasks.json
The file is created automatically on first run. No sync, no telemetry — just your tasks.

<details> <summary><strong>Example <code>tasks.json</code></strong></summary>

```json
[
  {
    "id": 1,
    "title": "Write README",
    "priority": "high",
    "due": "2026-12-01",
    "done": false
  },
  {
    "id": 2,
    "title": "Ship v1.0",
    "priority": "medium",
    "due": "2026-12-15",
    "done": true
  }
]
```
</details>

## 🧑‍💻 Development

```bash
# Clone the repo
git clone https://github.com/YOUR_USERNAME/gotodo.git
cd gotodo

# Install dependencies
go mod download

# Build the binary
go build -o gotodo .

# Run the linter
golangci-lint run
```

## Project status **Progress:** ⬜⬜⬜⬜⬜⬜⬜⬜⬜⬜ 0% (🟩|⬜)
- [ ] Core commands (add, list, done, rm, clear)
- [ ]  JSON storage in ~/.gotodo/tasks.json
- [ ]  Colorful terminal output
- [ ]  Flags --priority, --due, --filter
- [ ]  go install support
- [ ]  Clean golangci-lint run

## 📄 License
Distributed under the MIT License. See LICENSE for details.
