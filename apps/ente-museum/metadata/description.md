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

### Object Storage (Rustfs) setup
- After the first startup, a specific API access key and API secret key must be created in Rustfs Admin Console
- to do so, create a custom app with a reverse proxy of your choice which points to the Rustfs Admin Console of your ente museum instance
- get the admin access key and secret key from your ente muesum Rustfs deployment (docker inspect)
- access the admin console and create a specific access key for your ente instance
- add the access key and secret key to the ente museum app configuration

```yaml
# sample caddy web server reverse proxy for rustfs admin console
x-runtipi:
  schema_version: 2
services:
  caddy:
    image: caddy:2-alpine
    restart: unless-stopped
    command: >
      sh -c "echo '
        :7001 {
          reverse_proxy http://ente-museum_{appstoreName}-caddy-1:9001
        }
      ' > /etc/caddy/Caddyfile && caddy run --config /etc/caddy/Caddyfile
      --adapter caddyfile"
    x-runtipi:
      internal_port: "7001"
      is_main: true
```

- Other Ente apps (e.g. Photos, Locker, Paste) will connect to this instance.
- All apps share the same user database and user base.

---

## Links

- [Ente](https://ente.com)
- [GitHub](https://github.com/ente/ente)
- [Museum releases](https://github.com/ente/ente/pkgs/container/server)
- [Ente CLI](https://ente.com/help/self-hosting/administration/cli)
- [Coraza WAF Images](https://github.com/coreruleset/coraza-crs-docker/pkgs/container/coraza-crs)
---

**Note**: This is a core component. To use Ente's full functionality, you'll also need to deploy the companion Ente apps (e.g., Photos, Locker, etc.) as separate Runtipi apps. Each of these will connect to **Ente Museum** for API.