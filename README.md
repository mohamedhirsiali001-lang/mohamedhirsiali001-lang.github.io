# Portfolio

Static site built with Astro, deployed to GitHub Pages by GitHub Actions.

## First-time setup
1. Create a **public** repo named `YOUR-USERNAME.github.io` and upload these files.
2. In the repo: Settings > Pages > Source: **GitHub Actions**.
3. Edit `astro.config.mjs` (your username) and the files in `src/data/`.
4. Commit to `main`. The "Deploy" run appears under the Actions tab; the site goes live when it turns green.

## Update content (no code needed)
| To change | Edit |
|---|---|
| Name, headline, about text | `src/data/profile.json` |
| Links and email | `src/data/social.json` |
| Resume content | `src/data/resume.json` |
| Resume PDF | upload to `public/resume/` named `resume.pdf` |
| Skills | `src/data/skills.json` (statuses: Learning, Practiced, Demonstrated) |
| Learning timeline | `src/data/timeline.json` |
| New project | copy `project-template.md` to `src/content/projects/my-project.md`, set `draft: false` |
| Screenshots | upload to `public/images/projects/` |

**On GitHub:** open a file, click the pencil, edit, Commit. Use Add file > Upload files for images and PDFs.
**On your computer:** install Node 20+, then `npm install` and `npm run dev` to preview at localhost:4321. Push to publish.

## Troubleshooting
- Red X in Actions: open the run and read the error; it is usually a typo in JSON (missing comma/quote) or project front matter.
- Page 404 or unstyled: check `site`/`base` in `astro.config.mjs`.
- Project missing: check `draft: false`.
