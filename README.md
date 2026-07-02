# 🔥 CuryDDOS v1 — Advanced Network Stress Testing Suite

> ⚡ **C++ / ImGui / OpenGL3** — Single binary, zero dependencies, full stealth.

<p align="center">
  <img src="https://img.shields.io/badge/Version-1.0-green?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Language-C%2B%2B-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/License-MIT-red?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Platform-Windows%2010%2F11-lightgrey?style=for-the-badge" />
</p>

---

## 📋 Table des matieres

- [Presentation](#-presentation)
- [Fonctionnalites](#-fonctionnalites)
- [Interface](#-interface)
- [Installation](#-installation)
- [Usage](#-usage)
- [Payloads](#-payloads)
- [Stealth](#-stealth)
- [Avertissement Legal](#-avertissement-legal)

---

## 🎯 Presentation

**CuryDDOS v1** est un outil de **stress test reseau** developpe en C++ avec une interface ImGui moderne. Il utilise des **raw sockets** pour generer des flux reseau a haute vitesse avec un maximum de discretion.

| Caracteristique | Detail |
|---|---|
| 🔧 **Backend** | C++ natif avec Winsock2 raw sockets |
| 🖥️ **Frontend** | ImGui + GLFW + OpenGL3 |
| 📦 **Taille** | ~1.5 MB (single binary) |
| 🚀 **DPI-Aware** | Support multi-monitor, ecrans 4K |
| 🔒 **Stealth** | Rotation automatique de profils, IP spoofing |
| 🎭 **Admin** | Demande elevation UAC au demarrage |

---

## 🛠️ Fonctionnalites

### 🔴 28 Mode d'attaque

| Categorie | Mode |
|---|---|
| 🏴 **TCP Flags** | SYN, RST, ACK, FIN, PUSH+ACK, XMAS, NULL |
| 🌊 **L4 Flood** | UDP, ICMP, QUIC, SIP, GRE |
| ⚡ **Amplification x10k** | DNS, NTP, SSDP, Memcached, Chargen, SNMP, NetBIOS, mDNS, WS-Discovery, CoAP |
| 🐌 **L7** | Slowloris |
| 💀 **Exhaustion** | DHCP Starvation, IGMP Flood |

### 🎯 Port Scanner
- SYN scan multi-thread
- Full port scan (1-65535)
- OS fingerprinting
- Service detection

### 🎭 Stealth System
- **4 niveaux** de stealth (L0 → L3)
- Rotation automatique des profils
- IP spoofing dynamique
- Fragmentation des paquets
- TTL aleatoire
- Delais intelligents

### 📊 Interface
- Real-time stats (bandwidth, packets, elapsed)
- Progress bar avec countdown
- Logs colores en temps reel
- Right-click context menu sur chaque mode (description, detection risk, success rate)
- Kill Switch d'urgence
- Scan integre avec popup resultats
- Guide d'infiltration (10 sections)
- Report generator (upload vers file.io)

### 🎁 Payload Builder
- **6 types de payloads** : Stealer, Keylogger, Spyware, Ransomware, Worm, Custom
- Compilation directe via MSVC (`cl.exe`)
- Upload vers Discord Webhook, FTP, HTTP POST
- Quick presets en un clic
- File/folder picker dialogs

---

## 🖥️ Interface

```
┌──────────────────────────────────────────────────┐
│  🔥 CuryDDOS v1 — DPI-Aware ImGui Dark Theme    │
├──────────────────────────────────────────────────┤
│  [TARGET IP]  [PORT]  [DURATION]  [INTENSITY]   │
│  ┌────────────────────────────────────────────┐  │
│  │ ☐ SYN Flood    [right-click for info]     │  │
│  │ ☐ UDP Flood                               │  │
│  │ ☐ DNS Amplification                       │  │
│  │ ☐ Slowloris                               │  │
│  │ ☐ ICMP Flood                              │  │
│  │ ... (28 modes)                             │  │
│  └────────────────────────────────────────────┘  │
│  [🟢 LAUNCH ATTACK]  [🔴 KILL SWITCH]           │
├──────────────────────────────────────────────────┤
│  Progress Bar: ████████████░░░░ 67%              │
│  Bandwidth: 1.2 Gbps | Packets: 1.2M | Time: 45s│
├──────────────────────────────────────────────────┤
│  [LOGS]                                          │
│  > [CuryDDOS] Target: 192.168.xxx.xxx:443        │
│  > [CuryDDOS] SYN Flood started                  │
│  > [CuryDDOS] Bandwidth: 1.2 Gbps                │
└──────────────────────────────────────────────────┘
```

---

## 📦 Installation

### Prerequis
- Windows 10/11
- [Visual Studio 2022+](https://visualstudio.microsoft.com/) avec le workload "Desktop development with C++"
- [CMake](https://cmake.org/) 3.20+
- [Git](https://git-scm.com/)

### Build

```bash
# Clone le repo
git clone https://github.com/ton-username/CuryDDOS_v1.git
cd CuryDDOS_v1

# Build automatique (un clic)
build.bat
```

L'executable sera genere dans `build\Release\CuryDDOS_v1.exe`.

---

## 🚀 Usage

```bash
# Lancer en admin (obligatoire)
CuryDDOS_v1.exe
```

1. **Remplir** le target IP + port
2. **Selectionner** les modes d'attaque
3. **Regler** la duree et l'intensite
4. **Cliquer** Launch Attack
5. **Kill Switch** en cas d'urgence

---

## 🎁 Payloads

Le Payload Builder genere des executables C++ compiles avec MSVC :

| Type | Description |
|---|---|
| 🔑 **Stealer** | Exfiltre navigateurs, Discord, wallets, WiFi |
| ⌨️ **Keylogger** | Enregistre frappes + presse-papiers → Discord |
| 📸 **Spyware** | Screenshots toutes les 30s → Discord |
| 🔐 **Ransomware** | Chiffrement XOR + exfiltre cle → HTTP |
| 🪱 **Worm** | Propagation SMB + autorun |
| 🛡️ **Stealth** | Toutes techniques combinees |

### Quick Presets
```
[STEALER + DISCORD]  [KEYLOGGER + HTTP]  [SPYWARE + DISCORD]
[WORM + HTTP]        [ALL STEALTH]       [RANSOMWARE + HTTP]
```

---

## 🎭 Stealth

| Niveau | Description |
|---|---|
| **L0** | Aucun stealth — performance maximale |
| **L1** | Delais aleatoires + TTL variable |
| **L2** | + IP spoofing + fragmentation |
| **L3** | + Rotation profils + delays adaptatifs |

---

## ⚖️ Avertissement Legal

> **🔴 CE LOGICIEL EST UNIQUEMENT A DES FINS EDUCATIVES ET DE RECHERCHE.**

### ⚠️ AVERTISSEMENT IMPORTANT

**CuryDDOS v1** est un outil de **stress test reseau** conçu pour :

- ✅ Tester la **resilience** de votre propre infrastructure
- ✅ Apprendre les **techniques de test de securite reseau**
- ✅ Effectuer des **audits de securite autorises**
- ✅ La **recherche academique** en securite informatique

### 🚫 UTILISATION INTERDITE

**Il est STRICTEMENT INTERDIT d'utiliser cet outil sur des reseaux ou machines n'appartenant pas a l'utilisateur, sans autorisation explicite prealable du proprietaire.**

### ⚖️ Responsabilite

- L'utilisateur est **SEUL RESPONSABLE** de l'utilisation de cet outil
- Le createur **DECLINE TOUTE RESPONSABILITE** pour tout usage abusif
- L'utilisation non autorisee peut entrainer des **poursuites judiciaires**
- Les sanctions peuvent inclure des **amendes** et de la **prison**

### 📜 Conformite

Cet outil doit etre utilise uniquement dans le cadre :

- D'un **pentest autorise** avec contrat signe
- D'un **audit de securite** avec permission ecrite
- D'un **test de charge** sur votre propre infrastructure
- D'un **projet de recherche** academique

---

<p align="center">
  <b>🔥 CuryDDOS v1 — Built with passion 🔥</b><br>
  <sub>Made by <a href="https://github.com/JusDeFruis">JusDeFruis</a> — 2026</sub>
</p>
