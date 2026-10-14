# Kanika & Abhishek – Celebration Invitation

A static, single-page wedding celebration invitation (HTML + images + music). No build step, no dependencies.

## Contents
| File | Purpose |
|---|---|
| `index.html` | The whole invitation (inline CSS + JS) |
| `*.webp`, `song.mp3` | Illustrations and background music (all referenced by relative path) |
| `404.html` | Redirects stray URLs back to the invitation |
| `robots.txt` + `<meta robots noindex>` | Asks search engines not to list the (private) invite |
| `.nojekyll` | Tells GitHub Pages to serve files as-is |
| `.github/workflows/pages.yml` | Auto-deploys on every push to `main` |

## Deploy (GitHub Actions – recommended)
1. Create a new GitHub repo (e.g. `invite`) and push this folder to the `main` branch:
   ```bash
   git init -b main
   git add . && git commit -m "Initial invitation"
   git remote add origin https://github.com/<you>/<repo>.git
   git push -u origin main
   ```
2. In the repo: **Settings → Pages → Build and deployment → Source: GitHub Actions**.
3. Open the **Actions** tab, wait for "Deploy to GitHub Pages" to finish.
4. Your site is live at `https://<you>.github.io/<repo>/`.

### Alternative (no Actions)
**Settings → Pages → Source: Deploy from a branch → `main` / `(root)`**. You can delete the `.github` folder in that case.

## Personalised guest links
Append the guest's name; it appears on the envelope and as "Dear <name>," and is prefilled in the RSVP WhatsApp message:
```
https://<you>.github.io/<repo>/?to=Sharma%20Family
https://<you>.github.io/<repo>/#Sharma_Family
```
Add `#invite` to skip the envelope.

## Custom domain (optional)
Add a file named `CNAME` containing your domain (e.g. `invite.example.com`), create a DNS CNAME record to `<you>.github.io`, then enable **Enforce HTTPS** in Settings → Pages.

## Notes
- Music starts on the envelope tap (browsers block autoplay without a gesture).
- Fonts load from Google Fonts; the page falls back to system serif/script fonts offline.
- Countdown targets **17 Nov 2026, 6:30 PM IST**.
- Pages sites are public to anyone with the link, even though the page asks search engines not to index it.
- This is a copy of an invitation shared with you by its author; make sure you have their OK to host and edit it.
