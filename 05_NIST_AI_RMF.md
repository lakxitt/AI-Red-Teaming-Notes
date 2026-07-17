# 📘 NIST AI Risk Management Framework (AI RMF) – Detailed Notes

---

# What is NIST AI RMF?

The **NIST AI Risk Management Framework (AI RMF)** is a framework developed by the **National Institute of Standards and Technology (NIST)** to help organizations **identify, assess, manage, and reduce risks associated with Artificial Intelligence (AI) systems**.

Unlike traditional cybersecurity frameworks that focus only on technical vulnerabilities, the AI RMF addresses risks related to **security, privacy, fairness, transparency, reliability, and accountability** throughout the AI lifecycle.

> **Purpose:** Build AI systems that are **Trustworthy, Secure, Reliable, and Responsible.**

---

# Objectives of NIST AI RMF

- Identify AI-related risks
- Improve AI security
- Ensure trustworthy AI
- Reduce bias and unfairness
- Protect privacy
- Support continuous risk management
- Improve governance and accountability

---

# Core Functions of NIST AI RMF

The framework consists of **four core functions**:

```text
Govern
   │
   ▼
Map
   │
   ▼
Measure
   │
   ▼
Manage
```

These functions are continuous and repeated throughout the AI system's lifecycle.

---

# 1. Govern

## Definition

**Govern** establishes the policies, processes, and responsibilities needed to manage AI risks.

It defines **how AI will be developed, deployed, and monitored securely and responsibly**.

### How it Works

```text
Organization
      │
      ▼
Create AI Policies
      │
      ▼
Assign Roles & Responsibilities
      │
      ▼
Define Security & Compliance Rules
```

### Activities

- Create AI governance policies
- Define roles and responsibilities
- Establish risk management processes
- Develop AI ethics guidelines
- Define security policies
- Ensure legal and regulatory compliance

### Example

A company creating an AI chatbot:

- Creates an AI security policy.
- Assigns an AI Security Team.
- Defines who can access training data.
- Establishes rules for handling sensitive information.

### Goal

Create a strong governance structure before building or deploying AI.

---

# 2. Map

## Definition

**Map** identifies and understands the AI system, its environment, and the risks it may face.

It answers:

- What AI system are we protecting?
- What assets are involved?
- Who are the stakeholders?
- What risks exist?

### How it Works

```text
AI System
      │
      ▼
Identify Assets
      │
      ▼
Understand Business Context
      │
      ▼
Identify Risks & Stakeholders
```

### Activities

- Identify AI assets (models, datasets, APIs)
- Understand business objectives
- Identify stakeholders
- Determine potential threats
- Assess the AI attack surface

### Example

For a healthcare AI assistant:

- Identify the LLM used.
- Identify patient records used by the AI.
- Determine who can access the system.
- Identify risks such as data leakage or prompt injection.

### Goal

Understand the AI environment and identify potential risks.

---

# 3. Measure

## Definition

**Measure** evaluates AI risks by testing and assessing the security, reliability, and performance of AI systems.

### How it Works

```text
AI System
      │
      ▼
Security Testing
      │
      ▼
Risk Evaluation
      │
      ▼
Identify Vulnerabilities
```

### Activities

- AI Red Teaming
- Vulnerability Assessment
- Security Testing
- Bias testing
- Performance evaluation
- Safety validation

### Example

An organization tests its AI chatbot by:

- Performing prompt injection attacks.
- Conducting jailbreak testing.
- Assessing for hallucinations.
- Running vulnerability assessments.

### Goal

Measure how secure and trustworthy the AI system is.

---

# 4. Manage

## Definition

**Manage** focuses on reducing identified risks and continuously improving AI security after deployment.

### How it Works

```text
Risks Identified
        │
        ▼
Apply Fixes
        │
        ▼
Monitor AI System
        │
        ▼
Continuous Improvement
```

### Activities

- Apply security patches
- Monitor AI systems
- Fix vulnerabilities
- Update models and datasets
- Respond to new threats
- Improve security continuously

### Example

After discovering a prompt injection vulnerability:

- Update the system prompt.
- Add input validation.
- Patch the application.
- Monitor for future attacks.

### Goal

Continuously reduce risk and maintain secure AI operations.

---

# Complete AI RMF Workflow

```text
Govern
(Create policies & governance)
        │
        ▼
Map
(Identify assets & risks)
        │
        ▼
Measure
(Test & evaluate AI risks)
        │
        ▼
Manage
(Mitigate & continuously improve)
```

---

# Example Scenario

A company develops an AI-powered customer support chatbot.

## Govern

- Creates AI security policies.
- Assigns an AI governance team.

## Map

- Identifies customer data, APIs, and the LLM.
- Recognizes risks such as prompt injection and data leakage.

## Measure

- Conducts AI Red Teaming.
- Tests for jailbreaks and hallucinations.
- Performs vulnerability assessments.

## Manage

- Fixes discovered vulnerabilities.
- Updates security controls.
- Continuously monitors the chatbot for new threats.

---

# NIST AI RMF vs Traditional Risk Management

| Traditional Risk Management | NIST AI RMF |
|-----------------------------|-------------|
| Focuses mainly on IT systems | Focuses specifically on AI systems |
| Security and compliance | Security, fairness, privacy, transparency, reliability |
| Periodic assessments | Continuous AI risk management |
| Traditional software testing | AI Red Teaming, bias testing, prompt injection testing |

---

# Key Terms

| Term | Meaning |
|------|---------|
| NIST AI RMF | Framework for managing AI-related risks |
| Govern | Establish AI policies, roles, and governance |
| Map | Identify AI assets, stakeholders, and risks |
| Measure | Evaluate AI risks through testing and assessments |
| Manage | Mitigate risks and continuously improve AI security |
| AI Red Teaming | Simulating attacks to identify AI vulnerabilities |
| Vulnerability Assessment | Identifying weaknesses in AI systems |
| Continuous Monitoring | Ongoing observation to detect and respond to new risks |

---
