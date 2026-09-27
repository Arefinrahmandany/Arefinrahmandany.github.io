# Md Arefin Rahman — Profile website

Live website: https://arefinrahmandany.github.io/
Repository: https://github.com/Arefinrahmandany/Arefinrahmandany.github.io

This is a static GitHub Pages site. `index.html` is the website entry point. Changes become live after they are committed and pushed to the `main` branch and GitHub Pages finishes deploying.

## First-time setup on Windows

Your current folder is `D:\ontgreen projects\github-profile`. First open **Git Bash** and check whether that folder is already connected to GitHub:

```bash
cd "/d/ontgreen projects/github-profile"
git status
git remote -v
```

If `git status` shows `On branch main` and `git remote -v` shows `https://github.com/Arefinrahmandany/Arefinrahmandany.github.io.git` (or the matching SSH URL), continue to **Daily workflow**.

If it says `not a git repository`, keep your current files safe and make a clone:

1. In Windows File Explorer, rename `D:\ontgreen projects\github-profile` to `github-profile-backup`. Do not delete it.
2. In Git Bash run:

```bash
cd "/d/ontgreen projects"
git clone https://github.com/Arefinrahmandany/Arefinrahmandany.github.io.git github-profile
cd github-profile
git status
git remote -v
```

3. The cloned `index.html` is the published version. If your backup has edits you want to keep, compare the files and copy your intended changes into the cloned `index.html`. Copy this README into the cloned folder too. Keep `index.html` at the repository root.

## Daily workflow

Open Git Bash:

```bash
cd "/d/ontgreen projects/github-profile"
git status
git pull origin main
```

Edit and save `index.html` in VS Code. Preview the file in your browser. Then publish:

```bash
git diff -- index.html
git status
git add index.html README.md
git commit -m "Update profile page"
git push origin main
```

If there are no changes, `git commit` will say `nothing to commit`; that is normal. After pushing, check https://arefinrahmandany.github.io/ and refresh after deployment completes. You can also check the repository's **Actions** tab or **Settings → Pages**.

## Editing from another computer

On that computer, clone once using `git clone`. Before each editing session run `git pull origin main`; after editing, commit and push. On your original computer, run `git pull origin main` before making more changes.

## Useful commands

| Command | Purpose |
| --- | --- |
| `git status` | See current branch and changed files |
| `git remote -v` | Confirm the connected GitHub repository |
| `git pull origin main` | Download and merge new changes |
| `git diff` | Review uncommitted edits |
| `git add index.html README.md` | Stage only these files |
| `git commit -m "Describe change"` | Save a revision locally |
| `git push origin main` | Send revisions to GitHub and trigger deployment |
| `git log --oneline -5` | View five recent commits |

If `git pull` reports local changes would be overwritten, do not force it. Commit your current edits first, then pull. If it reports a merge conflict, open the marked file, resolve the conflict, then stage and commit it. Do not use `git push --force` for normal updates.
