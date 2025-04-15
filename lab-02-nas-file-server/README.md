# Lab 02 – Home NAS File Server using Raspberry Pi

## 🧠 Objective
Create a secure, headless network-attached storage (NAS) system using a Raspberry Pi, Linux, and Samba. Simulate a small office file sharing solution similar to enterprise-level file server infrastructure.

## 🛠️ Tools & Technology
- Raspberry Pi 4 (4GB RAM)
- Raspberry Pi OS (Lite)
- Linux Terminal (Bash)
- Samba for SMB/CIFS protocol
- Windows 11 Client for access testing

## 🧪 What I Did
- Installed Raspberry Pi OS Lite on a microSD card for a headless setup
- Configured Linux file system partitions and mounted a 2TB SSD as persistent storage using `fstab`
- Installed and configured Samba for cross-platform SMB file sharing with user-based authentication
- Set secure folder and file permissions with `chmod`, `chown`, and Samba share definitions
- Debugged system service failures and permission errors using `systemctl`, `journalctl`, and log files
- Mapped the NAS on a Windows 11 machine as a persistent network drive (Z:)

## 🔐 Security Measures
- Disabled password-less sharing
- Created restricted Samba user accounts
- Verified all file access required authentication
- Blocked unnecessary services and changed Samba ports (optional testing)

## 💡 What I Learned
- Configuring secure file shares on Linux using Samba
- Linux storage mounting, permissions, and troubleshooting
- How enterprise file shares operate behind the scenes
- Systemd-based service management and debugging techniques

## 📸 Screenshots
[Mounted_Drive](screenshot1-nas.png)
[Mapped_Drive](screenshot2-nas.png)
[Samba_Conf_Perm](screenshot3-nas.png)

---

**Status:** ✅ Complete & Functional  

