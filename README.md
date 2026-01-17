# WiFi Deauth Tool (SHADOW269)

A Python-based automation script for wireless network auditing. This tool simplifies the process of discovering nearby Access Points (APs) and performing deauthentication attacks using the `aircrack-ng` suite.

## 🛠 Features

* **Automatic Dependency Check:** Verifies if required tools are installed.
* **Interface Management:** Automatically discovers wireless interfaces and forces "Monitor Mode."
* **Real-time Scanning:** Live dashboard view of available networks (BSSID, Channel, and ESSID).
* **Targeted Deauth:** Disconnects users from a specific Access Point by flooding deauthentication frames.
* **Auto-Cleanup:** Backs up old scan data and restores network services (NetworkManager) upon exit.

---

## 📋 Prerequisites

Before running the script, ensure your system has the following:

1. **Linux OS** (Kali Linux, Parrot OS, or Ubuntu recommended).
2. **Wireless Adapter** that supports **Monitor Mode** and **Packet Injection**.
3. **Aircrack-ng Suite**:
```bash
sudo apt update && sudo apt install aircrack-ng -y

```



---

## 🚀 Installation & Usage

### 1. Clone the repository

```bash
git clone https://github.com/SHADOW269/your-repo-name.git
cd your-repo-name

```

### 2. Make the script executable

```bash
chmod +x script.py

```

### 3. Run with Root Privileges

The script requires `sudo` to manipulate network interfaces and hardware.

```bash
sudo python3 script.py

```

---

## 📖 How it Works

1. **Monitor Mode:** The script kills conflicting processes and toggles your WiFi card from "Managed" to "Monitor" mode.
2. **Discovery:** It launches `airodump-ng` in the background and parses the CSV output to show you a clean table of nearby networks.
3. **Deauthentication:** Once you select a target index, the script locks your card to the target's channel and uses `aireplay-ng` to send deauth packets.
* *Note: This disconnects devices from the selected WiFi network.*



---

## ⚠️ Disclaimer

**For Educational Purposes Only.** Unauthorized access or disruption of wireless networks is illegal. The author (SHADOW269) is not responsible for any misuse or damage caused by this program. Only use this tool on networks you own or have explicit permission to test.

---

## 🔗 Connect

* **Developer:** SHADOW269
* **Portfolio:** [portfolio.shadow269.in](https://portfolio.shadow269.in/)
* **GitHub:** [SHADOW269](https://github.com/SHADOW269)

