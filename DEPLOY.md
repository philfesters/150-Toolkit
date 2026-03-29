# 🚀 DEPLOY.md — Push Guide for philfesters

> Complete guide to getting everything onto GitHub from Termux

---

## ⚡ Quick Deploy (One-Shot)

```bash
# From Termux — run this ONCE to set up git credentials
git config --global user.name "philfesters"
git config --global user.email "your@email.com"
git config --global init.defaultBranch main

# Then for each repo:
cd /sdcard/Download/fezzy_github_package
git init
git remote add origin https://github.com/philfesters/fezzy-station.git
git add .
git commit -m "🐾 Fezzy Station V57 — Bojack Security — SOI Brand"
git push -u origin main
```

---

## 📦 What to Push Where

### Repo 1: `philfesters/philfesters` (Profile README)
Files to push:
```
README.md       ← Auto-displays on your GitHub profile page
```

```bash
mkdir ~/philfesters_readme
cp README.md ~/philfesters_readme/
cd ~/philfesters_readme
git init
git remote add origin https://github.com/philfesters/philfesters.git
git add README.md
git commit -m "✦ Profile README — Bojack Fezzy 999 SOI"
git push -u origin main
```

---

### Repo 2: `philfesters/fezzy-station`
Files to push:
```
fezzy_station.sh    ← Main bash script
index.html          ← GitHub profile page
DEPLOY.md
INSTALL.md
BUILDS.md
README.md
```

---

### Repo 3: `philfesters/bojack-security`
Files to push:
```
.bashrc (copy as bashrc_v10.sh)
TOOLS_INDEX.md
HOW-TO.md
PHILOSOPHY.md
```

---

### Repo 4: `philfesters/termux-security-tools`
Files to push:
```
TOOLS_INDEX.md      ← 150+ tools
INSTALL.md
README.md
```

---

## 🔑 GitHub Token Auth (Termux)

GitHub no longer accepts passwords. Use a Personal Access Token:

1. Go to: GitHub → Settings → Developer Settings → Personal Access Tokens → Tokens (classic)
2. Generate new token — check: `repo`, `workflow`, `read:org`
3. Copy the token (shown once!)
4. When `git push` asks for password → paste the token

**Save token in Termux:**
```bash
git config --global credential.helper store
# Next push will save it permanently
```

---

## 📋 Full Deploy Sequence from Termux

```bash
# STEP 1: Install git if needed
pkg install git -y

# STEP 2: Configure
git config --global user.name "philfesters"
git config --global user.email "your@email.com"

# STEP 3: Navigate to your files
cd /sdcard/Download/fezzy_github_package

# STEP 4: Init, add, push
git init
git add .
git status  # Check what's being added
git commit -m "🐾 Bojack Fezzy 999 — Full package V1"
git branch -M main
git remote add origin https://github.com/philfesters/REPO_NAME.git
git push -u origin main

# STEP 5: Verify
# Open browser → github.com/philfesters → check repo
```

---

## 🔄 Update Existing Repo

```bash
cd ~/your_repo_folder
git add .
git commit -m "Update: describe what changed"
git push
```

---

## ❌ Common Errors

| Error | Fix |
|-------|-----|
| `remote: Repository not found` | Create the repo on GitHub.com first |
| `Authentication failed` | Use token not password |
| `Updates were rejected` | `git pull --rebase` then push |
| `fatal: not a git repository` | Run `git init` first |
| `Permission denied` | Check token has `repo` scope |

---

## 🐾 Bojack's Deploy Checklist

- [ ] Repo created on GitHub.com
- [ ] `git init` done
- [ ] `git remote add origin` done
- [ ] Token saved (not password)
- [ ] `git add .` run
- [ ] `git commit -m "..."` done
- [ ] `git push -u origin main` done
- [ ] Checked github.com/philfesters to confirm

*Strategy Over Impulse. Push clean. 999.*
