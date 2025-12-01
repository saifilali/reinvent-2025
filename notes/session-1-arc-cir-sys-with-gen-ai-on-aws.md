# Architecting Circular Systems with Generative AI on AWS

**Speakers:** Ana Suja Lucia, Pauline Tine

---

## How Can Technology Enable Circularity

- Data analytics
- AI/ML
- Collaboration tools

---

## Use Case: CardboardCorp Operations

### Scenario

Maria, a production supervisor at CardboardCorp, faces daily operational challenges:

- Manual alert management
- Fragmented data sources
- Physical inspection dependency
- Reactive maintenance approach
- Resource constraints

---

## Part 1: Water Usage Analysis

**Key Question:** How much water does each process use and why? Is it normal?

### Data Collection Pipeline

**Data Sources:**

- Sensors
- Bills
- Rainwater metrics
- Compliance documents
- Machine documentation

**AWS Architecture:**

```
Data Collection:
├── Sensors → AWS IoT Core → S3
├── Bills → Amazon Textract → S3
├── Rainwater → API Gateway → S3
├── Compliance Documents → S3
└── Machine Documents → S3

Data Processing:
└── S3 → Amazon Bedrock Knowledge Base
```

---

## Part 2: Automated Anomaly Detection & Response

**Key Question:** How do we automate anomaly detection, root cause analysis, and remediation actions?

### Solution Architecture

```
Amazon Bedrock Knowledge Base
    ↓
Bedrock Agent (Anomaly Detection & Root Cause Analysis)
    ↓
Alert System (Automated Actions)
```

**Flow:**

1. Data from Knowledge Base feeds into Bedrock Agent
2. Agent performs anomaly detection and root cause analysis
3. Agent triggers alerts and automated remediation actions
