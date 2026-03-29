# 📖 HOW-TO.md — Build & Push Termux Projects to GitHub

> Fezzy's complete field manual for working from Android

---

## 🔑 Core Workflow: Termux → GitHub

```
Write/Edit in Termux → Test → Copy to /sdcard → git push
```

That's the entire loop. Everything below is just the details.

---

## 📁 File Structure Best Practices

```bash
~/                          ← Home (Termux)
├── .bashrc                 ← Bojack Security auto-loads here
├── fezzy_station.sh        ← Fezzy Station main script
├── fezzy_cheat.sh          ← Security cheatsheet
├── fezzy_welcome.sh        ← Welcome screen
└── go/bin/                 ← Go-installed tools

/sdcard/Download/           ← Accessible to Files app
├── fezzy_github_package/   ← Files ready to push
│   ├── index.html
│   ├── README.md
│   ├── DEPLOY.md
│   └── ...
```

---

## ✏️ Editing Files in Termux

**Rule:** `nano` for `.bashrc`, `vim` for `.sh` files

```bash
# Edit bashrc (nano — safe, simpler)
nano ~/.bashrc

# Edit shell scripts (vim)
vim ~/fezzy_station.sh

# Save in nano: Ctrl+X → Y → Enter
# Save in vim: Esc → :wq → Enter
```

---

## 🔄 Bash File Versioning System

**CRITICAL RULE:** Always increment version on every bash file. Never overwrite.

```bash
# WRONG — overwrites previous version
cp /sdcard/Download/bashrc.sh ~/.bashrc

# RIGHT — keep version history
cp /sdcard/Download/bashrc_v11.sh ~/bashrc_v11.sh
# Then manually review before sourcing

# Deploy pattern
cp /sdcard/Download/[file] ~/[file] && source ~/.bashrc
```

---

## 🧪 Testing Before Deploy

```bash
# Syntax check ALWAYS before sourcing bashrc changes
bash -n ~/.bashrc && echo "✅ Syntax OK" || echo "❌ Syntax Error"

# Test a script without running it
bash -n ~/fezzy_station.sh

# Test specific function
source ~/.bashrc 2>&1 | head -20
```

---

## 🌐 Git Workflow from Termux

```bash
# First time only: configure git
git config --global user.name "philfesters"
git config --global user.email "your@email.com"
git config --global credential.helper store

# Navigate to your project
cd /sdcard/Download/fezzy_github_package

# Initialize
git init
git branch -M main
git remote add origin https://github.com/philfesters/REPO_NAME.git

# Stage all files
git add .

# Check what's staged
git status

# Commit
git commit -m "🐾 Descriptive commit message here"

# Push (first time use -u)
git push -u origin main

# Subsequent pushes
git push
```

---

## 🔁 Update Existing Repo

```bash
cd /path/to/local/repo
git pull  # Get latest from GitHub first
# ... make changes ...
git add .
git commit -m "Update: what changed and why"
git push
```

---

## 📦 Zipping for Transfer

```bash
# Create zip
cd /sdcard/Download
zip -r fezzy_github_package.zip fezzy_github_package/

# Unzip
unzip fezzy_github_package.zip -d /sdcard/Download/

# Check contents
unzip -l fezzy_github_package.zip
```

---

## 🐍 Python Scripts in Termux

```bash
# Always use --break-system-packages for pip
pip install package_name --break-system-packages

# Run scripts
python3 script.py

# Check installed packages
pip list --break-system-packages | grep package_name
```

---

## 🔒 Security Tool Quick Reference

```bash
# Username OSINT
python3 ~/sherlock/sherlock.py username

# Domain recon
amass enum -d target.com
subfinder -d target.com

# Web fingerprint
whatweb target.com
nikto -h target.com

# Port scan
nmap -sV target.com

# Directory scan
ffuf -w /path/to/wordlist -u http://target.com/FUZZ

# Hash crack
hashcat -m 0 hash.txt wordlist.txt
john hash.txt --wordlist=wordlist.txt
```

---

## ⚡ Alias Cheatsheet

```bash
# Fezzy Station
alias station='bash ~/fezzy_station.sh'
alias dl='bash ~/fezzy_station.sh'

# Git shortcuts (add to .bashrc)
alias gs='git status'
alias ga='git add .'
alias gc='git commit -m'
alias gp='git push'
alias gl='git log --oneline -10'

# Termux utilities
alias cls='clear'
alias brc='nano ~/.bashrc'
alias src='source ~/.bashrc'
alias bashtest='bash -n ~/.bashrc && echo OK'
```

---

## 🐾 Bojack's Rules

1. Never commit a file you haven't read
2. Always `bash -n` before sourcing
3. Version numbers are sacred — never skip
4. If it breaks, it's a learning version
5. Strategy Over Impulse — plan the commit message before typing it

---

*philfesters · Strategy Over Impulse · 999 · Rhrc sNeve e