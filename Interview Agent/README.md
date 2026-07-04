# Interview Agent

## Overview
The Interview Agent is responsible for simulating dynamic, adaptive technical interviews. It reads the candidate's profile and the job description to generate relevant, probing questions on the fly, mimicking a real human recruiter.

## Inputs
- **Candidate JSON**
- **JD JSON**
- **Interview History** (Optional list of previous questions and answers)

## Outputs
- **Next Question**: A targeted question string tailored to the candidate's experience and the role's requirements.

## Dependencies
- `google-generativeai`

## Usage
```python
from interview_agent import generate_question

next_q = generate_question(candidate_json, jd_json, history)
print(next_q)
```
