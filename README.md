# Minastic family site

Static site for the Minastic apps (Run, Lift, Ride): `/`, `/privacy/`, `/terms/`, `/ai/`, `/delete/` and `404.html`.
Plain HTML and one CSS file (`assets/style.css`). No build step, no JavaScript, no cookies, no trackers. No outside requests:
Archivo (SIL OFL 1.1) is served from `assets/fonts/`.

Replaces Run's older site `https://trools.github.io/stamina-site/` (its pages redirect here).

## Publish (GitHub Pages)

1. Create a public repo named `minastic-site` under the `Trools` account (no README, no licence, so the first push is clean).
2. From this folder: `git remote add origin https://github.com/Trools/minastic-site.git` then `git push -u origin main`.
3. In the repo: Settings, Pages, Build and deployment: Source "Deploy from a branch", Branch `main`, folder `/ (root)`, Save.
4. After a minute the site is at `https://trools.github.io/minastic-site/`. Check all four pages and a wrong address (the 404 page).
5. Then push the redirect branch in the `stamina-site` repo (`redirect-to-minastic`), merge it into `main`, so the old links forward here.

## Notes

- `404.html` uses absolute paths starting with `/minastic-site/`. If the site later moves to its own domain at the root, change those paths.
- Every page uses relative links, so the site works under any folder name except for `404.html`.
- Logos in `assets/logo/` are copied unchanged from the Minastic logo kit (`RunningCoach/docs/design/logo/final/`). Never redraw them.
- Legal texts are AI-drafted and not reviewed by a lawyer. Run's section is Run's privacy notice v0.2 (4 October 2026). When
  Run's rewritten notice ships, replace Run's section, the terms' version line and the dates.
- Contact address: the one the old site already published.
