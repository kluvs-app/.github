<p align="center"><img src="kluvs-banner.png"/></p>

# Kluvs

**Kluvs** is a multi-server Discord book club platform: manage reading sessions, track members, schedule discussions, and engage with AI-powered features through its proprietary Discord bot.

- Website: [kluvs.com](https://kluvs.com)
- API Reference: [docs.kluvs.com](https://docs.kluvs.com)

---

## Repositories

| Repo | Description | Stack |
|------|-------------|-------|
| [kluvs-mobile](https://github.com/kluvs-app/kluvs-mobile) | Native Android & iOS app | Kotlin Multiplatform, Compose |
| [kluvs-frontend](https://github.com/kluvs-app/kluvs-frontend) | Web dashboard | React 19, TypeScript, Vite, Tailwind |
| [kluvs-bot](https://github.com/kluvs-app/kluvs-bot) | Discord bot | Python, discord.py |
| [kluvs-backend](https://github.com/kluvs-app/kluvs-backend) | REST API | Deno, Supabase Edge Functions |
| [kluvs-api](https://github.com/kluvs-app/kluvs-api) | Public API contract | OpenAPI 3.0 |
| [kluvs-brain](https://github.com/kluvs-app/kluvs-brain) | AI tutoring engine | Python, RAG, LLMs |

---

## Architecture

```
Discord ────► kluvs-bot
                  │
Web ────────► kluvs-frontend
                  │
Mobile ─────► kluvs-mobile
                  │
                  ▼
              kluvs-backend  (Supabase Edge Functions)
                  │
              PostgreSQL (Supabase)
                  │
              kluvs-brain  (Agentic RAG — Socratic AI)
```

---

## Highlights

- **Cross-platform** — web dashboard, native Android & iOS app, and a Discord bot
- **Multi-server** — one deployment serves unlimited Discord guilds with full data isolation
- **AI-powered** — Quill answers questions Socratically using a ReAct RAG loop grounded in the book being read
- **Open API** — full OpenAPI 3.0 spec with interactive docs at [docs.kluvs.com](https://docs.kluvs.com)
