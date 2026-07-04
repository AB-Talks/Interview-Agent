# Memory Agent

## Overview
The Memory Agent maintains long-term context across an interview. It updates a living "Memory JSON" state after every question, keeping track of demonstrated skills, weak areas, and topics that need follow-up.

## Inputs
- **Previous Memory State**
- **Latest QA Evaluation**

## Outputs
- **Updated Memory State**

## Usage
```python
from memory_agent import update_memory

new_memory = update_memory(old_memory, latest_eval)
```
