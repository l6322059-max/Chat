# Orbit Chat — web + desktop starter

A small, GitHub-ready chat UI starter with a web build and an Electron desktop shell.

## Important Claude account limitation

This project does **not** sign into a Claude account inside a third-party app, read Claude session cookies, reuse browser tokens, or route Claude subscription usage through a custom backend.

Anthropic's current rules distinguish the official Claude Code application from third-party products: third-party developers must not offer Claude.ai login inside their own apps or intermediate Claude subscription credentials. Claude Code itself supports official sign-in for eligible Claude plans. See:

- https://code.claude.com/docs/en/legal-and-compliance
- https://docs.anthropic.com/en/docs/claude-code/getting-started

This starter therefore:
- provides a local chat-interface demo and local conversation history;
- has an **Open Claude** button that opens the official Claude website for sign-in and real conversations;
- does not ask for an API key or pretend that the demo UI is connected to Claude.

## Requirements

- Node.js 20+
- npm

## Web app

```bash
npm install
npm run web
```

Open the local URL printed by Vite.

## Desktop app

```bash
npm install
npm run desktop
```

The Electron window loads the same local web UI. The Open Claude button opens Claude in your default browser, where you can sign in through Anthropic's official flow.

## Build desktop package

```bash
npm run desktop:build
```

## GitHub

Create a repository on GitHub, then upload these files or push this folder:

```bash
git init
git add .
git commit -m "Initial Orbit Chat starter"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/orbit-chat.git
git push -u origin main
```

## Project structure

```text
orbit-chat-starter/
├── web/
│   ├── index.html
│   ├── app.js
│   └── style.css
├── desktop/
│   └── main.cjs
├── package.json
└── README.md
```

## Security notes

- No credentials or session tokens are collected.
- Local demo messages are stored in your browser's local storage.
- Do not paste passwords, login codes, cookies, or private tokens into this project.
- The app is an independent starter and is not affiliated with or endorsed by Anthropic.
