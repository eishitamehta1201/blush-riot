# Blush Riot

A maximalist pink fashion app — browse a weekly drop, manage your own closet, and check out. Built to demo authentication, CRUD, and a full business flow in one file.

**Live app:** _add your deployed URL here_ https://heroic-dasik-b1c20e.netlify.app
**Video walkthrough:** _add your Loom link here_

## What it does

- **Auth** — sign up, log in, log out. Accounts persist across sessions.
- **Closet (CRUD)** — add, edit, and delete clothing items you own: name, category, color swatch, notes.
- **Shop → Bag → Checkout (core flow)** — browse a 10-item drop, filter by category, add to bag, adjust quantities, check out with shipping details, and see the order land in your order history.

## Test credentials

```
username: demo
password: demo1234
```
Or sign up with any username/password — it's instant, no email verification.

## Stack

- Plain HTML, CSS, and vanilla JavaScript — no framework, no build step.
- Data persistence via the app's built-in key-value storage API (`window.storage`), scoped per user for closet items, bag contents, and order history.
- Built with Claude (Anthropic).

## Run it locally

No install needed — it's a single file.

```bash
git clone https://github.com/mayanknagpal3107/blush-riot.git
cd blush-riot
open index.html   # or just double-click it
```

## Deploy it

Static host of your choice works since there's no backend:

**Vercel**
```bash
npm i -g vercel
vercel --prod
```

**Netlify** — drag `index.html` into [app.netlify.com/drop](https://app.netlify.com/drop)

**GitHub Pages** — in the repo, Settings → Pages → Deploy from branch → `main` / root.

## Known limitations

- Storage is tied to the browsing session's key-value store, not a real database — fine for a demo, not for production scale.
- No password hashing (plaintext demo storage) — would need a real backend + hashed credentials for production use.
- Product catalog is hardcoded; a real version would pull from a database or CMS.
