# How to put this on GitHub (private repo)

Follow these once. Commands assume you have **git** installed and a **GitHub account**.

## A. Create the private repository on GitHub

1. Go to **https://github.com/new**
2. **Repository name:** `aigreenbots-sensor-fusion` (or your choice)
3. **Visibility:** select **Private** 🔒
4. Do **NOT** tick "Add a README" (this folder already has one).
5. Click **Create repository**. Keep the page open — you'll need the URL, e.g.
   `https://github.com/<your-username>/aigreenbots-sensor-fusion.git`

## B. Push this folder

Open a terminal **inside this folder** and run:

```bash
git init
git add .
git commit -m "Initial commit: base paper, beated results, satellite integration, poster"
git branch -M main
git remote add origin https://github.com/<your-username>/aigreenbots-sensor-fusion.git
git push -u origin main
```

If GitHub asks for a password, use a **Personal Access Token** (Settings → Developer settings → Personal access tokens), not your account password.

## C. Add collaborators (optional)

On GitHub: **repo → Settings → Collaborators → Add people** (e.g. your supervisors).

## D. Day-to-day updates

After you add code/results later:

```bash
git add .
git commit -m "Add feature-engineering scripts and results"
git push
```

---

## Notes

- **Big data stays out.** The `.gitignore` already blocks rasters, archives, and model files. Commit code, configs, small results, and figures — link to large datasets instead.
- **Base-paper data:** don't re-host it if it's not yours to share — cite the source in `01-base-paper/`.
- **Folder order:** the `01-`, `02-`, `03-` prefixes keep the stages in reading order on GitHub.
