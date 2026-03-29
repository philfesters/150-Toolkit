# 🔧 TOOLS_INDEX.md — 150 OSINT & Exploitation Tools

> Bojack Fezzy 999 | philfesters | Strategy Over Impulse
> Full explanations in BOJACK_FEZZY_150_TOOLS.pdf

---

## 🔍 OSINT & RECON (1-50)

| # | Tool | Category | Install |
|---|------|----------|---------|
| 1 | Sherlock | Username OSINT | `git clone + pip` |
| 2 | Recon-ng | OSINT Framework | `pkg install recon-ng` |
| 3 | Amass | DNS Enumeration | `pkg install amass` |
| 4 | Subfinder | Subdomain Discovery | `go install ...subfinder` |
| 5 | Assetfinder | Subdomain Discovery | `go install ...assetfinder` |
| 6 | Httpx | HTTP Probing | `go install ...httpx` |
| 7 | Nuclei | Vuln Scanner | `go install ...nuclei` |
| 8 | Dalfox | XSS Scanner | `go install ...dalfox` |
| 9 | Arjun | Parameter Discovery | `pip install arjun` |
| 10 | Dirsearch | Dir Brute Force | `pip install dirsearch` |
| 11 | Nikto | Web Server Scanner | `pkg install nikto` |
| 12 | Whatweb | Tech Fingerprinting | `pkg install whatweb` |
| 13 | Wapiti | Web Vuln Scanner | `pip install wapiti3` |
| 14 | Ffuf | Web Fuzzer | `go install ...ffuf` |
| 15 | Feroxbuster | Recursive Discovery | `pkg install feroxbuster` |
| 16 | Hakrawler | Web Crawler | `go install ...hakrawler` |
| 17 | Katana | Next-Gen Crawler | `go install ...katana` |
| 18 | Gau | Historical URLs | `go install ...gau` |
| 19 | Waybackurls | Wayback OSINT | `go install ...waybackurls` |
| 20 | Unfurl | URL Analysis | `go install ...unfurl` |
| 21 | CeWL | Wordlist Generator | `gem install cewl` |
| 22 | Photon | OSINT Crawler | `git clone + pip` |
| 23 | EyeWitness | Screenshot Tool | `git clone` |
| 24 | LinkFinder | JS Endpoint Extractor | `git clone + pip` |
| 25 | theHarvester | Email & Domain OSINT | `pip install theHarvester` |
| 26 | Maltego CE | Visual OSINT | Download from maltego.com |
| 27 | SpiderFoot | Automated OSINT | `pip install spiderfoot` |
| 28 | Shodan CLI | Device Search | `pip install shodan` |
| 29 | Nmap | Network Scanner | `pkg install nmap` |
| 30 | Masscan | Fast Port Scanner | `pkg install masscan` |
| 31 | DNSx | DNS Toolkit | `go install ...dnsx` |
| 32 | MassDNS | DNS Resolver | `git clone + make` |
| 33 | Gobuster | Dir & DNS Bruter | `pkg install gobuster` |
| 34 | Wfuzz | Web Fuzzer | `pip install wfuzz` |
| 35 | SQLMap | SQL Injection | `git clone sqlmap` |
| 36 | XSStrike | XSS Suite | `git clone + pip` |
| 37 | Commix | Command Injection | `git clone commix` |
| 38 | Tplmap | SSTI Exploitation | `git clone tplmap` |
| 39 | WPScan | WordPress Scanner | `gem install wpscan` |
| 40 | Droopescan | CMS Scanner | `pip install droopescan` |
| 41 | JoomScan | Joomla Scanner | `git clone OWASP/joomscan` |
| 42 | CMSeeK | CMS Detection | `git clone + pip` |
| 43 | GitDorker | GitHub OSINT | `git clone GitDorker` |
| 44 | TruffleHog | Secret Scanner | `pip install truffleHog` |
| 45 | Gitleaks | Secret Scanner | `go install ...gitleaks` |
| 46 | Censys CLI | Internet Search | `pip install censys` |
| 47 | Holehe | Email OSINT | `pip install holehe` |
| 48 | Maigret | Username OSINT (3000+ sites) | `pip install maigret` |
| 49 | Osintgram | Instagram OSINT | `git clone Osintgram` |
| 50 | Instaloader | Instagram Downloader | `pip install instaloader` |

---

## 💥 EXPLOITATION & NETWORK (51-100)

| # | Tool | Category | Install |
|---|------|----------|---------|
| 51 | Exiftool | Metadata Extraction | `pkg install perl + cpan` |
| 52 | Metagoofil | Document OSINT | `git clone metagoofil` |
| 53 | Wireshark/tshark | Packet Analysis | `pkg install tshark` |
| 54 | Tcpdump | Packet Capture | `pkg install tcpdump` |
| 55 | Volatility 3 | Memory Forensics | `pip install volatility3` |
| 56 | Binwalk | Firmware Analysis | `pkg install binwalk` |
| 57 | Steghide | Steganography | `pkg install steghide` |
| 58 | Foremost | File Carving | `pkg install foremost` |
| 59 | Radare2 | Reverse Engineering | `pkg install radare2` |
| 60 | GDB | Debugger | `pkg install gdb` |
| 61 | Yara | Malware Matching | `pkg install yara` |
| 62 | Strings | Binary Strings | `pkg install binutils` |
| 63 | xxd | Hex Dump | `pkg install vim` |
| 64 | Hashcat | Password Cracking | `pkg install hashcat` |
| 65 | John the Ripper | Password Cracking | `pkg install john` |
| 66 | Hydra | Online Brute Force | `pkg install hydra` |
| 67 | Medusa | Online Brute Force | `pkg install medusa` |
| 68 | Crunch | Wordlist Generator | `pkg install crunch` |
| 69 | Cupp | Targeted Wordlist | `git clone Mebus/cupp` |
| 70 | Metasploit | Exploit Framework | `pkg install metasploit-framework` |
| 71 | RouterSploit | Router Exploitation | `git clone + pip` |
| 72 | Searchsploit | Exploit Database | `pkg install exploitdb` |
| 73 | BeEF | Browser Exploitation | `git clone beefproject/beef` |
| 74 | SET | Social Engineering | `git clone trustedsec/set` |
| 75 | HiddenEye | Phishing Framework | `git clone DarkSecDevelopers` |
| 76 | SocialFish | Phishing Framework | `git clone UndeadSec` |
| 77 | Bettercap | Network MITM | `pkg install bettercap` |
| 78 | Ettercap | Network MITM | `pkg install ettercap` |
| 79 | Aircrack-ng | WiFi Testing | `pkg install aircrack-ng` |
| 80 | Reaver | WPS Attack | `pkg install reaver` |
| 81 | Kismet | Wireless Detection | `pkg install kismet` |
| 82 | Hping3 | Packet Crafting | `pkg install hping3` |
| 83 | Slowloris | DoS Testing | `pip install slowloris` |
| 84 | Snort | IDS/IPS | `pkg install snort` |
| 85 | Tcpflow | TCP Stream Capture | `pkg install tcpflow` |
| 86 | Netcat | Network Swiss Knife | `pkg install netcat-openbsd` |
| 87 | Socat | Advanced Relay | `pkg install socat` |
| 88 | Proxychains | Traffic Routing | `pkg install proxychains-ng` |
| 89 | Tor | Anonymity Network | `pkg install tor` |
| 90 | OpenSSL | SSL/TLS Testing | `pkg install openssl` |
| 91 | SSLyze | SSL Scanner | `pip install sslyze` |
| 92 | TestSSL.sh | SSL Testing | `git clone drwetter/testssl` |
| 93 | Searchsploit/ExploitDB | CVE Research | `pkg install exploitdb` |
| 94 | Empire | Post-Exploitation | `git clone BC-SECURITY/Empire` |
| 95 | Sliver | C2 Framework | `curl sliver.sh/install \| bash` |
| 96 | Mimikatz (via msfvenom) | Credential Dump | Via Metasploit kiwi module |
| 97 | Pupy | RAT & Post-Exploit | `git clone n1nj4sec/pupy` |
| 98 | PowerSploit | PowerShell Exploit | `git clone PowerShellMafia` |
| 99 | BloodHound | AD Mapping | Download from BloodHoundAD |
| 100 | Impacket | Protocol Attacks | `pip install impacket` |

---

## 🔒 ADVANCED & CLOUD (101-150)

| # | Tool | Category | Install |
|---|------|----------|---------|
| 101 | Responder | LLMNR Poisoning | `git clone lgandx/Responder` |
| 102 | CrackMapExec | AD Auditing | `pip install crackmapexec` |
| 103 | Enum4linux | SMB Enumeration | `pkg install enum4linux` |
| 104 | Smbmap | SMB Share Enum | `pip install smbmap` |
| 105 | Ldapdomaindump | LDAP/AD Dump | `pip install ldapdomaindump` |
| 106 | Kerbrute | Kerberos Enum | `go install ...kerbrute` |
| 107 | Ligolo-ng | Tunneling/Pivoting | `go install ...ligolo` |
| 108 | Chisel | TCP Tunneling | `go install ...chisel` |
| 109 | Pwncat | Post-Exploit Shell | `pip install pwncat-cs` |
| 110 | LinPEAS | Linux PrivEsc | `curl + bash linpeas.sh` |
| 111 | GTFOBins | Living Off Land | Reference site |
| 112 | Pspy | Process Monitor | Binary download |
| 113 | Dirb | Web Dir Brute | `pkg install dirb` |
| 114 | Burp Suite | Web Proxy | Download portswigger.net |
| 115 | Caido | Modern Web Proxy | Download caido.io |
| 116 | Corsy | CORS Scanner | `git clone + pip` |
| 117 | SSRF-Sheriff | SSRF Detection | `go install ...ssrf-sheriff` |
| 118 | Interactsh | OOB Detection | `go install ...interactsh` |
| 119 | JADX | APK Decompiler | `pip install jadx-wrapper` |
| 120 | Apktool | APK RE | `pkg install apktool` |
| 121 | MobSF | Mobile Security | `git clone MobSF` |
| 122 | Androbugs | Android Vuln Scan | `git clone AndroBugs` |
| 123 | Frida | Dynamic Instrument | `pip install frida-tools` |
| 124 | Objection | Mobile Runtime | `pip install objection` |
| 125 | Subfinder+Httpx+Nuclei | Recon Pipeline | Combine tools 4+6+7 |
| 126 | GhostFramework | Offensive Framework | `git clone entynetproject` |
| 127 | Mdk4 | WiFi DoS | `pkg install mdk4` |
| 128 | Wifite2 | Automated WiFi | `pip install wifite2` |
| 129 | AhMyth RAT | Android RAT | `git clone AhMyth` |
| 130 | Kali NetHunter | Android Pentesting | Requires root |
| 131 | Wigle.net CLI | WiFi OSINT | `pip install wigle` |
| 132 | LaZagne | Credential Recovery | `git clone AlessandroZ` |
| 133 | Gitjacker | .git Exploitation | `go install ...gitjacker` |
| 134 | Git-dumper | .git Exploitation | `pip install git-dumper` |
| 135 | S3Scanner | Cloud Storage OSINT | `pip install s3scanner` |
| 136 | CloudMapper | Cloud Mapping | `git clone duo-labs` |
| 137 | Pacu | AWS Exploitation | `pip install pacu` |
| 138 | Semgrep | Code Analysis | `pip install semgrep` |
| 139 | Graudit | Source Audit | `git clone wireghoul/graudit` |
| 140 | Retire.js | JS Vuln Scanner | `npm install -g retire` |
| 141 | OSV-Scanner | Dependency Vulns | `go install ...osv-scanner` |
| 142 | Prowler | Cloud Security | `pip install prowler` |
| 143 | Metabigor | OSINT No APIs | `go install ...metabigor` |
| 144 | Chaos Client | Bug Bounty Assets | `go install ...chaos` |
| 145 | Naabu | Port Scanner | `go install ...naabu` |
| 146 | Fingerprintx | Service Fingerprint | `go install ...fingerprintx` |
| 147 | Ppmap | Prototype Pollution | `go install ...ppmap` |
| 148 | GraphQLmap | GraphQL Testing | `git clone swisskyrepo` |
| 149 | Newman | API Testing | `npm install -g newman` |
| 150 | Hayabusa | Event Log Analysis | Binary download |

---

## ⚡ Quick Termux Install Batches

```bash
# Core pkg tools (batch 1)
pkg install -y nmap amass recon-ng gobuster nikto whatweb \
  hydra medusa crunch john hashcat binwalk steghide foremost \
  radare2 gdb yara tshark tcpdump aircrack-ng bettercap kismet \
  hping3 snort netcat-openbsd socat proxychains-ng tor openssl \
  feroxbuster mdk4 enum4linux dirb exploitdb apktool

# Python tools (batch 2)
pip install --break-system-packages \
  arjun dirsearch wapiti3 subfinder sherlock \
  theHarvester spiderfoot shodan holehe maigret instaloader \
  volatility3 sslyze impacket crackmapexec smbmap ldapdomaindump \
  pwncat-cs slowloris wifite2 s3scanner prowler semgrep \
  frida-tools objection git-dumper metabigor wfuzz \
  truffleHog droopescan

# Go tools (batch 3) — requires: pkg install golang
export GOPATH=$HOME/go && export PATH=$PATH:$GOPATH/bin
go install github.com/projectdiscovery/subfinder/v2/cmd/subfinder@latest
go install github.com/projectdiscovery/httpx/cmd/httpx@latest
go install github.com/projectdiscovery/nuclei/v2/cmd/nuclei@latest
go install github.com/projectdiscovery/naabu/v2/cmd/naabu@latest
go install github.com/projectdiscovery/dnsx/cmd/dnsx@latest
go install github.com/projectdiscovery/katana/cmd/katana@latest
go install github.com/projectdiscovery/chaos-client/cmd/chaos@latest
go install github.com/ffuf/ffuf@latest
go install github.com/hahwul/dalfox/v2@latest
go install github.com/tomnomnom/waybackurls@latest
go install github.com/tomnomnom/assetfinder@latest
go install github.com/tomnomnom/unfurl@latest
go install github.com/lc/gau/v2/cmd/gau@latest
go install github.com/hakluke/hakrawler@latest
go install github.com/zricethezav/gitleaks/v8@latest
go install github.com/ropnop/kerbrute@latest
go install github.com/jpillora/chisel@latest
go install github.com/liamg/gitjacker@latest
go install github.com/google/osv-scanner/cmd/osv-scanner@latest
go install github.com/kleiton0x00/ppmap@latest
go install github.com/j3ssie/metabigor@latest
go install github.com/praetorian-inc/fingerprintx/cmd/fingerprintx@latest
```

---

*Full explanations for all 150 tools: see BOJACK_FEZZY_150_TOOLS.pdf*

*philfesters · Strategy Over Impulse · 999 · Ravensmead, Cape Town*
