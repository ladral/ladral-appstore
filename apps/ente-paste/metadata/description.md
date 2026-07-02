# Ente Paste

Ente Paste is a privacy-focused pastebin service that uses end-to-end encryption to securely share text snippets, code, and other content. It connects to Ente Museum (the core backend server) to store and manage your encrypted paste data.

---

## What's Included

- **Paste App** - The client web application for creating, viewing, and managing encrypted pastes

---

## Features

- **End-to-End Encrypted**: Only you and your intended recipients can access your pastes
- **Self-Destructing Pastes**: Pastes are automatically deleted after first view or after expiration time exceeds
- **Password Protected**: Set a password to protect your pastes
- **Secure Sharing**: Share encrypted pastes with others

---

## How It Works

This app deploys Ente Web as a Runtipi app. Ente Web serves different web apps on different ports. This deployment only exposes the relevant ports for Ente Paste.

- Users create and access pastes through web
- All paste content is encrypted
- Requires Ente Museum to be installed and running first

---

## Links

- [Ente Paste](https://paste.ente.com/)
- [Ente](https://ente.com)
- [GitHub](https://github.com/ente/ente)
- [Ente Web releases](https://github.com/ente/ente/pkgs/container/web)

Note: This is a client application. It requires Ente Museum to be deployed as a separate Runtipi app to function.