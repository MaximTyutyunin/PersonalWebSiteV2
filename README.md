# Project Architecture Overview  

## Frontend 
- **Framework:** React + TypeScript + Vite → defines components (buttons, pages, etc.)
- **Styling:** Tailwind → styling (colors, spacing, fonts)
- **Hosting:** Vercel (free tier)
  

**Local Commands**
- Run frontend locally: `npm run dev`

## Backend
- **Framework:** FastAPI (Python) → handles requests
- **Database:** Supabase (PostgreSQL) → stores project info, messages, analytics
- **Hosting:** Render / Railway / Fly.io (free tier)
  

**Local Commands**
- Run backend locally: `uvicorn main:app --reload`
  
**Deployment Steps**
1. Deploy frontend → verify it loads
2. Deploy backend → verify endpoints work
3. Connect frontend and backend
  

## AI (v2 Feature)
- **LLM API:** OpenAI API (via backend only)
- **Embeddings:** OpenAI embeddings stored in Supabase (`pgvector`)
 
---

# MVP Features (Must-have for v1)  
- Single-page React/TypeScript app (Home, Projects, About, Contact pages)
- Home/hero section summarizing who you are (60-seconds-read info)
- Projects showcase linking to GitHub
- Downloadable resume (PDF)
- Basic contact form (email only)
- Personal login route (admin-only) using modern auth (Auth0, Clerk, Supabase, or NextAuth)
- Owner/admin panel for:
  - Basic analytics
  - Content editing
  - Maintenance mode toggle
- Light/dark mode toggle for accessibility
- Simple AI chat widget (your own RAG bot)
  - Answers questions about you from CV, About, and Projects data
  - Fallbacks gracefully when unsure

---

# v2+ Features (Add Later)  
- Blog or changelog section  
- Comment/discussion system  
- Advanced analytics dashboard  
- Granular permissions and multi-role admin  
- Expanded RAG system (larger doc sets, live updates, persistent chat entries)  
- Full mobile app or PWA version