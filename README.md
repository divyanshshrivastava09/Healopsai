# ResolveAI — Self-Healing AI Automation System

**Detect failures. Diagnose problems. Recover intelligently.**

ResolveAI is an AI-assisted customer support and self-healing automation platform designed to detect API failures, identify potential causes, and support automated recovery through controlled repair and verification workflows.

The project combines customer support functionality with API monitoring and intelligent error handling to demonstrate how software systems can become more resilient, reduce manual intervention, and improve service reliability.

## 🚀 Key Features

- **Customer Support Interface:** Provides a user-facing interface for customer queries and support-related operations.
- **API Health Monitoring:** Tracks API behavior and displays service health and failure information.
- **Error Detection:** Identifies simulated or encountered API failures, such as timeouts, server errors, and schema mismatches.
- **AI-Assisted Diagnosis:** Uses AI, where configured, to analyze error information and suggest possible causes or recovery actions.
- **Self-Healing Workflow:** Supports controlled recovery actions, such as retries or predefined repairs, depending on the implemented functionality.
- **Recovery Verification:** Checks whether a recovery attempt succeeded instead of assuming that the issue is resolved.
- **Incident History:** Records detected errors, diagnosis details, attempted actions, and recovery outcomes.
- **Failure Simulation:** Enables testing with controlled errors to demonstrate the system’s detection and recovery workflow.

## 🎯 Problem Statement

Modern customer-support applications often depend on multiple APIs and backend services. When one of these services fails, users may experience interrupted workflows, unsuccessful requests, and delays in receiving support.

Diagnosing these failures manually can consume time and require developer intervention.

ResolveAI addresses this challenge by demonstrating a workflow that combines failure detection, AI-assisted diagnosis, controlled recovery, and post-recovery verification.

## 💡 Our Solution

ResolveAI follows a structured self-healing process:

1. **Detect:** Identify an API failure or unexpected response.
2. **Diagnose:** Analyze error details and determine a likely cause.
3. **Validate:** Check whether a proposed recovery action is safe to execute.
4. **Recover:** Perform an approved repair, retry, or other supported recovery action.
5. **Verify:** Check the result to determine whether the service has recovered.
6. **Record:** Store the incident and recovery outcome for monitoring and analysis.

This workflow helps distinguish between simply reporting an error and actively attempting to recover from it.

## 🏗️ System Architecture

The platform can be understood through the following components:

- **Frontend:** Customer support interface and administrative dashboard.
- **Backend API:** Handles application requests and coordinates system operations.
- **Monitoring and Error Detection:** Captures failures and unexpected API responses.
- **AI Diagnosis Layer:** Analyzes error information and proposes explanations or recovery actions.
- **Recovery Engine:** Executes supported, validated recovery procedures.
- **Verification Layer:** Checks whether the attempted recovery was successful.
- **Logging and History:** Maintains incident records and recovery results.
- **Failure Simulator:** Generates controlled failures for testing and demonstrations.

### Workflow

```text
Customer / Admin
       |
       v
  Frontend UI
       |
       v
   Backend API
       |
       v
 Request Monitoring
       |
       v
  Error Detected
       |
       v
 AI-Assisted Diagnosis
       |
       v
 Validate Recovery Action
       |
       v
 Execute Safe Recovery
       |
       v
 Verify Service Health
       |
       v
 Record Recovery Outcome
```

If recovery fails, the system should record the failure and escalate the issue instead of retrying indefinitely.

## 🧪 Example Failure Scenarios

ResolveAI can be tested with controlled failure scenarios, depending on the integrations implemented.

| Scenario | Example | Expected handling |
|---|---|---|
| API timeout | A service takes too long to respond | Detect the timeout and apply a bounded retry if appropriate |
| HTTP 500 | A backend service returns an internal server error | Record the failure, diagnose the issue, and attempt an approved recovery |
| Schema mismatch | An API returns a string where a numeric value is expected | Identify the validation error and suggest or apply a validated correction |
| Recovery failure | The service remains unavailable after a repair attempt | Record the unsuccessful attempt and escalate the issue |

These scenarios help demonstrate how the system responds to failures and how recovery outcomes are verified.

## 🛠️ Technology Stack

Update this section to reflect the technologies actually used in your implementation.

- **Frontend:** React, HTML, CSS, or the framework used by the project
- **Backend:** Python and FastAPI, if configured
- **Data Storage:** SQLite or the database used by the project
- **AI Integration:** The configured LLM provider and model, if implemented
- **Validation:** Pydantic or another validation mechanism, if used
- **Monitoring:** Application logs, API status checks, and error tracking
- **Version Control:** Git and GitHub

## ⚙️ Installation and Setup

### Prerequisites

Install the tools required by your project, such as:

- Git
- Node.js and npm, if the frontend uses React
- Python 3.10 or later, if the backend uses Python
- API credentials for any external services your project requires

### 1. Clone the repository

```bash
git clone <YOUR_REPOSITORY_URL>
cd <YOUR_PROJECT_FOLDER>
```

Replace the placeholders with your actual repository URL and folder name.

### 2. Set up the backend

If your backend uses Python and FastAPI:

```bash
python -m venv venv
```

Activate the environment.

**Windows:**

```bash
venv\Scripts\activate
```

**macOS/Linux:**

```bash
source venv/bin/activate
```

Install the dependencies listed in your project:

```bash
pip install -r requirements.txt
```

Start the backend using the entry point configured in your application. For example, if your entry file is `main.py`:

```bash
uvicorn main:app --reload
```

### 3. Set up the frontend

If your frontend uses npm:

```bash
cd frontend
npm install
npm run dev
```

Adjust the folder name and commands to match your actual project structure.

### 4. Configure environment variables

Create a `.env` file if your application requires API keys or configuration values.

Example:

```env
# Add only the variables your application actually uses
AI_API_KEY=your_api_key_here
BACKEND_URL=http://localhost:8000
```

Use the exact variable names expected by your code. Never commit real API keys, passwords, or other secrets to GitHub.

### 5. Open the application

Open the local URL displayed by your frontend development server. Ensure that the backend is running and that the frontend is configured to communicate with it.

## ▶️ How to Use

1. Launch the application.
2. Explore the customer-support interface.
3. Open the administrative dashboard, if available.
4. Review API health indicators and incident information.
5. Trigger a supported failure scenario using the failure simulator.
6. Observe the detected error and its diagnosis.
7. Review or initiate the available recovery action.
8. Check the verification result and incident history.

The exact steps depend on the features enabled in your implementation.

## 🔐 Safety and Reliability

Self-healing automation must be controlled and verifiable. ResolveAI's intended design principles include:

- Validate recovery actions before execution.
- Use bounded retries to avoid retry loops.
- Restrict automated changes to approved operations.
- Require human approval for high-risk changes.
- Record recovery attempts and their outcomes.
- Report success only after verification.

AI-generated diagnoses should be treated as suggestions unless independently validated. A successful diagnosis does not necessarily mean that a service has been repaired.

## 🎯 Use Cases

- Customer-support automation
- API failure detection and diagnosis
- Automated retry and recovery workflows
- Testing backend resilience
- Incident tracking and recovery analysis
- Demonstrations of AI-assisted operations

## 🔮 Future Enhancements

Potential improvements include:

- Real-time monitoring and alert notifications
- Integration with additional APIs and services
- More advanced root-cause analysis
- Configurable recovery policies
- Human approval workflows for sensitive repairs
- Metrics for recovery success rate and time to recovery
- Persistent incident analytics and reporting
- Deployment with production monitoring and access controls

## 🏆 Project Purpose

ResolveAI was developed as a project exploring the **Self-Healing AI Automation System** concept. It demonstrates how AI-assisted diagnosis can work alongside deterministic validation, controlled automation, and verification to improve application resilience.

## 👥 Contributors

- **Team:** Add your team name
- **Developers:** Add contributor names
- **Event:** Add hackathon name, if applicable

## 📄 License

Choose and add a license appropriate for your project before distributing it publicly.

---

**ResolveAI — From error detection to verified recovery.**
