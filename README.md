# 🧱 Lab 00 — Physical Infrastructure Foundations  
**Standalone Proof-of-Skill Project**

---

## 📌 Overview

This repository documents **Lab 00 — Physical Infrastructure Foundations**, a standalone, real-world focused project designed to prove competency in the **physical layer of IT infrastructure** — the domain where many of the most expensive and disruptive outages actually begin.

Unlike traditional networking labs that start at Layer 2 or Layer 3, this project focuses on the **foundational realities that exist before packets ever move**, including power, airflow, cabling, optics, and physical failure domains.

This lab is intentionally **not tied to any certification or simulator**.  
It reflects real-world reasoning used by network engineers, data center technicians, and infrastructure architects.

---

## 🎯 Purpose of This Lab

The goal of this project is to demonstrate the ability to:

- Reason about infrastructure failures **below the network layer**
- Design and document physical layouts used in enterprise environments
- Understand how physical decisions impact network stability
- Communicate infrastructure decisions clearly and professionally
- Produce artifacts used in real operational environments

This lab answers a critical question:

> *“Do you understand what can break a network before configuration is even involved?”*

---

## 🧠 Why This Lab Exists

Most networking education focuses on:
- VLANs
- Routing protocols
- IP addressing
- CLI configuration

However, in real environments:
- Power loss
- Poor airflow
- Incorrect optics
- Bad labeling
- Cabling mistakes

…are often the **true root cause** of outages.

This project exists to prove awareness of those realities.

---

## 🔍 Scope of the Project

This lab focuses on the following physical infrastructure domains:

### 1️⃣ Rack Layout & Airflow
- Equipment placement
- Heat management
- Hot aisle / cold aisle concepts
- Cable management considerations

### 2️⃣ Power Redundancy
- A/B power feeds
- UPS concepts
- Failure scenarios
- Single points of failure

### 3️⃣ Copper vs Fiber Decisions
- Distance considerations
- Speed requirements
- EMI susceptibility
- Cost and handling tradeoffs

### 4️⃣ Optics Selection
- SFP / SFP+ / QSFP use cases
- Multimode vs single-mode
- Link compatibility
- Common failure scenarios

### 5️⃣ Cable Labeling & Documentation
- Labeling standards
- Consistency and clarity
- Troubleshooting efficiency
- Human error reduction

### 6️⃣ Failure Cascade Simulation
- Power → switch → routing → outage
- Root cause vs symptom analysis
- Documentation of incident progression

---

## 📂 Repository Structure

