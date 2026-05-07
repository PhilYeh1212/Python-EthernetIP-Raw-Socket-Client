# 🏭 EtherNet/IP Study Kit — Learn CIP Byte-by-Byte (Mock PLC Included)

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Stdlib](https://img.shields.io/badge/Dependencies-stdlib%20only-success.svg)](https://docs.python.org/3/library/)
[![Protocol](https://img.shields.io/badge/Protocol-EtherNet%2FIP%20%2F%20CIP-orange.svg)](https://www.odva.org/)
[![License](https://img.shields.io/badge/License-MIT--like-lightgrey.svg)](#-license)

> **Stop reading the 700-page ODVA spec at midnight.** An interactive
> learning toolkit for the EtherNet/IP (CIP) protocol — every byte of
> every packet labeled, color-coded, and explained. Includes a real
> CIP-parsing **Mock PLC server** so you can learn without buying
> $2,000 of hardware.

EtherNet/IP Study Kit screenshot
<img width="1280" height="720" alt="eip_cover" src="https://github.com/user-attachments/assets/042b882b-5b0e-42c2-8d20-47e640261b2d" />


---

## 🎯 Why this exists

EtherNet/IP and CIP are powerful — but the official ODVA specs cost $400
and most online tutorials hand you a hex string and say "send this", which
teaches you nothing about *why* it works.

This kit does the opposite:

- **Every byte is labeled**: `65 00` is "Cmd 0x65 (Register Session)"
- **Every field has a tooltip** explaining what it does
- **The Mock PLC actually parses your packets** (it's not a dumb echo
  server — it identifies CIP services and replies with proper CPF format)
- **Step-by-step mode**: Register → Forward Open → I/O → Close, one
  click at a time, with full packet inspection

Built by an automation engineer who learned CIP the hard way and wished
this kit existed back then.

---

## 📂 Open Source vs Pro

This repo contains the **Community Edition** — a basic CIP client and a
simple mock server. Free for learning.

The **[EtherNet/IP Study Kit Pro](https://philyeh.gumroad.com)** version on
Gumroad adds the educational features that make this an actual textbook:

| Feature | Community (this repo) | **[Pro Edition ($29)](https://philyeh.gumroad.com)** |
|---|:---:|:---:|
| Register Session + Forward Open + UDP I/O | ✅ | ✅ |
| Forward Close (clean teardown) | ⚠️ Basic | ✅ |
| **Byte-by-byte annotated packet view** | ❌ | ✅ |
| **Hover tooltips** on every field | ❌ | ✅ |
| **Step-by-step interactive mode** | ❌ | ✅ |
| **Mock PLC actually parses incoming CIP** | ⚠️ Echo only | ✅ Full parser |
| **Annotated server console output** (color-coded) | ❌ | ✅ |
| **CIP Cheat Sheet** (PDF/MD reference) | ❌ | ✅ |
| **Constants for every CIP service** (no magic hex) | ❌ | ✅ |
| **Auto-incrementing sequence numbers** | ❌ | ✅ |
| **Free-Run mode** for sustained I/O testing | ❌ | ✅ |
| **Dark industrial UI theme** | ❌ | ✅ |
| **Commercial license** | ❌ | ✅ |

### 👉 [Get EtherNet/IP Study Kit Pro on Gumroad — $29](https://philyeh.gumroad.com)

Or save $47 with the **[Industrial Python Toolkit Bundle](https://philyeh.gumroad.com)**
($129) — includes EtherNet/IP + Modbus + MQTT + J1939.

---

## 🚀 Quick Start (Community Edition)

You need **two terminals**.

### Terminal 1 — start the mock PLC

```bash
git clone https://github.com/PhilYeh1212/Python-EthernetIP-Raw-Socket-Client
cd Python-EthernetIP-Raw-Socket-Client
python mock_plc_server.py
```

### Terminal 2 — launch the client

```bash
python client_gui.py
```

In the GUI, set Target IP to `127.0.0.1` and click ▶ Start. The client
will perform Register Session → Forward Open → UDP I/O → Forward Close
in a loop, while the mock PLC logs everything in Terminal 1.

**No external dependencies — pure Python standard library.**

---

## 🔧 What you'll learn

After working through this kit you will understand:

- **Why EtherNet/IP needs both TCP and UDP** (TCP for connection mgmt, UDP for I/O)
- **The 24-byte encapsulation header** that every CIP packet starts with
- **Forward Open** — what's actually being negotiated
- **O2T and T2O Connection IDs** — the most misunderstood part of CIP
- **The Common Packet Format (CPF)** that wraps every CIP message
- **Why sequence numbers matter** in Class 1 implicit messaging

The Pro version takes this further with byte-level annotation on every
packet, so you can literally watch the protocol work in real time.

---

## 📚 Related reading

- [**The Architecture of Implicit Messaging: Implementing Raw CIP I/O in Python**](https://dev.to/philyeh/the-architecture-of-implicit-messaging-implementing-raw-cip-io-in-python-1o0c)
  — my Dev.to article explaining CIP implicit messaging in depth

---

## 📥 Get the Pro version

The Community Edition gets you started. The
**[Pro version](https://philyeh.gumroad.com)** is the actual learning kit —
byte-by-byte teaching, real CIP parser, step-by-step mode, and the cheat
sheet. The cheap way to actually *understand* EtherNet/IP.

| Product | Price | Link |
|---|---:|---|
| 🏭 **EtherNet/IP Study Kit** (this tool, Pro edition) | $29 | [Buy](https://philyeh.gumroad.com) |
| 🚛 **J1939 Sniffer Pro** | $59 | [Buy](https://philyeh.gumroad.com) |
| ⚙️ **Modbus Logger Pro** | $49 | [Buy](https://philyeh.gumroad.com) |
| 📡 **MQTT Logger Pro** | $39 | [Buy](https://philyeh.gumroad.com) |
| 🔒 **Private ChatGPT Stack** | $59 | [Buy](https://philyeh.gumroad.com) |
| 📦 **Industrial Python Toolkit Bundle** (4 tools, save $47) | **$129** | [Buy](https://philyeh.gumroad.com) |
| 📊 **CSV Dashboard** (free companion tool) | $0 | [Download](https://philyeh.gumroad.com) |

---

## 📫 About

**Phil Yeh** — Senior Automation Engineer based in Taiwan. I build Python
tools for industrial protocol work.

- 🛒 **Store:** [philyeh.gumroad.com](https://philyeh.gumroad.com)
- ✍️ **Blog:** [dev.to/philyeh](https://dev.to/philyeh)

---

## 📝 License

The Community Edition in this repository is free for personal and
educational use. For commercial use (client projects, internal company
tools, products you sell), please get the **[Pro Edition](https://philyeh.gumroad.com)**
which includes a proper commercial license.

If this tool helped you, **a ⭐ on the repo** means a lot to an indie
developer. Thanks!

---

<sub>**Keywords:** Python, EtherNet/IP, CIP, ODVA, Allen-Bradley,
Rockwell, Omron, CompactLogix, ControlLogix, Implicit Messaging,
Forward Open, encapsulation, raw socket, industrial protocol, study kit</sub>
