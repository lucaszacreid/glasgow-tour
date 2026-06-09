# The Grand Glasgow Tour

Private guided tours of Glasgow's finest landmarks in a vintage Mercedes, with Ewen as your personal guide.

A single-page static website built with plain HTML, CSS, and JavaScript. No build step required — open `index.html` in a browser or deploy to Vercel as-is.

---

## First-time deployment

**Step a.** Create a new repository on GitHub:
- Go to github.com → New repository
- Name it something like `glasgow-tour`
- Keep it public or private — your choice
- **Do not** add a README, .gitignore, or licence (they're already here)
- Copy the repository URL (e.g. `https://github.com/YOUR_USERNAME/glasgow-tour.git`)

**Step b.** Connect this folder to your new GitHub repo:
```bash
git remote set-url origin YOUR_GITHUB_REPO_URL
```
> Replace `YOUR_USERNAME` and `glasgow-tour` with your actual GitHub username and repo name.

**Step c.** Push to GitHub:
```bash
git push -u origin main
```

**Step d.** Deploy to Vercel:
- Go to [vercel.com](https://vercel.com) → **New Project**
- Click **Import from GitHub** → select your `glasgow-tour` repo
- Vercel will auto-detect this as a static site — just click **Deploy**

**Step e.** Wait ~30 seconds — your site will be live on a `.vercel.app` URL.

**Step f.** Add your custom domain (optional):
- In the Vercel dashboard → your project → **Settings → Domains**
- Add your domain and follow the DNS instructions

---

## Making changes and redeploying

Every push to `main` automatically triggers a fresh Vercel deployment.

**Step a.** Make your edits in index.html (or any other file)

**Step b.** Stage your changes:
```bash
git add .
```

**Step c.** Commit with a description:
```bash
git commit -m "describe your change here"
```

**Step d.** Push:
```bash
git push
```

**Step e.** Vercel detects the push and redeploys automatically — no further action needed. Watch progress at vercel.com/dashboard.

---

## Swapping placeholder content

Everything below needs to be updated before the site goes live. Each item notes where to find it.

| Placeholder | Where to find it |
|---|---|
| **Hero background photo** | CSS rule `.hero-bg` — change the `background-image` URL |
| **Ewen's portrait photo** | `<img id="ewen-photo">` tag — change the `src` attribute |
| **All Calendly booking links** | Search for `calendly.com/YOURLINK` — 6 occurrences |
| **Calendly inline widget** | Find the large HTML comment block starting `CALENDLY INLINE BOOKING WIDGET` and follow the instructions inside |
| **Pricing — Classic** | Search for `£95` |
| **Pricing — Grand Tour** | Search for `£145` |
| **Pricing — Full Experience** | Search for `£295` |
| **Contact email** | Search for `hello@thegrandglasgowtourtour.co.uk` — 2 occurrences in the footer |
| **GitHub remote URL** | Run: `git remote set-url origin YOUR_GITHUB_REPO_URL` |
| **Page title / meta description** | `<title>` and `<meta name="description">` tags in `<head>` |

---

## Tech stack

- Plain HTML5, CSS3, JavaScript — no framework, no build step
- [Google Fonts](https://fonts.google.com/) — Playfair Display + Inter
- [Leaflet.js](https://leafletjs.com/) — interactive route map (CartoDB Positron tiles)
- [Calendly](https://calendly.com/) — booking links + optional inline embed

---

## Project structure

```
glasgow-tour/
├── index.html      ← entire site (self-contained)
├── vercel.json     ← Vercel deployment config
├── .gitignore
└── README.md
```
