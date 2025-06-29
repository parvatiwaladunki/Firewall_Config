# Firewall Config

## Objective
Configure and test basic firewall rules using **Windows Defender Firewall** to block and allow specific ports.

---

## Tools Used
- Windows Defender Firewall with Advanced Security
- Telnet client (Windows Feature)
- Command Prompt (`cmd`)

---

##  Configuration Steps

### 1. Viewed Current Firewall Rules
- Opened `Windows Defender Firewall with Advanced Security`.
- Navigated to **Inbound Rules** to view existing traffic rules.

### 2. Created Rule to **Block Telnet (Port 23)**
- Created a new **Inbound Rule**:
  - Type: Port
  - Protocol: TCP
  - Port: 23
  - Action: Block the connection
  - Applied to: Domain, Private, Public
  - Rule name: `Block Telnet Port 23`

### 3. Tested Rule Using Telnet
- Enabled Telnet Client:
  - Control Panel → Programs → Turn Windows features on/off → Telnet Client
- Tested with command:
  ```sh
  telnet 127.0.0.1 23

### 4. Test Results:
- Telnet on port 23 blocked as expected.
