# Final Summary – AI Agent Multi-Turn Evaluation

## Overview

This repository evaluates an AI agent operating in a simulated multi-turn enterprise environment focused on flight booking and communication workflows.

The system tests the agent’s ability to:
- Maintain context across turns
- Ask for clarification when required
- Apply user corrections
- Execute constrained multi-step tasks safely

---

## Failure Run (Run 1)

### Key Observation

In the first turn, the agent failed to correctly follow the expected decision logic.

Instead of **yielding and asking for missing information**, the agent attempted to continue searching for information.

### Expected Behavior (Turn 1)
- The agent should have recognized missing structured constraints
- The correct action was to **YIELD and ask clarification**

### Actual Behavior
- The agent proceeded to search for information
- It did not explicitly request missing details from the user

### Resulting Issue
- Early breakdown in ACT/YIELD decision boundary
- Incorrect initialization of shared context
- Compounded errors in later turns due to weak starting state

---

## Golden Run (Run 2)

Using structured hints, the second run successfully guided the agent toward:

- Correctly identifying missing information in Turn 1
- Maintaining updated constraints across turns
- Applying user corrections properly (date change in Paris leg)
- Enforcing flight time constraints (<11AM)
- Completing booking sequence correctly
- Handling final email communication task using consistent state
