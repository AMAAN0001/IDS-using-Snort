# Intrusion Detection System (IDS) Using Snort


**Timeline:** Dec 2024 – Jan 2025
**Author:** Sayyed Amaan


## 📌 Overview
This project implements a real-time **Intrusion Detection System (IDS)** using **Snort**. It monitors live network traffic, performs advanced packet inspection, and identifies patterns associated with common cyber threats (port scans, brute-force attempts, exploit payloads). The detection capability is enhanced with **custom Snort rules**.


## 🚀 Key Features
- Real-time traffic monitoring & analysis
- Packet capture, inspection, and filtering
- Detection for: TCP port scans, SSH/FTP brute-force, suspicious downloads, SQLi, shellcode
- Tuned with custom **`local.rules`**


## 🛠️ Tech Stack
- **Snort** (IDS)
- **Linux** (Ubuntu/Debian/Kali)
- **tcpdump / Wireshark** (optional verification)


## ⚡ Quick Start
```bash
# 1) Install Snort (Debian/Ubuntu-based)
sudo apt-get update && sudo apt-get install -y snort


# 2) Verify installation
snort -V


# 3) Copy repo files into place (example paths)
sudo mkdir -p /etc/snort/rules
sudo cp rules/local.rules /etc/snort/rules/local.rules
sudo cp configs/snort.conf.example /etc/snort/snort.conf


# 4) Run Snort in IDS mode (replace eth0 with your interface)
sudo snort -A console -q -c /etc/snort/snort.conf -i eth0
