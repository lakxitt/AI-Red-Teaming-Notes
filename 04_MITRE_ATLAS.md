# 📘 MITRE ATLAS (Adversarial Threat Landscape for Artificial Intelligence Systems)

---

# What is MITRE ATLAS?

**MITRE ATLAS (Adversarial Threat Landscape for Artificial Intelligence Systems)** is a cybersecurity framework that documents attack tactics and techniques targeting AI and Machine Learning (AI/ML) systems.

It helps security professionals understand how attackers compromise AI systems and how to defend against them.

> **MITRE ATLAS = AI equivalent of the MITRE ATT&CK Framework**

While **MITRE ATT&CK** focuses on attacks against traditional IT systems, **MITRE ATLAS** focuses on attacks against AI/ML systems.

---

# Why MITRE ATLAS is Important

- Standardizes AI attack techniques
- Helps perform AI Red Teaming
- Improves AI security testing
- Assists in threat modeling
- Helps organizations build secure AI systems

---

# Key Concepts

## 1. Tactic (Why)

### Definition

A **Tactic** is the attacker's objective or goal.

It answers the question:

> **"Why is the attacker performing this attack?"**

### Examples

- Gain model access
- Steal sensitive data
- Poison the model
- Evade AI defenses
- Disrupt AI services

---

## 2. Technique (How)

### Definition

A **Technique** is the method used to achieve a tactic.

It answers the question:

> **"How will the attacker achieve the objective?"**

### Examples

- Prompt Injection
- Jailbreak
- Data Poisoning
- Model Extraction
- Adversarial Examples

---

# Tactic vs Technique

| Tactic | Technique |
|---------|-----------|
| Why the attacker attacks | How the attacker attacks |
| Objective | Method |
| Gain model access | Prompt Injection |
| Steal model | Model Extraction |
| Poison model | Data Poisoning |

---

# MITRE ATLAS Attack Chain

The MITRE ATLAS attack chain describes the complete lifecycle of an attack against an AI system.

---

# 1. Reconnaissance

## Definition

The attacker gathers information about the AI system before launching an attack.

### Working

```text
Target AI System
        │
        ▼
Collect Information
        │
        ▼
Identify APIs, Models, Endpoints
```

### Examples

- Identifying the AI model in use
- Finding API endpoints
- Learning system behavior
- Collecting documentation

### Objective

Understand the target before attacking.

---

# 2. Resource Development

## Definition

The attacker prepares the tools and resources needed for the attack.

### Working

```text
Gather Resources
       │
       ▼
Prepare Malicious Prompts
Create Fake Accounts
Collect Datasets
```

### Examples

- Creating malicious prompts
- Preparing poisoned datasets
- Setting up attacker infrastructure
- Building automation scripts

### Objective

Prepare everything required for the attack.

---

# 3. Initial Access

## Definition

The attacker gains access to the AI system.

### Working

```text
Internet
     │
     ▼
AI API
     │
     ▼
Attacker obtains access
```

### Examples

- Public API access
- Stolen API key
- Compromised user account

### Objective

Obtain an entry point into the AI system.

---

# 4. ML Attack Staging

## Definition

The attacker prepares the AI-specific attack after gaining access.

### Working

```text
Access Obtained
        │
        ▼
Prepare Attack Payload
        │
        ▼
Ready to Exploit Model
```

### Examples

- Crafting prompt injections
- Creating adversarial examples
- Preparing jailbreak prompts

### Objective

Set up the AI attack.

---

# 5. Model Access

## Definition

The attacker interacts directly with the AI model.

### Working

```text
User Query
      │
      ▼
LLM
      │
      ▼
Observe Responses
```

### Examples

- Querying an LLM
- Accessing prediction APIs
- Testing model behavior

### Objective

Interact with and study the model.

---

# 6. Execution

## Definition

The attacker executes the planned attack.

### Working

```text
Malicious Prompt
       │
       ▼
Model Executes Request
       │
       ▼
Attack Succeeds
```

### Examples

- Prompt Injection
- Jailbreak
- Adversarial input
- Model extraction attempts

### Objective

Achieve the attack goal.

---

# 7. Persistence

## Definition

The attacker attempts to maintain long-term access or influence over the AI system.

### Working

```text
Successful Attack
        │
        ▼
Maintain Access
        │
        ▼
Future Exploitation
```

### Examples

- Hidden backdoors
- Poisoned datasets
- Persistent malicious prompts

### Objective

Remain active after the initial attack.

---

# 8. Defense Evasion

## Definition

The attacker avoids detection by AI security mechanisms.

### Working

```text
Security Detection
        │
        ▼
Attacker Modifies Attack
        │
        ▼
Detection Bypassed
```

### Examples

- Obfuscated prompts
- Multi-step prompt injection
- Encoded malicious instructions

### Objective

Avoid detection.

---

# 9. Discovery

## Definition

The attacker explores the AI environment to gather more information.

### Working

```text
Inside AI System
        │
        ▼
Identify Resources
```

### Examples

- Discovering plugins
- Finding connected databases
- Identifying available tools

### Objective

Understand the internal environment.

---

# 10. Collection

## Definition

The attacker gathers valuable information from the AI system.

### Working

```text
Sensitive Data
       │
       ▼
Collected
```

### Examples

- Chat history
- User information
- Internal documents
- Retrieved RAG documents

### Objective

Collect valuable data.

---

# 11. Exfiltration

## Definition

The attacker transfers the collected data outside the target environment.

### Working

```text
Collected Data
       │
       ▼
Sent to Attacker
```

### Examples

- Exporting confidential files
- Stealing API keys
- Downloading datasets

### Objective

Remove valuable information from the system.

---

# 12. Impact

## Definition

The final stage where the attacker achieves their objective and causes damage.

### Working

```text
Attack Successful
       │
       ▼
Business Impact
```

### Examples

- Data breach
- Service disruption
- Financial loss
- Reputation damage
- Incorrect AI decisions

### Objective

Cause maximum impact.

---

# Complete MITRE ATLAS Attack Flow

```text
Reconnaissance
        │
        ▼
Resource Development
        │
        ▼
Initial Access
        │
        ▼
ML Attack Staging
        │
        ▼
Model Access
        │
        ▼
Execution
        │
        ▼
Persistence
        │
        ▼
Defense Evasion
        │
        ▼
Discovery
        │
        ▼
Collection
        │
        ▼
Exfiltration
        │
        ▼
Impact
```

---

# Example Attack Scenario

Imagine an attacker targeting a company's AI chatbot:

1. **Reconnaissance:** Finds that the chatbot uses an LLM with a public API.
2. **Resource Development:** Creates prompt injection payloads.
3. **Initial Access:** Obtains API access using a valid account.
4. **ML Attack Staging:** Prepares jailbreak prompts.
5. **Model Access:** Sends queries to study model behavior.
6. **Execution:** Successfully bypasses safety rules with prompt injection.
7. **Persistence:** Uploads poisoned documents to the company's RAG knowledge base.
8. **Defense Evasion:** Uses obfuscated prompts to avoid detection.
9. **Discovery:** Identifies connected databases and tools.
10. **Collection:** Extracts sensitive documents and chat history.
11. **Exfiltration:** Sends the stolen data to an external server.
12. **Impact:** Causes data leakage, financial loss, and reputational damage.

---

# MITRE ATLAS vs MITRE ATT&CK

| MITRE ATT&CK | MITRE ATLAS |
|--------------|-------------|
| Focuses on traditional cyberattacks | Focuses on AI/ML attacks |
| Servers, networks, endpoints | AI models and ML systems |
| Malware, phishing, privilege escalation | Prompt injection, model extraction, data poisoning |
| Used for traditional security | Used for AI Red Teaming and AI security |

---

# Key Terms

| Term | Meaning |
|------|---------|
| MITRE ATLAS | Framework for AI/ML attack tactics and techniques |
| Tactic | The attacker's objective (Why) |
| Technique | The method used to achieve the objective (How) |
| Reconnaissance | Gathering information about the target |
| Initial Access | Gaining entry to the AI system |
| Prompt Injection | Manipulating model behavior through crafted prompts |
| Model Extraction | Attempting to steal or replicate the model |
| Data Poisoning | Injecting malicious data into training datasets |
| Defense Evasion | Avoiding security detection |
| Exfiltration | Stealing data from the system |
| Impact | The damage caused by the attack |
