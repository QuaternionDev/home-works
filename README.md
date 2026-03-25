# Home · Works

A homework management web app for classroom use. Students submit homework tickets, admins approve them, and approved assignments appear on a shared timetable sorted by due date. Built with vanilla HTML/CSS/JS — no build step, no framework, just a single HTML file.

> **Note:** The app is currently in demo/preview state. All features are fully functional in the UI, but there is no backend integration yet — data is not persisted anywhere. Backend support (Appwrite) is planned for a future release.

## How it works

1. Students log in with their class account and submit a homework ticket — subject, due date, time, and a description
2. The ticket lands in the admin panel as **pending**
3. The admin (teacher) reviews and either approves or rejects it
4. Approved tickets appear on the shared **Timetable** screen, sorted by due date, visible to everyone in the class
5. Students can filter their own submissions by status (pending / approved / rejected) and delete their own tickets

## Features

- 🔐 Username/password authentication (UI only — no backend yet)
- 📋 Ticket list with `pending`, `approved`, and `rejected` states
- 📅 Shared timetable view — approved homework sorted by due date
- ⚙️ Admin panel — approve, reject, or delete any ticket
- 🌍 Hungarian, English, and German language support
- 📱 Mobile-friendly with a bottom navigation bar
- 👁 Preview mode — explore the full UI with sample data, no account needed

## Project structure

```
home-works/
└── index.html    # Full frontend — single self-contained file
```

---

## Trying it out

Since the app is currently demo-only, the easiest way to explore it is through **Preview mode** — just open `index.html` in a browser and click the preview button on the login screen. You'll get the full UI with sample homework data, including admin access, without needing any account or backend.

To host it as a static page (for sharing or testing on mobile), any static file host works — just upload `index.html`:

- **Netlify** — drag and drop the file at [netlify.com](https://netlify.com)
- **GitHub Pages** — push to a repo, enable Pages under Settings
- **Vercel** — import the repo at [vercel.com](https://vercel.com)
- **Replit** — create a new HTML/CSS/JS repl and replace the default `index.html`

---

## Customisation

A few things you might want to tweak:

- **Subject list** — the dropdown in the upload modal is hardcoded. Edit the `<option>` tags inside `#uf-subject` to match your class's actual subjects.
- **School name / class code** — change the `eyebrow` string in each language in the `STRINGS` object at the top of the script.
- **Default language** — the app defaults to Hungarian (`hu`). Change `localStorage.getItem('lang') || 'hu'` to `'en'` or `'de'` if needed.

---

## Planned

- [ ] Appwrite backend integration (auth, database, persistence)
- [ ] Per-user ticket ownership and delete permissions
- [ ] Scheduled or real-time state sync across classmates

---

## Disclaimer

This project was built with the assistance of Claude by Anthropic. The code, documentation, and design were generated and iterated through a conversational development process. Most of this repo is vibe-coded.

---

## License

MIT
