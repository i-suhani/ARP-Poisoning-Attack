# 🕵️ ARP Poisoning (Man-in-the-Middle) using Ettercap

## 📌 Overview
This repository documents a **Man-in-the-Middle (MITM) attack via ARP poisoning** performed in a controlled lab environment as part of an internship with **IIT Jammu**. The goal is to demonstrate how ARP spoofing can redirect traffic through an attacker and expose plaintext (HTTP) credentials, and to discuss **defensive countermeasures**.

> ⚠️ **Educational Use Only.** Do not run these techniques on networks without explicit permission.

---

## 🛠 Tools
- **Kali Linux**
- **Ettercap (GUI)**
- **Wireshark** (optional, for packet analysis)
- **VirtualBox / VMware**

---

## 📂 Repository Structure
```

/screenshots    # Screenshots of the setup and captured traffic
/report         # Detailed report (PDF) and slides (PPTX)
/README.md      # You're reading this
/LICENSE        # MIT License

```

---

## 🚀 Quick Start (Reproduce in Lab)
1. Enable IP forwarding on the attacker (Kali) machine.  
2. Launch Ettercap GUI: `sudo ettercap -G`  
3. Select network interface (e.g., `eth0`) → **Scan for hosts**.  
4. Set **TARGET 1** (victim IP) and **TARGET 2** (gateway IP).  
5. Start **ARP poisoning** with “Sniff remote connections”.  
6. Observe captured HTTP credentials and requests.  

> Note: HTTPS traffic is encrypted and will not reveal credentials unless additional techniques are used.

---

## 📊 Documentation
- **Full Report (PDF):** `report/ARP_Poisoning_Report (2).pdf`  
- **Slides (PPTX):** `report/MITM_Ettercap_Report.pptx`  

---
## 🔐 Mitigation & Defenses
- Prefer **HTTPS**; disable plaintext logins.
- Use **ARP monitoring** / static ARP entries when possible.
- **Client isolation** on Wi‑Fi networks.
- **IDS/IPS** rules to detect ARP anomalies.

---

## 👩‍🏫 Attribution
- Project executed during internship with **IIT Jammu**.
- Author: *Suhani Saini* — connect on LinkedIn.

---

## ⚖️ License
This project is released under the **MIT License** (see `LICENSE`).