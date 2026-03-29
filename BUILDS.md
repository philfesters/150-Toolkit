# 🏗️ BUILDS.md — Complete Project History

> Every major build by Bojack Fezzy 999 | philfesters

---

## 📡 Fezzy Station — V1 to V57+

**Type:** Multi-portal Bash media download dashboard  
**Language:** Bash  
**Platform:** Termux / Android  
**Status:** Active — currently V57+

### What it is
A complete media management system running in Bash on Termux. No root. No PC. Launches from a single alias (`station` or `dl`). Features collapsible portals for different media types, multi-platform search, system tools, and web grab utilities.

### Portal Architecture
```
FEZZY STATION
├── 🎥 VIDEO PORTAL
│   ├── YouTube (yt-dlp)
│   ├── Vimeo
│   ├── Dailymotion
│   ├── Rumble
│   ├── Twitch (VODs)
│   └── Facebook Video
│
├── 🎵 MUSIC PORTAL
│   ├── SoundCloud
│   ├── Audiomack
│   ├── Mixcloud
│   └── Spotify (via search)
│
├── 🖼️ GALLERY PORTAL
│   ├── Instagram
│   ├── Reddit
│   ├── Flickr
│   ├── DeviantArt
│   ├── Pixiv
│   ├── Imgur
│   ├── Newgrounds
│   └── ArtStation
│
├── 🐦 SOCIAL PORTAL
│   ├── Twitter/X
│   └── TikTok
│
├── 🌐 WEB GRAB PORTAL
│   └── Direct URL download
│
└── 🛠️ TOOLS PORTAL
    ├── System info
    ├── File manager shortcuts
    └── OSINT shortcuts
```

### Key Milestones
| Version | Major Change |
|---------|-------------|
| V1-V10 | Core concept, basic download menus |
| V11-V20 | Portal system introduced, aliases added |
| V21-V30 | Gallery portal expanded, music portal added |
| V31-V34 | Full audit — color fixes, shortcut alignment |
| V35-V40 | Flask web version built alongside |
| V41-V50 | SOI branding integrated, persona toggles |
| V51-V57 | Bojack K9 Live Widget, Mode Toggle, complete package |

---

## 🛡️ Bojack Security — V1 to V10+

**Type:** OSINT & security dashboard in ~/.bashrc  
**Language:** Bash  
**Platform:** Termux / Android  
**Status:** Active — currently V10+

### What it is
A complete security toolkit embedded into `~/.bashrc`. Auto-loads on every Termux session. Features OSINT portals, exploitation tool menus, forensics, network utilities — all wrapped in a custom Bash framework with Bojack-themed boot sequence.

### Architecture
```
BOJACK SECURITY (~/.bashrc)
├── 🎭 Boot Sequence
│   ├── Bojack ASCII art
│   ├── Rotating 999 quotes
│   └── System status display
│
├── 🔍 OSINT PORTAL
│   ├── Username OSINT (Sherlock)
│   ├── Domain recon (Amass, Subfinder)
│   ├── Web fingerprinting (Whatweb, Nikto)
│   └── URL archive (Waybackurls, Gau)
│
├── 💥 EXPLOITATION PORTAL
│   ├── Web scanning (Nuclei, Dalfox)
│   ├── Brute force (Hydra, Hashcat, John)
│   └── Framework launchers (Metasploit)
│
├── 🔬 FORENSICS PORTAL
│   ├── Binary analysis (Binwalk, Radare2)
│   ├── Steganography (Steghide)
│   └── Memory forensics (Volatility)
│
├── 🌐 NETWORK PORTAL
│   ├── Scanning (Nmap)
│   ├── Traffic (Wireshark/tshark)
│   └── MITM tools
│
├── 🎯 CONTROL HUB
│   └── Master tool menu
│
└── 🧩 MAZE PORTAL
    └── Inventory + cheatsheet
```

### Key Milestones
| Version | Major Change |
|---------|-------------|
| V1-V3 | Basic OSINT menus |
| V4-V6 | Exploitation portal, dual aliases system |
| V7-V8 | Forensics added, boot sequence refined |
| V9 | MAZE inventory, King Phisher, alignment fixes |
| V10 | Full audit, 999 decorative lines, complete polish |

---

## 🌐 SOI Brand — HTML Variants

**Type:** Personal branding web pages  
**Language:** HTML/CSS/JS  
**Status:** 5 variants complete

| Variant | Effect | Theme |
|---------|--------|-------|
| V1 | Matrix rain | Green cascade on black |
| V2 | Typewriter boot | CRT terminal |
| V3 | CRT aesthetics | Scanlines + phosphor |
| V4 | Circuit grid | Tech blueprint |
| V5 | Aurora blobs | Gradient organism |

---

## 🐍 Fezzy Flask — Web App

**Type:** Flask web application  
**Language:** Python 3  
**Status:** Deployed

### Features
- Search API endpoint (`/search`)
- yt-dlp download endpoint (`/download`)
- gallery-dl download endpoint (`/gallery`)
- Live system info panel
- Portal launcher
- Built entirely in Termux on Android

---

## 📄 Document Builds

| Document | Description |
|----------|-------------|
| Life Story PDF | Narrative: man, machines, late nights, Bojack |
| Termux Build History PDF | Full timeline of every project |
| AI Workflow System PDF | Three-AI role map: Claude/ChatGPT/Gemini |
| fezzy_dashboard_V2.html | 2,675-line cyberpunk dashboard, 10 portals |
| Split Personality Dashboard | Admin vs Intoxicated Fezzy toggle |
| Termux 999 Hacks Page | Landing page for Termux tools |
| Bojack Dark Humour Page | Personality meters + incident logs |
| TOOLS_INDEX.md | 150+ OSINT & Exploitation tools |

---

## ⚡ Supporting Scripts

| Script | Purpose |
|--------|---------|
| `fezzy_cheat.sh` | Hacking toolkit cheatsheet V5 |
| `fezzy_welcome.sh` | Welcome screen with rotating quotes |
| `install-all.sh` | Mass tool installer |
| `install-core.sh` | Core tools only installer |

---

*Strategy Over Impulse · 999 · Bojack Fezzy · philfesters*
