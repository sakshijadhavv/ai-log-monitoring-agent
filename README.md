# ai-log-monitoring-agent
AI Log Monitoring &amp; Alert Triage Agent — Built a LangChain-based AI agent that analyzes application logs, classifies alert severity, identifies probable root causes, and recommends remediation steps, reducing manual log-review effort.


## Architecture

```mermaid
flowchart TD

    A[Applications<br/>Kubernetes / EC2]
    B[Application Logs]
    C[Log Collector]
    D[Alert Detector]
    E[LangChain AI Agent]

    F[Log Analysis]
    G[Kubernetes Investigation]
    H[Metrics Investigation]

    I[Incident Analysis]
    J[Severity Classification]
    K[Root Cause Analysis]
    L[Remediation Recommendation]

    M[Slack]
    N[Jira]
    O[Email]

    A --> B
    B --> C
    C --> D
    D --> E

    E --> F
    E --> G
    E --> H

    F --> I
    G --> I
    H --> I

    I --> J
    I --> K
    I --> L

    I --> M
    I --> N
    I --> O
```


Agent:

1. Search recent logs
2. Detect repeated database timeout
3. Check Kubernetes pod status
4. Detect CrashLoopBackOff
5. Inspect pod logs
6. Detect OOMKilled
7. Check recent deployment
8. Determine probable cause
9. Generate incident summary
10. Send Slack notification
