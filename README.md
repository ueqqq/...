# Pinar Press

Cuban newspaper project — editor + public site + Discord bot.

## Folder structure

```
pinar-press-complete/
├── public/
│   └── index.html          ← NEW polished public site (use this as the face of the paper)
├── original/
│   └── pinar_press_site.html  ← Full editor + old site (newspaper designer)
├── bot/
│   ├── index.js
│   ├── package.json
│   └── env.example
└── README.md
```

## How to use

### 1. Public site (recommended face of the project)
- Open `public/index.html` in any browser.
- It is a single self-contained file. No server needed.
- It reads posts from the same browser storage as the original editor (`pp_posts`, `pp_staff`, etc.).
- Looks cleaner, more atmospheric, and more intentional than the previous public view.

### 2. Newspaper editor (create front pages)
- Open `original/pinar_press_site.html`.
- This is the full designer: layouts, Cuban themes, image upload, PNG export, Discord pack, library, etc.
- Use the “Website” button inside it to switch to the site view, or just use the new `public/index.html` instead.

### 3. Discord bot
```bash
cd bot
cp env.example .env
# edit .env with your real tokens and IDs
npm install
npm start
```

Commands:
- `/noticia` — staff publish a news post
- `/contratar` — application form with Accept/Reject buttons

## Recommended workflow

1. Design front pages with the original editor.
2. Publish stories so they appear on the new public site.
3. Host `public/index.html` anywhere (Netlify, Cloudflare Pages, GitHub Pages, etc.) when you want a real public URL.
4. Run the Discord bot on a cheap VPS or Railway/Render if you want the slash commands live.

## Next improvements (if you want them later)
- Better image handling and real photos
- Multi-page newspaper
- Light backend so posts are shared across devices
- Tighter link between the Discord bot and the site
