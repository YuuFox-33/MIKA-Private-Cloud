# MIKA-Private-Cloud


A self-hosted, zero-trust private cloud built on Raspberry Pi using WireGuard and Filebrowser.

This project is designed to provide secure, private, and scalable storage infrastructure with direct filesystem access, optimized for AI training pipelines and personal data ownership.

---

## ✨ Features

- 🔐 WireGuard-based private networking (no exposed services)
- 📁 Filebrowser web UI for file management
- 💾 NVMe SSD-backed storage
- 👤 Per-user isolated directories
- 🧠 AI-friendly: direct disk access for training workloads
- 📱 Accessible from PC and mobile devices over VPN
- 📴 Fully usable offline / LAN-only

---

## 🏗 Architecture Overview

- **Hardware:** Raspberry Pi 5 + NVMe SSD
- **Network:** WireGuard VPN (10.10.0.0/24)
- **Storage:** ext4 on SSD, mounted at `/mnt/ssd`
- **Users:** Linux users mapped to isolated storage roots
- **UI:** Filebrowser (no cloud dependency)

---

## 📂 Storage Layout

/mnt/ssd/--clint 1
         --Clint 2
         --Clint 3


Each directory is:
- Privately owned
- Permission-isolated
- VPN-accessible only

---

## 🔐 Security Model

- No public IP exposure
- No port forwarding
- All access through WireGuard
- No third-party cloud services
- Admin-controlled credentials

See [`docs/threat-model.md`](docs/threat-model.md).

---

## 🚀 Use Cases

- Personal private cloud
- AI dataset storage (MIKA)
- Secure file sync across devices
- Off-grid or low-trust network environments
- Edge computing experiments

---

## 🛠 Status

🟢 **Active development**

Next milestones:
- systemd services
- quota enforcement
- automated backups
- multi-node expansion

---

## 📜 License

MIT 
         
