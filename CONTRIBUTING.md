---
output:
  pdf_document: default
  html_document: default
---
# Contributing to PRZB

Thanks for helping out! Changes are made through a **fork and pull request** (PR).
For larger changes, please open an [issue](https://github.com/{{OWNER}}/{{REPO}}/issues) first.
In the commands below, replace `YOU` with your GitHub username.

## 1. Fork and clone (once)

```bash
gh repo fork rmonajemi/przb --clone --remote
cd przb
```

Without the GitHub CLI: click **Fork** on GitHub, clone `RM-LUMC/przb`, then
`git remote add upstream https://github.com/rmonajemi/przb.git`.

## 2. Make your change on a new branch

```bash
git switch main
git pull upstream main
git switch -c fix/short-description
# edit, then:
git add <files>
git commit -m "fix: short description"
git push -u origin fix/short-description
```

One branch per change; never work on `main`.

## 3. Open a pull request

On GitHub, click **Compare & pull request** and check that the base is **`rmonajemi/przb`, `main`**.
Describe what you changed and why, then click **Create pull request**.
To process review comments, push new commits to the same branch; the PR updates automatically.

## 4. After the merge

PRs are merged with **Squash and merge**. Then update your fork and remove the branch:

```bash
git switch main
git pull upstream main
git push origin main
git branch -D fix/short-description
git push origin --delete fix/short-description
```

Questions? Open an issue or ask in your PR.
