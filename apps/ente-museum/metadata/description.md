# Ente Museum

Ente Museum is the core backend server for the [Ente](https://ente.com) ecosystem.

It powers all Ente apps - Photos, Locker, Auth, and Paste - with a single, data-agnostic backend. This allows users to use the same credentials to store different types of end-to-end encrypted data without needing to create new accounts.

---

## What’s Included

- **Museum** - The core server for all Ente apps
- **PostgreSQL** - Database for user metadata
- **Object Storage**: Storage for encrypted user data

---

## Features

- **Unified Access**: One account for all Ente apps
- **Data-agnostic**: Works with any type of end-to-end encrypted data
- **Scalable**: Built to support future Ente apps and use cases

---

## How It Works

This app deploys **Ente Museum** as a Runtipi app. This is the core backend server for all Ente apps and must be installed prior to any other Ente app.

- Other Ente apps (e.g. Photos, Locker, Paste) will connect to this instance.
- All apps share the same user database and user base.

---

## Links

- [Ente](https://ente.com)
- [GitHub](https://github.com/ente/ente)
- [Museum releases](https://github.com/ente/ente/pkgs/container/server)
- [Ente CLI](https://ente.com/help/self-hosting/administration/cli)

---

**Note**: This is a core component. To use Ente's full functionality, you'll also need to deploy the companion Ente apps (e.g., Photos, Locker, etc.) as separate Runtipi apps. Each of these will connect to **Ente Museum** for API.