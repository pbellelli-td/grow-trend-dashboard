# GROW+ Weekly Trend Dashboard

Static dashboard for the International CSAM team's GROW+ call scores.

- **Data source:** Supabase project `ritual-dashboard` (ref `yhvjxbjpbjfofpbingop`), table `grow_calls`
- **Hosting:** Netlify (static site, no build step — plain `index.html`)
- **Update model:** This site is never redeployed for data updates. It queries Supabase live on every page load. Weekly updates only write new rows to `grow_calls` (via the Cowork scheduled task) — the deployed site itself doesn't change.
- Uses the Supabase **publishable/anon key**, scoped by RLS policies to the `grow_calls` table only.

## Deploy
1. Push this repo to GitHub.
2. Netlify → Add new site → Import from Git → select this repo.
3. Build command: none. Publish directory: `/` (root).
4. Deploy. Done — permanent, no redeploys needed for weekly data updates.

## Local preview
Just open `index.html` in a browser — no build step required.
