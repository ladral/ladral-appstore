# Ente Locker
Ente Locker is a privacy-focused password manager that uses end-to-end encryption to keep your credentials, secure notes, and sensitive data secure. It connects to Ente Museum (the core backend server) to store and manage your encrypted vault.

---

## What’s Included

- **Locker App** - The client web application for storing, viewing, and managing passwords, secure notes, and other sensitive data

---

## Features

- **End-to-End Encrypted**: Only you can access your passwords and sensitive data
- **Secure Storage**: Store passwords, credit cards, secure notes, and more
- **Autofill**: Seamless autofill for browsers and apps
- **Cross-Platform**: Access your vault from any device
- **Password Generator**: Create strong, unique passwords
- **Secure Sharing**: Share encrypted entries with others

---

## How It Works

This app deploys Ente Web as a Runtipi app. Ente Web serves different web apps on different ports. This deployment only exposes the relevant ports and paths for Ente Locker.

- Users access Locker through web or mobile clients
- All data is encrypted on-device before being uploaded to Museum's object storage
- Locker shares the same user database as other Ente apps via Museum
- Requires Ente Museum to be installed and running first

---

## Links

- [Ente Locker](https://ente.com/locker/)
- [Ente](https://ente.com)
- [GitHub](https://github.com/ente/ente)
- [Ente Web releases](https://github.com/ente/ente/pkgs/container/web)

Note: This is a client application. It requires Ente Museum to be deployed as a separate Runtipi app to function. Users will authenticate through Museum and all data will be stored in Museum's object storage.
