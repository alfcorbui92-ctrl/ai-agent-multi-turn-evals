# AI Agent Multi-Turn Evaluations

This repository contains multi-turn evaluation tasks designed to assess how AI agents behave inside simulated digital environments.

The evaluations focus on conversational reasoning, context retention, action safety, and decision-making across extended interactions.

## Evaluation Areas

The repository evaluates whether AI agents can:

- Maintain context across multiple turns
- Handle follow-up requests correctly
- Adapt to changing goals
- Process user corrections
- Decide when to act vs when to ask for clarification
- Avoid unsafe or irreversible actions without confirmation
- Perform safe intermediate reasoning before yielding

## Repository Structure

ai-agent-multi-turn-evals/
│
├── README.md
│
├── personas/
│   ├── founders/
│   ├── managers/
│   ├── interns/
│   └── researchers/
│
├── trajectories/
│   ├── terminal/
│   ├── airline/
│   └── retail/
│
├── rubrics/
│
├── worlds/
│
├── analyses/
│
└── results/

## Simulated Environments

Tasks are designed around lightweight fictional digital environments using combinations of:

- Terminal workspaces
- Gmail
- Notes and Lists
- Calendar systems
- Airline workflows
- Retail purchasing systems

The complexity is centered on the conversation rather than the environment itself.

## Core Multi-Turn Skills

### Maintaining Context
The agent must preserve constraints, preferences, and prior information across multiple turns without requiring repetition.

### Goal Switching
The user changes objectives mid-conversation, requiring the agent to adapt while preserving relevant context.

### Follow-Up Reasoning
The agent must correctly interpret vague references to previous outputs or actions.

### User Corrections
The user modifies or overrides previous instructions, requiring the agent to discard outdated assumptions.

## Decision Framework

- ACT → proceed when all required information is available  
- YIELD → request clarification before irreversible or ambiguous actions  
- ACT→YIELD → perform safe intermediate steps before asking for confirmation  

## Evaluation Components

- Persona definition  
- World design  
- Multi-turn trajectory  
- ACT/YIELD reasoning analysis  
- Rubric criteria  
- Model comparison analysis  
- Failure analysis  

## Purpose

The goal is to understand how AI agents behave in realistic multi-turn scenarios where memory, reasoning, and decision-making are required.
