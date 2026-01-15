# Lab 03 – Cabling Infrastructure (MDF)

## Objective
Design and document a professional **Layer 1 cabling infrastructure** for a small enterprise **Main Distribution Frame (MDF)**, demonstrating correct separation of ISP demarcation, security, passive termination, active switching, and horizontal cabling.

This lab focuses strictly on **physical infrastructure design**, not logical configuration.

---

## Scope & Design Intent
This diagram represents how enterprise networks are **physically cabled and terminated** inside an MDF:

- ISP handoff enters the building
- Traffic is secured at the edge
- Cabling is terminated on a patch panel
- Active switching connects to horizontal runs
- End devices are implied, not exhaustively drawn

The goal is **clarity, serviceability, and scalability**.

---
## Diagram Overview
The following overview describes the physical cabling flow shown in  
![Cabling Infrastructure – MDF](/screenshots/03-cabling-infrastructure.png)



**Topology Flow (Top-Down):**
```bash
ISP Modem / ONT
↓
Edge Router / Firewall
↓
Patch Panel (PP1 – 48 Port)
↓
Access Switch (SW1 – 48 Port)
↓
Horizontal Cabling → Office Drops / End Devices
```


---

## Real-World Relevance
This cabling model aligns with:
- Corporate offices
- Clinics and hospitals
- Schools and campuses
- Small to mid-size enterprise environments

The design scales cleanly into:
- IDF expansion
- Fiber uplinks
- Redundant switching
- Structured cabling standards (TIA/EIA)

---

## Lab Status
**Status:** Complete  
**Phase:** CAINO – Physical Infrastructure  
**Diagram State:** Frozen (no further modifications)

---

## Next Steps
- IDF design with fiber uplink
- Rack elevation diagram
- Port schedule documentation
- Logical network topology (VLANs, routing)

---

