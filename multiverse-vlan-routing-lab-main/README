# 🧙‍♂️ MARVEL NETWORK: Multiverse Communication System (VLAN Lab)

> ⚡ *“Different worlds. Different teams. One network to control them all.”*

---

## 🌍 Mission Brief

The multiverse is expanding, and multiple superhero teams now operate from different locations.
Each team requires:

* 🔒 Isolation for security
* 🔄 Controlled communication when needed

As the Network Engineer, your mission was to:

> Design a network that **segments teams using VLANs** and enables **inter-team communication via routing**

---

## 🏗️ Network Architecture

```id="topo123"
            🧙‍♂️ Doctor Strange (Router)
                     |
                 [TRUNK]
                     |
          🏢 Avengers HQ (S1)
             /            \
    🖥️ PCs (Access)     [TRUNK]
                          |
                🏢 New Avengers Tower (S2)
                          |
                       🖥️ PCs
```

---

## 🧬 Team Segmentation (VLAN Design)

| VLAN | Team      | Members                   |
| ---- | --------- | ------------------------- |
| 10   | Avengers  | Iron Man, Captain America |
| 20   | Guardians | Star-Lord, Groot 🌱       |
| 30   | X-Men     | Wolverine 🐺, Deadpool 🔴 |

---

## ⚔️ Network Strategy

### 🧩 Layer 2 (Switching)

* VLANs used to isolate teams
* Trunk links carry multiple VLAN traffic between switches

### 🧠 Layer 3 (Routing)

* Router-on-a-Stick enables inter-VLAN communication
* Each VLAN has its own gateway (subinterface)

---

## 🔑 Key Configuration

### 🧙‍♂️ Router (Doctor Strange – Multiverse Gateway)

```bash id="routercfg"
interface g0/0.10
encapsulation dot1Q 10
ip address 192.168.10.1 255.255.255.0

interface g0/0.20
encapsulation dot1Q 20
ip address 192.168.20.1 255.255.255.0

interface g0/0.30
encapsulation dot1Q 30
ip address 192.168.30.1 255.255.255.0
```

---

### 🏢 Switch Configuration

```bash id="switchcfg"
interface fa0/X
switchport mode access
switchport access vlan <VLAN_ID>

interface fa0/Y
switchport mode trunk
```

---

## 🧪 Mission Results

| Communication              | Result              |
| -------------------------- | ------------------- |
| Iron Man ↔ Captain America | ✅ Success           |
| Star-Lord ↔ Groot          | ✅ Success           |
| Wolverine ↔ Deadpool       | ✅ Success           |
| Cross-Team Communication   | ✅ Routed via Router |

---

## 🐞 Battle Log (Real Issues Faced)

### ⚠️ VLAN Misconfiguration

* Ports were in default VLAN
* Fixed by assigning correct VLANs

---

### ⚠️ Trunk Failure

* One-side trunk configuration
* Fixed by enabling trunk on both ends

---

### ⚠️ Native VLAN Mismatch

* Caused CDP errors and traffic issues
* Fixed by aligning native VLAN

---

### ⚠️ Inter-VLAN Failure

* Missing default gateway
* Fixed by configuring router gateway on PCs

---

### ⚠️ Guardians Network Isolation 🛑

* Star-Lord & Groot couldn't communicate
* Root cause: VLAN/IP mismatch
* Resolved by correcting configuration

---

## 🧠 Key Learnings

* VLANs provide **logical segmentation**
* Trunks carry **tagged VLAN traffic**
* Router enables **cross-network communication**
* Default gateway is **critical**
* Troubleshooting is the **real skill**

---

## 🚀 Future Enhancements

* 🔐 ACL (Control which team can talk to whom)
* ⚡ DHCP (Automatic IP assignment)
* 🛡️ Security features (Port Security, DHCP Snooping)

---

## 📸 Proof of Work

* Topology Screenshot
* Configuration Files

---

## 🧑‍💻 Network Engineer

**Hari Krishnan**
*“From VLANs to Multiverse Routing 🌐”*
