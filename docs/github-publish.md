# Publishing to GitHub

Run these commands **on your machine** (outside restricted sandboxes) from the repository root.

## New repository with GitHub CLI

```bash
cd /path/to/better-frontend-skills
git init -b main
git add -A
git commit -m "Initial commit: accessibility-audit skill and docs"
gh repo create better-frontend-skills --public --source=. --remote=origin --push
```

Use `--private` instead of `--public` if you prefer.

## New repository from the GitHub website

1. Create an empty repo named `better-frontend-skills` (no README, no `.gitignore`).
2. Then:

```bash
cd /path/to/better-frontend-skills
git init -b main
git add -A
git commit -m "Initial commit: accessibility-audit skill and docs"
git remote add origin https://github.com/<YOUR_NAMESPACE>/better-frontend-skills.git
git push -u origin main
```

After publishing, replace `<YOUR_USER_OR_ORG>` in the root [README.md](../README.md) clone URL with your real GitHub namespace (optional cleanup).
