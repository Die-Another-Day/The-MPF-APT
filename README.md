# MPF APT Repository

Official APT repository for the **Mobile Pentesting Framework (MPF)**.

This repository allows Debian/Ubuntu-based systems to install and update MPF using the native APT package manager.

---

# Supported Platforms

* Ubuntu 22.04+
* Ubuntu 24.04+
* Debian 12+
* Kali Linux (Debian-based)
* WSL Ubuntu

---

# Linux Installation

## 1. Import the MPF signing key

```bash
curl -fsSL https://die-another-day.github.io/The-MPF-APT/public-key.asc \
| gpg --dearmor \
| sudo tee /usr/share/keyrings/mpf.gpg > /dev/null
```

## 2. Add the MPF repository

```bash
echo "deb [signed-by=/usr/share/keyrings/mpf.gpg] https://die-another-day.github.io/The-MPF-APT stable main" \
| sudo tee /etc/apt/sources.list.d/mpf.list
```

## 3. Update package lists

```bash
sudo apt update
```

## 4. Install MPF

```bash
sudo apt install mpf
```

## 5. Launch MPF

```bash
mpf
```

---

# Updating MPF

Whenever a new release is published:

```bash
sudo apt update
sudo apt upgrade mpf
```

---

# Verify Installation

```bash
which mpf
```

Expected output:

```text
/usr/bin/mpf
```

Check version:

```bash
mpf --version
```

---

# Windows Installation

MPF currently provides native package management support through APT on Linux.

For Windows users:

## Option 1 (Recommended)

Install WSL (Windows Subsystem for Linux):

```powershell
wsl --install
```

After Ubuntu is installed, follow the Linux installation steps above.

## Option 2

Clone the framework manually:

```powershell
git clone https://github.com/Die-Another-Day/The-MPF.git
cd The-MPF
```

Run MPF:

```powershell
ruby bin/mpf
```

Requirements:

* Ruby
* Java Runtime Environment
* Apktool

---

# Repository Information

Repository URL:

https://die-another-day.github.io/The-MPF-APT

Source Code:

https://github.com/Die-Another-Day/The-MPF

---

# About MPF

Mobile Pentesting Framework (MPF) is a mobile application security assessment framework designed for Android and iOS application analysis.

Current capabilities include:

* Static Analysis
* Dynamic Analysis
* OWASP Mobile Top 10 Coverage
* Vulnerability Correlation
* Attack Chain Generation
* Intelligence Analysis
* HTML Reporting
* Android APK Analysis
* iOS IPA Analysis

---

# License

Refer to the license provided in the main MPF repository.
