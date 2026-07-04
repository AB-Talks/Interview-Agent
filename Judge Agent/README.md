# Judge Agent

## Overview
The Judge Agent evaluates interview responses against predefined scoring rubrics. It provides a granular breakdown of the candidate's answer quality, including depth, accuracy, and communication skills.

## Inputs
- **Question**: The question asked by the Interview Agent.
- **Answer**: The candidate's response.
- **Telemetry Signals**: Optional metrics like latency, word count, and filler words.

## Outputs
- **Evaluation JSON**:
  - `accuracy`
  - `depth`
  - `communication`
  - `problemSolving`
  - `starFramework` (bool values for Situation, Task, Action, Result)

## Dependencies
- `google-generativeai`

## Usage
```python
from judge_agent import evaluate_answer

eval_result = evaluate_answer("How do you optimize React?", "I use useMemo...", telemetry)
print(eval_result)
```
