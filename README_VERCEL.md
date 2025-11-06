# Burraco Tournament (Vercel + Supabase)

**Stack:** Vite + React + TypeScript + Supabase + shadcn/ui  

## 🧩 Deploy rapido
1. Carica questo progetto su **GitHub**.
2. Su **Vercel → New Project**:
   - Root directory: *(vuota)*
   - Build Command: `pnpm run build`
   - Output directory: `dist`
3. In **Environment Variables** aggiungi:
   - `VITE_SUPABASE_URL`
   - `VITE_SUPABASE_ANON_KEY`
4. Clicca **Deploy** 🎉

## 🗄️ Tabelle Supabase (SQL)
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
