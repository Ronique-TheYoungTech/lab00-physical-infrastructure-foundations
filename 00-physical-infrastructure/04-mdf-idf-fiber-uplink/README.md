# Lab 04 – MDF ↔ IDF Design (Fiber Uplink)

## Objective
Design and document a **building-scale physical distribution architecture** by extending an existing **Main Distribution Frame (MDF)** to an **Intermediate Distribution Frame (IDF)** using a **fiber uplink**.

This lab demonstrates correct use of fiber for inter-closet connectivity, proper separation of MDF and IDF roles, and enterprise-standard Layer 1 documentation practices.

---

## Scope & Design Intent
This lab focuses strictly on **physical infrastructure (Layer 1)** and intentionally excludes all logical configuration.

The design proves:
- How networks scale beyond a single wiring closet
- Why fiber is used between distribution frames
- How MDFs and IDFs are physically and functionally separated
- How horizontal cabling is localized to the serving IDF

---

## Diagram Reference

- **Primary Reference (Screenshot):**  
  `./screenshots/mdf-idf-fiber-uplink.png`

- **Source Diagram (Editable):**  
  `./04-mdf-idf-fiber-uplink.drawio`

---

## Physical Topology Overview

**High-Level Flow:**

```bash
[MDF]
ISP Modem / ONT
Edge Router / Firewall
Patch Panel (PP1 – 48 Port)
Access Switch (SW1 – 48 Port)
↓
Fiber Uplink (MMF)
↓
[IDF]
Patch Panel (IDF-PP1 – 24 Port)
Access Switch (IDF-SW1 – 24 Port)
Horizontal Cabling → Floor-Level End Devices
```

This reflects standard enterprise building distribution architecture.

---

## Cabling Breakdown

### 1. MDF Internal Cabling
- **Edge Router → Patch Panel**
  - Cable Type: Cat6 Patch Cable  
  - Label: `Edge LAN → PP1 Port 1`

- **Patch Panel → MDF Access Switch**
  - Cable Type: Cat6 Patch Cable  
  - Label: `PP1 Port 1 → SW1 Port 1`

**Purpose:**  
Maintains clean termination, serviceability, and flexibility within the MDF.

---

### 2. MDF ↔ IDF Distribution Link
- **Cable Type:** Multi-Mode Fiber (MMF)
- **Label:**  
  `Fiber Uplink (MMF) – MDF-SW1 → IDF-PP1`

**Reasoning:**
- Fiber supports longer distances between closets
- Immune to electromagnetic interference
- Standard practice for inter-floor or inter-wing distribution
- Separates distribution from access cabling

---

### 3. IDF Internal Cabling
- **Patch Panel → IDF Access Switch**
  - Cable Type: Cat6 Patch Cable  
  - Label: `IDF-PP1 Port 1 → IDF-SW1 Port 1`

**Purpose:**  
Maintains the same passive-to-active discipline used in the MDF.

---

### 4. IDF Horizontal Cabling
- **Example Horizontal Run:**
  - Cable Type: Cat6 Horizontal Run  
  - Label: `IDF-SW1 Port 10 → Floor 2 Office Drop B-01`

**Notes:**
- Only one representative run is shown
- End devices are implied, not exhaustively drawn
- Prevents diagram clutter while proving standards compliance

---

## Why Horizontal Cabling Terminates at the IDF
In enterprise environments:
- Horizontal copper runs are limited in distance
- IDFs serve localized areas (floors, wings, zones)
- MDFs do not directly serve endpoint drops

This design ensures scalability, performance, and maintainability.

---

## Design Principles Demonstrated
- Clear physical separation of MDF and IDF roles
- Proper use of fiber for distribution
- Copper restricted to patching and horizontal runs
- Passive vs active infrastructure discipline
- Enterprise documentation clarity

---

## Tools Used
- **draw.io / diagrams.net** – Physical infrastructure diagramming

---

## Files
```bash
04-mdf-idf-fiber-uplink/
├── 04-mdf-idf-fiber-uplink.drawio
├── screenshots/
│ └── mdf-idf-fiber-uplink.png
└── README.md
```

---

## Real-World Relevance
This architecture aligns with:
- Corporate office buildings
- Schools and campuses
- Hospitals and clinics
- Multi-floor commercial environments

The design scales cleanly into:
- Additional IDFs
- Redundant fiber uplinks
- Core/distribution layer architectures

---

## Lab Status
**Status:** Complete  
**Phase:** CAINO – Physical Infrastructure  
**Diagram State:** Frozen (no further modifications)

---

## Phase Transition
With this lab complete:

✅ **Physical Infrastructure Phase CLOSED**  
➡️ Transition to **Phase 2 – Logical Network Design**

Upcoming focus:
- VLAN design
- Access vs trunk ports
- Inter-VLAN routing
- Logical topology documentation

---


