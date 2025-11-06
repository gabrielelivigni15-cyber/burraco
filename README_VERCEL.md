# Burraco Tournament (Vercel + Supabase)

**Stack**: Vite + React + TypeScript + shadcn/ui + Supabase (optional)

## Deploy with Vercel + GitHub

1. Push `workspace/shadcn-ui` to a GitHub repo.
2. Import the repo in Vercel (New Project) and select the folder root.
3. Set **Build Command**: `pnpm build` (or `npm run build`) and **Output Directory**: `dist`.
4. Add Environment Variables:
   - `VITE_SUPABASE_URL`
   - `VITE_SUPABASE_ANON_KEY`
5. Deploy.

## Local dev

```bash
pnpm i
pnpm dev
```

## Supabase schema (SQL)

```sql
create table if not exists participants (
  id uuid primary key default gen_random_uuid(),
  name text not null,
  phone text,
  isPresent boolean default true,
  created_at timestamptz default now()
);

create table if not exists draws (
  id uuid primary key,
  participant jsonb not null,
  prizeType text not null,
  drawnAt timestamptz default now()
);
```
App falls back to localStorage if env vars are missing.
