# Report Agent

## Overview
The Report Agent compiles the entire QA history and telemetry from an interview session into a comprehensive, readable summary. It highlights candidate strengths, weaknesses, and a final hire/no-hire recommendation.

## Inputs
- **QA History Array**
- **Evaluation Memory**

## Outputs
- **Final Report JSON**

## Usage
```python
from report_agent import generate_report

report = generate_report(qa_history, memory)
```
