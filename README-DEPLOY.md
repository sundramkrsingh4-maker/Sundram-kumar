# Sundram — Vercel / Netlify deployment

This repository is prepared so the **student web frontend** can be deployed directly to Vercel or Netlify.

## Option A — Vercel

1. Push this folder to GitHub.
2. In Vercel, import the repository.
3. The root `vercel.json` is already configured.
4. Build command: `npm run build -w frontend`
5. Output directory: `frontend/dist`
6. Deploy.

If the backend is hosted separately, add this environment variable in Vercel:

`VITE_API_BASE_URL=https://YOUR-BACKEND-DOMAIN`

## Option B — Netlify

1. Push this folder to GitHub.
2. In Netlify, choose **Add new site → Import an existing project**.
3. Select the repository.
4. `frontend/netlify.toml` supplies the build settings.
5. Deploy.

For a separately hosted backend, add:

`VITE_API_BASE_URL=https://YOUR-BACKEND-DOMAIN`

## Important architecture note

Vercel/Netlify host the React/Vite frontend. The Express/MongoDB backend should be deployed separately unless the API is migrated to platform-native serverless functions.

The current development backend is an in-memory demonstration and is **not production storage**. For the full Sundram specification, configure MongoDB, secure authentication, private object storage/signed URLs, and the remaining admin/practice services before real student use.

## Local development

From the repository root:

```bash
npm install
npm run dev
```

Frontend: `http://localhost:5173`
Backend: `http://localhost:4000`
