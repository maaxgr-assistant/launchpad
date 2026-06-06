# Launchpad

A minimal homelab dashboard — a static HTML page served via nginx that displays cards linking to self-hosted services.

## Stack

- **Frontend**: Single `index.html` (vanilla HTML/CSS/JS, no build step)
- **Server**: nginx:alpine via Docker Compose, exposed on port `8080`

## Running

```bash
docker compose up -d
```

Open [http://localhost:8080](http://localhost:8080).

## Adding a service

Edit the `services` array in `index.html`:

```js
{
  name: "My Service",
  url: "http://192.168.1.10:3000/",
  favicon: "http://192.168.1.10:3000/favicon.ico",
  accent: "#FF5733",
  letter: "M",   // fallback letter if favicon fails to load
}
```
