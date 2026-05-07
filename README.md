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


# EtherNet/IP Study Kit

> Learn the CIP (Common Industrial Protocol) byte-by-byte with an interactive packet inspector and a mock PLC server. The fastest way to actually understand EtherNet/IP from the wire up.

**This is a commercial educational tool, sold on Gumroad.** Source code is included in your purchase.

---

## What it does

- **Annotated packet view** — every CIP frame broken down by section, with tooltips explaining each byte
- **Mock PLC server** — talks real EtherNet/IP without needing an Allen-Bradley CompactLogix on your desk
- **Raw socket client** — see Class 3 explicit messaging at the TCP level
- **CIP service browser** — Get_Attribute_Single, Set_Attribute_Single, Read_Tag, Write_Tag
- **Implicit messaging primer** — see how I/O scanning actually works (UDP Class 1)
- **Side-by-side hex view** — bytes on one side, decoded fields on the other
- **Single-file Python** — runs on Windows, macOS, Linux

## Why this exists

EtherNet/IP is one of the most widely deployed industrial protocols, but learning resources are terrible. ODVA's spec costs $1,200. Books are out of print. Vendor docs assume you already know CIP. Most engineers learn by reverse-engineering Wireshark captures.

This tool flips that — you can see every CIP service request as it's built, byte by byte, with annotations explaining what each field does. It's how I wish I'd learned EtherNet/IP.

## Who this is for

| Audience | Why it fits |
|---|---|
| Junior controls engineers | Understand the protocol before you debug live PLCs |
| Embedded engineers | Implement EtherNet/IP slaves correctly |
| Security researchers | Analyze CIP traffic for vulnerabilities |
| Students | Learn industrial networking without a lab budget |
| EtherNet/IP scanner developers | See real frame structures for testing |

## What's covered

- Connection management (forward open, forward close)
- Class 3 explicit messaging (TCP)
- Class 1 implicit I/O (UDP) — basics
- CIP path encoding (logical, symbolic)
- Common services: Get/Set Attribute, Read/Write Tag, Reset
- Object model basics (identity, message router, connection manager)

## What's NOT covered (yet)

- ODVA conformance test details
- Advanced safety profiles (CIP Safety)
- Motion profiles (CIP Motion)
- Sync-over-EtherNet/IP

## Get it

→ **[EtherNet/IP Study Kit on Gumroad — $29](https://philyeh.gumroad.com/l/ethernetip-study-kit)**

Or grab the **[Industrial Toolkit Bundle](https://philyeh.gumroad.com/l/industrial-toolkit-bundle)** ($129) — EtherNet/IP + J1939 + Modbus + MQTT.

## What's in the purchase

- `eip_study_kit.py` — Annotated packet inspector + mock PLC server
- `eip_client_examples.py` — Working CIP client examples
- `requirements.txt` — Pinned dependencies
- `README.md` — Setup + study guide
- Commercial use license per Gumroad EULA

## License

Commercial use license per Gumroad EULA. You may use this software at the company that purchased it for any commercial purpose. Redistribution, resale, or open-sourcing the code is not permitted.

## Support

- Reply to your Gumroad purchase email
- Questions about CIP / EtherNet/IP via [GitHub Issues](https://github.com/PhilYeh1212/Python-EthernetIP-Raw-Socket-Client/issues)

---

I write about industrial Python and protocol internals at **[dev.to/philyeh](https://dev.to/philyeh)**, and post Chinese versions on [iThelp](https://ithelp.ithome.com.tw/users/20171204).

— Phil Yeh · Senior Automation Engineer · Industrial Python · Developer Tools

