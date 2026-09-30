# FindIt — Lost & Found Management System (Frontend Prototype)

Frontend-only prototype built for **Development Activity 1** of the Secure
Software Development semester project. Plain HTML/CSS/JavaScript, no build
step and no dependencies — this is a single static page.

## Pages

The prototype is a single `index.html` with three connected views, switched
by JavaScript and tracked in the URL hash so each one is linkable:

- `#home` — Home / landing page
- `#login` — Login / user entry page
- `#dashboard` — Report Lost Item + Browse Found Items (core page, Owner role)

## JavaScript interactions

- Show/hide password toggle (login)
- Form validation with inline error messages (login + report form)
- Live search and category filter over found items
- Character counter on the item description field
- Dynamic "My Reports" list with add/remove (cancel report) and a
  temporary confirmation banner

## Run locally

No build tools needed. Either:

```bash
# just open it
open index.html      # macOS
start index.html      # Windows
```

or serve it so relative paths behave exactly like production:

```bash
npx serve .
# or
python3 -m http.server 5500
```

## Deploy

Through vercel.
### Vercel

1. Go to https://vercel.com/new and import the GitHub repo.
2. Framework preset: **Other** (static site) — Vercel will detect
   `index.html` at the project root automatically.
3. Leave Build Command and Output Directory blank (there is nothing to
   build).
4. Click **Deploy**. Vercel gives you a public `*.vercel.app` URL — that's
   the link to submit for the activity.

Alternatively, with the Vercel CLI:

```bash
npm i -g vercel
vercel
```

## Notes

- Backend, database and real authentication are **not** implemented yet —
  this activity only covers the frontend. Security controls referenced in
  the UI (role separation, minimal data collection, masked passwords) will
  be enforced server-side later in the semester once the backend exists.
- Built by Hashim Shahid & Abdul Wahab.
