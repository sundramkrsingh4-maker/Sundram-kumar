# Sundram

Private Class 10 learning platform for Aarambh and Abhay batches.

## Included
- Mobile-first React/Vite/TypeScript student UI
- Login, batch-aware dashboard, notes/lectures/DPP/question practice UI
- Express/TypeScript API with JWT auth, role middleware, rate limiting, Helmet and backend batch authorization
- Search endpoint filters unauthorized content before returning it
- PWA-ready frontend structure
- Environment template and development seed notes

## Run
1. Install Node.js 20+.
2. `npm install`
3. Copy `.env.example` to `.env` and change `JWT_SECRET`.
4. `npm run dev`
5. Open http://localhost:5173

Demo credentials in this development build:
- student / sundram123
- abhay / sundram123
- admin / sundram123

Change/remove these before any real deployment.

## Important production work
The supplied specification calls for MongoDB/Mongoose persistence, S3-compatible private object storage with short-lived signed URLs, full admin CRUD, persistent practice attempts, AI provider integration, automated security tests, deployment configuration, HTTPS, monitoring and backups. This package includes the security-oriented API skeleton and working UX, but those provider-dependent pieces are deliberately not falsely represented as complete.
