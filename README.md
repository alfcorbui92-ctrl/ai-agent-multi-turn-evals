# AI Agent Multi-Turn Evaluation Project

## Overview

This repository contains structured evaluations of AI agents operating inside simulated enterprise environments.

The core objective is to test how well AI systems handle complex, multi-turn decision-making tasks that involve changing constraints, tool use, and evolving user intent.

The project is designed around the creation of **synthetic digital worlds**, where an AI agent must interact with applications, follow workflows, and make safe and correct decisions under ambiguity.

---

## Core Concept: The Simulated World

Each evaluation task is built around a **fictional but realistic digital environment ("world")**.

A world contains:

### 1. 👤 Persona
A synthetic user with:
- A role (e.g. founder, employee, traveler, operator)
- A goal (what they are trying to accomplish)
- A realistic context (time pressure, business constraints, urgency)

---

### 2. 🧩 Applications (Environment)

Each world includes:

#### Primary Application
The main system where the core task happens, such as:
- Terminal (file system / code execution)
- Airline (flight booking system)
- Retail (purchases / orders)

#### Secondary Applications
Supporting systems that introduce realism and cross-system dependency, such as:
- Gmail (email communication)
- Notes / Lists (task tracking)
- Documents (structured information storage)
- Calendar (scheduling)

These applications form a **multi-system environment** where the agent must navigate between tools.

---

## 🧪 Task Structure

Each task follows a structured evaluation pipeline:

### Step 1 — World Creation
A full simulated environment is defined, including:
- Persona
- Applications
- Data artifacts (files, emails, bookings, etc.)
- Initial state of the system

---

### Step 2 — Golden Trajectory Design

Before running any model, a **golden trajectory** is defined.

This is a step-by-step ideal conversation that includes:

- Multi-turn user prompts
- Expected agent behavior
- Decision points (ACT / YIELD / ACT→YIELD)
- Expected tool usage
- Skill being tested per turn

The trajectory must explicitly follow evaluation rubrics.

---

### Step 3 — Evaluation Rubrics

Each task includes a rubric used to evaluate success.

Rubrics define:
- What the agent must do in each turn
- What data it must retrieve or modify
- What decisions it must make
- Whether it should ACT, YIELD, or ACT→YIELD

At least one rubric item must:
- Reference a specific entity (file, email, booking, ID, etc.)
- Evaluate a decision point, not just output text

---

### Step 4 — Run 1 (Failure Run)

The first model run is used to test whether the task is sufficiently challenging.

The goal is to intentionally design a world where the agent fails in at least one of the following ways:

- ❌ Acts when it should YIELD
- ❌ Fails to act when it should proceed
- ❌ Takes an incorrect action
- ❌ Produces incorrect or inconsistent information

If the agent does not fail, the task is considered too easy and must be redesigned.

---

### Step 5 — Run 2 (Golden Trajectory)

The second run follows the same scenario but is guided toward the correct behavior.

During this run:
- The agent should follow the golden trajectory
- If it deviates, the user may introduce **HINTS** to redirect behavior
- Hints are corrective instructions, not new tasks
- Hints must be used sparingly and only to recover correct trajectory alignment

The goal is for the agent to successfully pass all evaluation rubrics.

---

## 🧠 Key Skills Being Evaluated

This project measures agent performance across:

- Multi-turn reasoning consistency
- Context retention across long interactions
- Goal switching between workflows
- Handling of user corrections
- Decision discipline (ACT vs YIELD behavior)
- Safe tool usage under ambiguity
- Cross-application coordination

---

## ⚠️ Failure Conditions

A task is considered successful in design only if Run 1 produces at least one failure case.

Common failure modes include:
- Premature execution without full constraints
- Ignoring updated user corrections
- Losing context across turns
- Incorrect tool selection or sequencing

---

## 🎯 Final Objective

By the end of Run 2, the AI agent must:
- Correctly follow the multi-turn structure
- Respect all rubrics
- Handle corrections and pivots
- Successfully complete all required actions across applications
- Maintain consistent reasoning across the entire trajectory

---

## 🛡️ Safety Note

All environments are fully simulated and synthetic.
No real systems, credentials, or external services are impacted.

This project exists solely for AI evaluation and safety research purposes.
