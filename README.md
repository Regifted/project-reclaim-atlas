# Project Reclaim | Dr. Atlas 2.0

A React/Vite personal wellness dashboard with responsive graphite/gold UI, guided reflection, journaling, mental and physical wellness routines, mood/sleep charts, life timeline, medication discussion notes and JSON backup.

## Run locally
```bash
npm install
npm run dev
```

## Vercel
Import `Regifted/project-reclaim-atlas` and select **Vite**. The root is the repository root. Build command `npm run build`, output directory `dist`. Pushes to `main` should trigger a build if Git integration is active.

## Optional live AI
Set `OPENAI_API_KEY` as a **server-side Vercel environment variable**, never in `VITE_*` or in the browser. Optional `OPENAI_MODEL` defaults to `gpt-4.1-mini`. The `/api/atlas` serverless route sends the selected conversation messages to OpenAI. It does **not** transmit journal entries, check-ins, or personal history automatically. Without a key, use Structured Guidance mode.

## Important privacy limitations
The current release uses browser localStorage and does not provide encrypted cloud storage, user authentication, cross-device sync, or clinician-grade medical record protections. It is **not appropriate for sensitive medical records on shared devices**. Export backups deliberately and protect exported files. Data from the earlier browser-local v1 version migrates automatically on the same browser origin when available. A change of domain or browser requires a manual export/import. Live AI sends chat content to an external provider, so avoid entering identifying medical information.

The mentor is fictional and educational, not a licensed therapist or prescriber. It does not diagnose or recommend medication changes.

## Next production milestones
- User authentication and row-level database authorization
- Encryption strategy, access controls, backups, retention/deletion controls
- Explicit consent and privacy disclosure for AI processing
- Rate limiting and abuse protection on the AI endpoint
- Automated tests, accessibility audit, mobile QA
