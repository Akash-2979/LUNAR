# 🌙 LUNAR: Safe Navigation and Landing on the Moon

### 🚀 Physics-Driven Lunar Landing Simulator | Python | Pygame | AI & Computer Vision Integration

---

## 🧠 Overview

**LUNAR** is a **physics-based lunar landing and navigation simulator** that models descent dynamics, thrust control, and terrain hazards under realistic lunar conditions.  
The project aims to simulate **autonomous safe landing** using a multi-phase strategy — from rough braking to fine descent — ensuring a soft touchdown even on uneven surfaces.

This project lays the groundwork for **AI-integrated safe navigation**, combining **realistic physics, terrain generation, and intelligent landing algorithms**.  
It also proposes future extensions using **Chandrayaan-2 imagery, U-Net segmentation, and reinforcement learning (RL)** to train autonomous rovers and landers.

---

## ✨ Features

- 🧩 **Physics-driven simulation** — Realistic gravity, thrust, velocity, and fuel consumption modeling.
- 🧠 **Autonomous landing logic** — Implements three key stages:  
  - **Rough Braking Phase**
  - **Fine Braking Phase**
  - **Final Touchdown Phase**
- 🌑 **Procedural terrain generation** — Random craters and boulders dynamically generated each run.
- 🎯 **Real-time feedback** — Displays altitude, fuel, and velocity for live status tracking.
- 💥 **Crash vs Safe detection** — Determines if landing conditions (speed, angle, and position) are safe.
- 🛰️ **Scalable AI roadmap** — Integration with Chandrayaan-2 datasets and YOLOv5 + U-Net for hazard segmentation.
- 🧭 **RL Agent Simulation (Future)** — Training RL-based landing agents to learn optimal trajectories autonomously.

---

## 🧩 Tech Stack

| Category | Technologies |
|-----------|---------------|
| **Language** | Python |
| **Framework / Library** | Pygame |
| **Physics Engine** | Custom gravity, thrust, and collision models |
| **AI / ML (Future)** | YOLOv5, U-Net, Reinforcement Learning |
| **Data Source (Future)** | Chandrayaan-2 IIRS and OHRC datasets |

---

## 🏗️ System Architecture

```

┌───────────────────────────┐
│      LUNAR Simulator      │
│  (Main Pygame Engine)     │
└────────────┬──────────────┘
│
▼
┌───────────────────────────┐
│  Physics Engine Module    │
│ Gravity | Thrust | Fuel   │
└────────────┬──────────────┘
│
▼
┌───────────────────────────┐
│  Terrain Generator        │
│ Randomized Craters & Rock │
└────────────┬──────────────┘
│
▼
┌───────────────────────────┐
│  AI Extension Layer       │
│ YOLOv5 | U-Net | RL Agent │
└───────────────────────────┘

````

---

## 🖥️ Setup Instructions

### 1️⃣ Clone the repository
```bash
git clone https://github.com/Akash-2979/LUNAR.git
cd LUNAR
````

### 2️⃣ Install dependencies

```bash
pip install pygame numpy opencv-python
```

### 3️⃣ Run the simulator

```bash
python main.py
```

### 4️⃣ Controls

* **↑ (Up Arrow)** → Thrust upward
* **← / → (Left / Right)** → Adjust landing direction
* **Fuel is limited**, so plan descent efficiently!

---

## 🧮 Simulation Parameters

| Parameter          | Description                      | Default   |
| ------------------ | -------------------------------- | --------- |
| Gravity            | Lunar gravity in m/s²            | 1.62      |
| Max Thrust         | Engine thrust capacity           | 5 units   |
| Initial Fuel       | Fuel available at start          | 100 units |
| Safe Landing Speed | Maximum speed for safe touchdown | < 2.0 m/s |

---

## 📊 Output Example

A typical run outputs:

```
Landing Velocity: 1.73 m/s
Fuel Remaining: 12.4 units
Status: ✅ SAFE LANDING
```

Or in case of crash:

```
Landing Velocity: 3.58 m/s
Fuel Remaining: 4.7 units
Status: 💥 CRASHED
```

---

## 🧠 Future Work

* Integration of **Chandrayaan-2 imagery** for realistic surface simulation.
* Implementation of **YOLOv5 & U-Net** for hazard segmentation.
* Training **Reinforcement Learning (RL)** agents to optimize descent strategies.
* Visualization of safe navigation paths in **Three.js** 3D surface.

---

## 📚 References

* **Silberschatz et al.** – Operating System Concepts (CPU Scheduling foundations)
* **ISRO Chandrayaan-2 Dataset** – For real lunar surface imaging
* **NASA Apollo Mission Logs** – For lunar descent physics modeling

