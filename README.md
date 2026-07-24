# AB Talks AI Agents

> **Open-source AI agents built by the AB Talks community for recruitment, interview preparation, and practical AI workflows.**

<p align="center">
  <b>Build. Learn. Contribute.</b>
</p>

## Why this project?

This repository contains modular AI agents developed as part of the AB Talks AI Challenge.

Each agent solves a specific task and can be reused independently or combined into larger AI workflows. We believe in practical, open-source AI development where each component is clean, self-contained, and easy to understand.

## Available Agents

| Agent | Purpose |
| --- | --- |
| **Resume Parser** | Extracts structured data from messy PDFs |
| **JD Parser** | Transforms raw job descriptions into precise requirements |
| **Readiness Match** | Compares candidates against role schemas to find gaps |
| **Interview Agent** | Simulates dynamic, adaptive technical interviews |
| **Judge Agent** | Evaluates interview responses against scoring rubrics |
| **Planner Agent** | Formulates interview and study roadmaps |
| **Report Agent** | Compiles QA history into final evaluation insights |
| **Memory Agent** | Maintains long-term context across workflows |

## Workflow

```text
Resume
      ↓
Resume Agent

Job Description
      ↓
JD Agent

      ↓
      
Readiness Match

      ↓

Interview

      ↓

Judge

      ↓

Final Report
```

## Getting Started

1. **Clone the repository:**
   ```bash
   git clone https://github.com/abtalks/AI-Agents.git
   cd AI-Agents
   ```

2. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run an Agent:**
   ```bash
   python "Interview Agent"/interview_agent.py
   ```

## Example Use Cases
- Candidate Screening
- Resume and Job Description Parsing
- Mock Interviews
- Skill Gap Analysis

## Future Agents
- ⬜ Resume Optimizer
- ⬜ ATS Simulator
- ⬜ Career Coach
- ⬜ Salary Negotiator

## How to Distribute & Use in Other Projects

Since these agents are built to be modular, you might want to integrate them into another application (like the AB Talks main platform). Here are the recommended ways to do so:

### Option 1: Install from GitHub (Recommended)

If the agents are structured as Python packages, the easiest way to integrate them is by installing directly from GitHub.

```bash
# Example for installing a specific agent repository
pip install git+https://github.com/AB-Talks/Interview-Agent.git
```

In your application code, you can then import the agent directly:

```python
from interview_agent import InterviewAgent

agent = InterviewAgent()
```
*Note: If the agent doesn't expose a clean public API (like `InterviewAgent` class) yet, we are working on designing a standardized entry point for each package.*

### Option 2: Git Submodule

You can add this repository as a submodule to your main project.

```text
Your-App/
├── backend/
├── frontend/
└── agents/
    └── Interview-Agent/
```

- **Pros:** Always pulls the latest changes; single source of truth.
- **Cons:** Git submodules can be tricky to manage.

### Option 3: Private PyPI (Best Long-Term)

Eventually, we plan to publish these agents as proper packages (e.g., `abtalks-interview-agent`). Once published, you can simply run:

```bash
pip install abtalks-interview-agent
```

---

## How to Test Without Installing & Demos

You don't need to install the project as a package just to try it out. You can run the scripts directly from the cloned repository.

### Running a Demo

To see a proper working demo of the agent, you can run the main agent script directly. For example, to test the Interview Agent:

```bash
python "Interview Agent"/interview_agent.py
```

This script will run the agent in your terminal, allowing you to interact with it and see its capabilities without any complex setup. 

Additionally, you can explore the `playground/` directory which contains interactive UI demos (like `index.html`) to visualize how these agents can be integrated into web applications.

## Contributing
See [CONTRIBUTING.md](CONTRIBUTING.md) for details. In short:
1. Fork the repo
2. Create a branch
3. Commit your changes
4. Open a Pull Request

## License
MIT License. See [LICENSE](LICENSE) for details.
