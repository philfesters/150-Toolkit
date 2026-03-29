# ⚙️ INSTALL.md — Termux Setup Guide

> Complete Termux environment setup for Fezzy Station + Bojack Security

---

## 📱 Requirements

- Android 5.0+ (tested on Android 14)
- Termux (F-Droid version — NOT Play Store)
- ~2GB free storage
- Internet connection for installs

---

## 🚀 Fresh Termux Setup (Complete)

```bash
# Step 1: Update packages
pkg update && pkg upgrade -y

# Step 2: Core dependencies
pkg install -y git curl wget python python-pip nodejs \
  ffmpeg ruby golang openssh nano vim bash zsh \
  binutils coreutils diffutils findutils grep \
  tar zip unzip p7zip

# Step 3: Python tools
pip install yt-dlp gallery-dl --break-system-packages
pip install flask requests beautifulsoup4 --break-system-packages

# Step 4: Storage access
termux-setup-storage
# Tap ALLOW when prompted

# Step 5: Verify
yt-dlp --version
gallery-dl --version
python3 --version
git --version
```

---

## 📡 Install Fezzy Station

```bash
# Clone from GitHub
git clone https://github.com/philfesters/fezzy-station ~/fezzy-station

# Copy main script
cp ~/fezzy-station/fezzy_station.sh ~/

# Make executable
chmod +x ~/fezzy_station.sh

# Add alias to bashrc
echo "alias station='bash ~/fezzy_station.sh'" >> ~/.bashrc
echo "alias dl='bash ~/fezzy_station.sh'" >> ~/.bashrc

# Reload
source ~/.bashrc

# Launch
station
```

---

## 🛡️ Install Bojack Security

```bash
# Clone from GitHub
git clone https://github.com/philfesters/bojack-security ~/bojack-security

# Backup existing bashrc
cp ~/.bashrc ~/.bashrc.backup.$(date +%Y%m%d)

# Apply new bashrc (READ IT FIRST before replacing!)
cat ~/bojack-security/bashrc_v10.sh >> ~/.bashrc

# Reload
source ~/.bashrc
```

---

## 🔒 Security Tools Installation

### OSINT Tools
```bash
# Sherlock — username OSINT
git clone https://github.com/sherlock-project/sherlock ~/sherlock
pip install -r ~/sherlock/requirements.txt --break-system-packages
alias sherlock='python3 ~/sherlock/sherlock.py'

# Recon-ng
pkg install recon-ng -y

# Amass
pkg install amass -y

# Nikto
pkg install nikto -y

# Whatweb
pkg install whatweb -y
```

### Go Tools (requires golang)
```bash
pkg install golang -y
export GOPATH=$HOME/go
export PATH=$PATH:$GOPATH/bin

# Subfinder
go install github.com/projectdiscovery/subfinder/v2/cmd/subfinder@latest

# Httpx
go install github.com/projectdiscovery/httpx/cmd/httpx@latest

# Nuclei
go install github.com/projectdiscovery/nuclei/v2/cmd/nuclei@latest

# Ffuf
go install github.com/ffuf/ffuf@latest

# Waybackurls
go install github.com/tomnomnom/waybackurls@latest

# Gau
go install github.com/lc/gau/v2/cmd/gau@latest
```

### Ruby Tools
```bash
pkg install ruby -y

# WPScan
gem install wpscan

# CeWL
gem install cewl
```

### Python Tools
```bash
pip install dirsearch arjun wifite2 --break-system-packages
pip install droopescan slowloris --break-system-packages
```

---

## 📦 Useful Utilities

```bash
# File management
pkg install ncdu ranger tree htop -y

# Network
pkg install nmap netcat-openbsd wget curl -y

# Forensics
pkg install binwalk steghide foremost yara -y
pkg install radare2 gdb binutils -y

# Cracking
pkg install hashcat john crunch -y

# Media
pkg install ffmpeg imagemagick -y
```

---

## 🎨 Terminal Enhancements

```bash
# Colors and fonts
pkg install gum -y  # gum spin and gum style work on Android
pkg install lolcat figlet toilet -y
pkg install neofetch -y

# Shell
pkg install zsh -y
# (optional: oh-my-zsh)
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

---

## ✅ Verify Installation

```bash
# Check core tools
yt-dlp --version       # Should show version
gallery-dl --version   # Should show version
python3 --version      # Should show 3.x
git --version          # Should show git version
sherlock --version     # Should show sherlock info

# Launch Fezzy Station
station

# Check bashrc loads correctly
source ~/.bashrc && echo "Bojack says: Bashrc loaded, 999"
```

---

## 🐾 Bojack's Note

*"Grant installed all of this on a phone. You have a PC and can't get git to work. Think about that."*

*— Bojack, perpetually unimpressed*

---

*Strategy Over Impulse · 999 · philfesters*
