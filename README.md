# InzoDutch

This project includes a frontend roadmap and a simple Node/Express backend with persistent progress storage.

## Run locally

1. Install dependencies:
   ```bash
   npm install
   ```
2. Start the server:
   ```bash
   npm start
   ```
3. Open `http://localhost:3000` in your browser.

## How it works

- `dutchapp.html` is served by `server.js`.
- Progress is saved to a SQLite database file at `data.db`.
- Each browser gets a stored `userId` in `localStorage` and syncs progress to the backend.
- Create a sync account to share progress across devices using a generated account code.

## Deploying with persistence

For persistent storage over sessions, deploy to a service that provides a writable disk or external DB.

Recommended options:
- Render Web Service
- Railway Web Service
- A VPS / Docker host

When deploying, use `npm start` as the start command.

> Note: Serverless hosts like Vercel Functions typically do not preserve file-based SQLite data across deployments. Use a full web service instead.
