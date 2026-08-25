# AI Password Security Analyzer

## Overview

AI Password Security Analyzer is an n8n-based AI workflow designed to analyze a password and generate a structured security assessment. The workflow visibly produces a security level or verdict, a security score, a risk level, and a summary of the assessment.

## How It Works

1. **When chat message received** starts the workflow when a user provides input through chat.
2. **Analyze Password Strength** processes the password or input and prepares password-strength information.
3. **Basic LLM Chain** uses the connected **OpenAI Chat Model** to analyze the password security information.
4. **Parse Password Security Result** processes and parses the generated security result.
5. **Basic LLM Chain1** uses the connected **OpenAI Chat Model1** to generate the final password security report.
6. The final output is returned as a structured password security report.

## Workflow Architecture

```text
User Chat Message
        |
        v
Analyze Password Strength
        |
        v
Basic LLM Chain
        |
        v
Parse Password Security Result
        |
        v
Basic LLM Chain1
        |
        v
Password Security Report
```

The **OpenAI Chat Model** and **OpenAI Chat Model1** nodes are connected to their respective LLM Chain nodes as AI models. They are model connections, not separate sequential workflow steps.

## Security Assessment Output

The visible result fields include:

- **Verdict / Security Level**
- **Security Score**
- **Risk Level**
- **Summary**

The screenshot shows the following example result:

- Verdict: **Very Strong**
- Security Score: **95/100**
- Risk Level: **Low**

These values are shown as an example from one workflow execution and are not guaranteed for every password.

## AI-Powered Analysis

OpenAI is used through the LLM Chain nodes to interpret the password-strength information and generate the security assessment and final report. The exact AI prompts and scoring algorithm are not visible in the workflow screenshot, so they are not specified here.

## Key Features

- Chat-based password analysis
- Password strength analysis
- AI-powered security assessment
- Security score
- Risk-level classification
- Structured password security report
- n8n workflow automation
- OpenAI integration

## Technologies & Integrations

| Technology / Node | Purpose |
| --- | --- |
| n8n | Hosts and orchestrates the automation workflow. |
| OpenAI | Provides the chat models connected to the LLM Chain nodes. |
| Chat Trigger | Starts the workflow when a chat message is received. |
| JavaScript / Code | Represents the code-style workflow nodes used to analyze password strength and parse the security result. |
| Basic LLM Chain | Uses a connected AI model to analyze information and generate the security report. |

## Use Cases

- Password strength assessment
- Security awareness
- AI-assisted password evaluation
- Automated security reporting

This workflow is intended as an analysis and reporting tool. It does not provide complete cybersecurity protection or guarantee password security.

## Workflow Screenshot

![AI Password Security Analyzer](AI%20Password%20Security%20Analyzer.png)

## Security Note

Real passwords and sensitive credentials should not be exposed or stored unnecessarily. API keys and credentials must never be committed to GitHub. Manage them through secure credential storage instead.

## Conclusion

This project demonstrates how n8n and AI can be combined to automate password-strength analysis and generate structured security assessments through a chat-based workflow.
