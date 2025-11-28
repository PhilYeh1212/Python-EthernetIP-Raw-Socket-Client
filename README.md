> **🔥 BLACK FRIDAY SALE:** Get **15% OFF** all source codes with code `BLACKFRIDAY`. [**Click here to apply discount automatically**](https://pokhts.gumroad.com/l/senior-engineer-toolkit?offer_code=BLACKFRIDAY)





# 🏭 Ethernet/IP Raw Packet Debugger & Mock PLC (Python)

[![Python](https://img.shields.io/badge/Python-3.x-blue.svg)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)]()
[![Protocol](https://img.shields.io/badge/Protocol-Ethernet%2FIP%20(CIP)-orange.svg)]()

> **Master the CIP protocol without expensive hardware.**
> This project demonstrates how to implement the **Ethernet/IP (CIP)** protocol using pure Python `socket` and `struct` libraries.
> It includes a **Mock PLC Server** that runs on localhost, allowing you to test the full `Forward Open` / `Forward Close` handshake and **Implicit Messaging (UDP I/O)** without needing a physical Allen-Bradley or Omron PLC.


[Ethernet/IP Debugger Demo]<img width="1916" height="1021" alt="螢幕擷取畫面 2025-11-18 213948" src="https://github.com/user-attachments/assets/70d072fb-b530-4720-b236-ee0a7a5b75e4" />
---

## 🚀 Features
* **Zero Dependencies:** Written in standard Python. No heavy libraries like `pycomm3` or `cpppo`.
* **Full Handshake Implementation:**
    * Command `0x65` (Register Session)
    * Command `0x6F` (Send RR Data / Forward Open)
    * UDP I/O Data Exchange (Class 1 Implicit Messaging)
* **Mock PLC Included:** A server script that simulates a CIP-compliant device, listening on TCP 44818 and UDP 2222.

---

## ⚡ Quick Start (How to Run)

Since this simulates a real network connection, you need to run the **Server** and **Client** in separate terminals.

### Step 1: Start the Mock PLC
Open your first terminal window and run:
```bash
python mock_plc_server.py
Output: [Mock PLC] TCP Listening on 44818
Step 2: Start the Client GUI
Open a second terminal window and run:

Bash

python client_gui.py
Step 3: Connect & Test
In the GUI, set Target IP to 127.0.0.1 (Localhost).

Set UDP Port to 2222.

Click ▶ Start I/O Cycle.
```
You will see the Hex Dump Logs appearing in both windows, simulating a real-time cyclic data exchange between a Controller (Scanner) and an Adapter.

📥 Download Source Code
The repository here provides a preview of the architecture.

To get the Complete Source Code (including the GUI implementation, threading logic, and the robust Mock PLC server), you can download the full study kit.

👉 Download the Full Kit on Gumroad ($9.9):[Link](https://pokhts.gumroad.com/l/ethernet-ip-study-kit)

(Includes: client_gui.py, mock_plc_server.py, and a detailed Protocol Guide)

👨‍💻 About the Author
Phil Yeh - Senior Automation Engineer

My Gumroad Store (More Engineering Tools)

Keywords: Ethernet/IP, CIP, Industrial Automation, Python, Scada, PLC, Allen-Bradley, Socket Programming, Source Code, Mock Server
