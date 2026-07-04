🧠 Nmap (Network Mapper) – Study Notes

🔍 Overview
⚡ Nmap: A free, open-source tool used for network discovery and security auditing — scans hosts, ports, services, and operating systems.
💻 Purpose: Used by network admins and security professionals for asset discovery, port scanning, vulnerability assessment, and penetration testing.

🧩 Key Elements of Nmap
🔸 Host Discovery: Finds which devices are alive on a network before scanning ports.
🔸 Port Scanning: Identifies open, closed, and filtered ports on a target.
🔸 Service/Version Detection: Determines exactly what software is running behind each port.
🔸 OS Fingerprinting: Guesses the target's operating system from how it responds to packets.
🔸 NSE (Scripting Engine): Automates vulnerability checks and advanced recon using scripts.

🧱 Types of Nmap Scans
📡 Ping Scan (-sn): Detects live hosts without scanning ports.
🔓 TCP Connect Scan (-sT): Completes full handshake; reliable, easily logged.
🥷 SYN Scan (-sS): Half-open scan; stealthier, needs root/sudo.
📶 UDP Scan (-sU): Scans UDP-based services (DNS, DHCP, SNMP).
🔬 Version Detection (-sV): Identifies service names and versions.
🖥️ OS Detection (-O): Fingerprints the target's operating system.
🛠️ Script Scan (--script): Runs NSE scripts for vuln detection or automation.
📊 Aggressive Scan (-A): Combines OS detection, version detection, script scanning, and traceroute.

⚙️ Nmap – Practical Setup (Linux)

📦 Step 1: Install Nmap
sudo apt install nmap

📂 Step 2: Basic Host Discovery
sudo nmap -sn 192.168.1.0/24

🚀 Step 3: Scan a Target
nmap 192.168.1.5

🔬 Step 4: Service & Version Detection
sudo nmap -sV 192.168.1.5

🖥️ Step 5: OS Detection
sudo nmap -O 192.168.1.5

🛠️ Step 6: Run Vulnerability Scripts
nmap --script vuln 192.168.1.5

💾 Step 7: Save Results
nmap 192.168.1.5 -oN scan_results.txt

🧠 Purpose of Study
🔹 To understand how networks and services can be mapped and audited.
🔹 To identify open ports and outdated/vulnerable services before attackers do.
🔹 To build core reconnaissance skills used in penetration testing.

⚠️ Ethical Use Reminder
🚫 Nmap must only be used on networks and hosts you own, or have explicit written authorization to test.
✅ Unauthorized scanning of networks you don't control can violate laws like the IT Act (India) or the Computer Fraud and Abuse Act (US), even without malicious intent.

🛡 Defensive Measures (Blue Team Side)
🔐 Close or firewall unused ports.
🧩 Run your own regular Nmap scans to catch unexpected open services.
📬 Monitor logs for repeated scan patterns (a sign of recon activity).
🧱 Use IDS/IPS to detect and alert on scanning behavior.
📚 Patch and update services regularly to reduce what attackers can exploit.

📘 Reference
🔗 Official Site: https://nmap.org
🔗 Download: https://nmap.org/download.html
👨‍💻 Author: Gordon Lyon (Fyodor)

🧾 Summary
Nmap is the foundation of network reconnaissance — it maps live hosts, open ports, running services, and operating systems. Security learners use it to understand how attackers discover targets, which directly strengthens defensive skills like hardening, monitoring, and vulnerability management.
