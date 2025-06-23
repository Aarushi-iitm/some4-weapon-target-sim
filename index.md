---
title: "Target Acquired: A Discrete Math Showdown Between Humans and Algorithms"
layout: default
---
# 🎯 Target Acquired: A Discrete Math Showdown Between Humans and Algorithms

Imagine a high-stakes defense scenario: enemy drones, missiles, and combat aircraft are rapidly approaching. You have a limited arsenal—three powerful weapons—but each is only partially effective against different targets. What’s your move?

This blog explores the power of **discrete mathematics** in tactical decision-making. Can human intuition outmatch a mathematical model in neutralizing threats?

---

## 🚀 Problem Setup

We consider three types of **weapons** and **aerial targets**:

|            | UAV (Drone) | Missile | Combat Aircraft |
|------------|-------------|---------|------------------|
| Missile    | 0.8         | 0.6     | 0.3              |
| Laser      | 0.4         | 0.3     | 0.9              |
| EMP        | 0.9         | 0.2     | 0.2              |

Each cell represents the **probability** of success if a weapon is used against a specific target.

🔒 **Constraints**:
- Each weapon can be used only once
- Each target can be engaged only once
- Some weapons are ineffective against certain targets

---

## 🎮 Manual Mode: Human Intuition

You play the game by selecting which weapon to assign to each threat.

🔍 **Example**:
- EMP → UAV  
- Missile → Missile  
- Laser → Combat Aircraft

Success depends on how well you match types based on your instincts.

> 📌 **Pigeonhole Principle in Action**:  
> When you have more targets than weapons, some threats *must* get through. Choose wisely!

---

## 🤖 Mathematical Mode: Optimization Strategy

We define the problem using discrete math:

- Let `x_ij = 1` if weapon `i` is assigned to target `j`, otherwise 0
- Let `P_ij` be the success probability
- Maximize total expected success:  
  **maximize** ∑∑ `P_ij * x_ij`

🔧 Subject to:
- Each weapon assigned to at most one target
- Each target assigned to at most one weapon
- Some `x_ij` are restricted (e.g., EMP → Missile = 0)

📊 Represented as a **bipartite graph** (weapons ↔ targets), solved with max-weight matching.

> 🕸 **Graph Theory Spotlight**:  
> This is a classic bipartite matching problem with weighted edges!

---

## 🧠 Discrete Math Insights

| Concept                     | Application                          |
|----------------------------|--------------------------------------|
| Pigeonhole Principle       | Limited weapons vs. multiple threats |
| Constraint Satisfaction    | Weapon-target compatibility          |
| Bipartite Graph Matching   | Optimal assignment                   |
| Probability Theory         | Expected outcome computation         |

Each mathematical idea powers the logic behind the model—and helps explain why some intuitive moves fail.

---

## 🆚 Human vs. Model: The Showdown

We tested both approaches under identical scenarios:

| Metric                  | Human Player | Mathematical Model |
|-------------------------|--------------|--------------------|
| Targets Neutralized     | 5/9          | 8/9                |
| Weapon Efficiency       | 60%          | 90%                |
| Constraint Violations   | 2            | 0                  |

> ✅ The model consistently outperforms manual play, especially as complexity increases.

---

## 🧩 Reflection

This project taught us that:
- Discrete math is *not just theory*—it’s a tactical toolkit.
- Optimization models can support or correct human instincts.
- Visualizing constraints leads to better real-world decisions.

> “When every second counts, logic wins over luck.”

---

## 🔗 Try the Simulation (coming soon!)

[🔫 Play the Game](./game/index.html)  
Compare your choices with the optimal strategy!

---

## 🛠️ Credits

Developed as part of **IIT-GN’s Discrete Mathematics** course for the [Summer of Math Exposition (SoME4)](https://summerofmath.com/).

Project by: Aarushi Ahlawat  
GitHub Repo: [some4-weapon-target-sim](https://github.com/aarushi-iitm/some4-weapon-target-sim)

---
