# NetAutomate Pro – Multi-Vendor Network Automation Suite

![Bash](https://img.shields.io/badge/shell-bash-4EAA25?logo=gnubash&logoColor=white)
![Ubuntu](https://img.shields.io/badge/ubuntu-22.04-E95420?logo=ubuntu&logoColor=white)
![MikroTik](https://img.shields.io/badge/mikrotik-routeros-293239?logo=mikrotik&logoColor=white)
![Cisco](https://img.shields.io/badge/cisco-ios-1BA0D7?logo=cisco&logoColor=white)
![Windows](https://img.shields.io/badge/windows-10-0078D6?logo=windows&logoColor=white)

**Automation scripts for rapid network infrastructure deployment** on Ubuntu Server, Cisco switches, and MikroTik routers.

> Developed during vocational training at SMKN 5 Bandung (Computer & Network Engineering) and tested in production-simulated environments.

---

## 📌 Quick Overview

| Script | Target Device | Primary Function |
|--------|---------------|------------------|
| `tomasi.sh` | Ubuntu Server | Web server deployment, SSH hardening, firewall configuration |
| `miktomasi.sh` | MikroTik RouterOS | VLAN setup, PCQ bandwidth, hotspot, firewall filtering |
| `ciscotomasi.sh` | Cisco Switch | VLAN trunking, port security, basic hardening |

---

## 🚀 Features

### Ubuntu Server (`tomasi.sh`)
- ✅ Apache2 & PHP deployment
- ✅ SSH key-based authentication
- ✅ UFW firewall automation
- ✅ User account provisioning

### MikroTik RouterOS (`miktomasi.sh`)
- ✅ VLAN configuration
- ✅ PCQ bandwidth management
- ✅ Hotspot server setup
- ✅ Firewall filter rules
- ✅ DNS static & port forwarding

### Cisco Switch (`ciscotomasi.sh`)
- ✅ VLAN creation & trunking
- ✅ Port security configuration
- ✅ Spanning-tree optimization
- ✅ Basic switch hardening

---

📁Project Structure
network-automation-suite/
├── ubuntu/
│ └── tomasi.sh
├── mikrotik/
│ └── miktomasi.sh
├── cisco/
│ └── ciscotomasi.sh
└── README.md

---

🛠️Tech Stack

| Device | Technologies |
|--------|--------------|
| Ubuntu | Bash, SSH, UFW |
| MikroTik | CLI scripts, SSH/winbox, PCQ queues |
| Cisco | Expect, Telnet/SSH, VLAN trunk |

---

## 🚀 Quick Start

### Prerequisites
- Ubuntu Server 22.04 (bare metal or VM)
- MikroTik RouterOS (CHR or physical)
- Cisco Switch (IOS 12.2+)
- SSH/Telnet access to all devices
- PnetLab / GNS3 / EVE-NG (for simulation)

### Run Ubuntu Automation

```bash
# Copy script to Ubuntu server
scp ubuntu/tomasi.sh user@ubuntu-server:/tmp/

# SSH into Ubuntu server
ssh user@ubuntu-server

# Make executable and run
chmod +x /tmp/tomasi.sh
sudo /tmp/tomasi.sh
Run MikroTik Automation
bash
# Copy script to MikroTik
scp mikrotik/miktomasi.sh admin@192.168.88.1:/

# SSH into MikroTik
ssh admin@192.168.88.1

# Execute script
/import miktomasi.sh
Run Cisco Automation
bash
# Copy script to Cisco switch
scp cisco/ciscotomasi.sh admin@192.168.1.1:

# SSH into Cisco switch
ssh admin@192.168.1.1

# Run script (Cisco uses different syntax - adjust as needed)
📸 Demonstration
Ubuntu Server	MikroTik RouterOS	Cisco Switch
https://./screenshots/ubuntu.png	https://./screenshots/mikrotik.png	https://./screenshots/cisco.png
Replace placeholder images with actual terminal screenshots from your setup.

📈 Impact
Metric	Before Automation	After Automation
Deployment Time	2–3 hours	~15 minutes
Configuration Errors	Frequent	Minimal
Reproducibility	Manual, fragile	One-command
Documentation	Separate	Built into scripts
🧪 Test Environment
Component	Specification
Simulation	PnetLab
Ubuntu Server	2x Ubuntu 22.04
MikroTik	1x RouterOS CHR
Cisco Switch	1x IOSv
Network	VLAN10 (Prod), VLAN20 (Guest), VLAN30 (Mgmt)
Client OS	Windows 10
📝 Script Details
tomasi.sh (Ubuntu)
Installs Apache2, PHP, and required modules

Configures UFW with specific rules (SSH, HTTP, HTTPS)

Sets up SSH key authentication (disables password login)

Creates standard user accounts

miktomasi.sh (MikroTik)
Configures VLANs on specified interfaces

Sets up PCQ queues for bandwidth management

Enables hotspot on selected interfaces

Adds firewall filter rules for security

ciscotomasi.sh (Cisco)
Creates VLANs and assigns ports

Configures trunk ports with allowed VLANs

Enables port security with sticky MAC

Sets up basic switch security (disable unused ports, etc.)

🔧 Troubleshooting
Issue	Solution
Permission denied	Run chmod +x script.sh
SSH connection failed	Check IP address and firewall rules
MikroTik import error	Ensure script uses RouterOS syntax (not Bash)
Cisco command not found	Use Cisco IOS syntax, not Bash
📄 License
MIT

👨‍💻 Author
Faris Farasdak Al Murtadha

GitHub: @falender0r

Portfolio: farisdev.vercel.app

Email: farasdakalfaris@gmail.com

Location: Bandung, Indonesia

🙏 Acknowledgments
SMKN 5 Bandung – Computer & Network Engineering Program

PnetLab Community

MikroTik & Cisco documentation

All instructors who provided guidance

⭐ Star this repository if you find it useful for network automation!

text

---

## Cara Copy Paste ke Notepad

1. Di terminal, sudah kamu ketik `notepad README.md` (dari perintah sebelumnya)
2. Notepad akan terbuka
3. **Blok semua teks README di atas** (dari `# NetAutomate Pro...` sampai akhir)
4. **Copy** (Ctrl+C)
5. **Paste ke Notepad** (Ctrl+V)
6. **Simpan** (Ctrl+S)
7. **Tutup Notepad**

---

## Kembali ke Terminal

Setelah notepad ditutup, lanjutkan perintah:

```bash
git add .
git commit -m "Add professional README with multi-vendor automation guide"
git push -u origin main --force
