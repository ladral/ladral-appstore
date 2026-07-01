# Ente Photos
Ente Photos is a privacy-focused photo and video storage app that uses end-to-end encryption to keep your memories secure. It connects to Ente Museum (the core backend server) to store and manage your encrypted media files.

---

## What’s Included

- **Photos App** - The client web application for uploading, viewing, and managing photos and videos

---

## Features

- **End-to-End Encrypted**: Only you can access your photos
- **Automatic Backup**: Continuous, battery-efficient photo uploads
- **Album Organization**: Create and manage custom albums
- **Cross-Platform**: Access your photos from any device
- **Selective Sync**: Choose which folders to back up
- **Live Photos & Videos**: Support for all media types
- **Secure Sharing**: Share encrypted albums with others

---

## How It Works

This app deploys Ente Web as a Runtipi app. Ente Web serves different web apps on different ports. This deployment only exposes the relevant ports and paths for Ente Photos.

- Users access Photos through web or mobile clients
- All media is encrypted on-device before being uploaded to Museum's object storage
- Photos shares the same user database as other Ente apps via Museum
- Requires Ente Museum to be installed and running first

---

## Links

. [Ente Photos](https://photos.ente.com/)
- [Ente](https://ente.com)
- [GitHub](https://github.com/ente/ente)
- [Ente Web releases](https://github.com/ente/ente/pkgs/container/web)

Note: This is a client application. It requires Ente Museum to be deployed as a separate Runtipi app to function. Users will authenticate through Museum and all data will be stored in Museum's object storage.
