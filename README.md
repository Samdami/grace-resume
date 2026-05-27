Host this site on GitHub Pages

Quick steps

1. Create a repository on GitHub (or use `gh`):

   gh repo create <your-username>/<repo-name> --public --source=. --remote=origin

2. Ensure the default branch is `main` locally:

```bash
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

3. Workflow auto-deploy

A GitHub Actions workflow is included at `.github/workflows/deploy.yml` that will automatically deploy the repository root to GitHub Pages whenever you push to `main`.

Notes

- Make sure `myimage.jpg` (the local hero image) is present in the repo root or update the path in `index.html`.
- Visit the repository's "Actions" tab to watch the Pages deployment. After the first successful run, your site will be available at `https://<your-username>.github.io/<repo-name>/` (or at the custom domain if configured).
- If you prefer to use the `gh` CLI, the `gh repo create` command above will push and set up the remote for you.

Need me to run the git commands and create the GitHub repo for you? If you give me the repo name and confirm you want me to push, I can do that (you'll need to authenticate with GitHub from this machine).
