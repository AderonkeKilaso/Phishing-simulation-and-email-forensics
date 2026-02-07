# Phishing Awareness Risk Analysis

## Project Overview
This project evaluates the risk that authorized users can be socially engineered into enabling unauthorized access, resulting in credential compromise and broader system exposure.

A simulated phishing awareness exercise was conducted in a controlled learning environment to measure human behavior at key decision points, including link interaction, credential submission, and phishing incident reporting.

The focus of this project is **human risk measurement** and access control exposure, not technical email security controls.

---

## Objectives
The simulation was designed to measure three observable behaviors:

1. **Reduce link-click rate**  
   Evaluate user ability to recognize and avoid suspicious email content. *(Prevent)*

2. **Reduce credential submission rate**  
   Assess access control exposure through social engineering. *(Protect)*

3. **Increase phishing reporting rate**  
   Measure user participation in detection and response processes. *(Detect / Respond)*

---

## Simulation Scope
- **User population:** 25 users  
- **Campaign type:** Single phishing campaign  
- **Scenario:** Invoice / service renewal phishing email  
- **Observation window:** 48–72 hours  
- **Training context:** First structured phishing awareness training  

---

## Tooling and Methodology

### Operating Environment
- **Kali Linux**  
  Used as the primary operating environment for phishing analysis and simulation activities.

### Simulation Mechanism
- **Social Engineering Toolkit (SET) – Credential Harvester**  
  Used in a controlled learning environment to model credential-harvesting behavior and demonstrate how social engineering can bypass access controls.

### Phishing Artifact and Content Analysis
- **GitHub (PhishPots repository)**  
  Public phishing email samples reviewed to inform realistic scenario design.
- **Thunderbird**  
  Used to inspect phishing emails in a standard email-client layout to replicate end-user experience.
- **Mousepad (text editor)**  
  Used to inspect raw email headers, including SPF, DKIM, DMARC, return-path, and sender IP fields.

### Threat Intelligence and Reputation Analysis
- **VirusTotal**  
  Used to assess reputation of embedded URLs.
- **AbuseIPDB**  
  Used to evaluate sender IP reputation and prior abuse reports.

### Conceptual Reference Only
- **sendEmail**  
  Discussed to explain sender spoofing and SPF bypass concepts. Not used to send emails.

### Explicitly Excluded Tools
- ServiceNow  
- Nessus  

---

## Metrics

The following metrics were measured before and after security awareness training.

| Metric | Baseline | Post-Training |
|------|---------|--------------|
| Link click rate | 40% | 20% |
| Credential submission rate | 28% | 12% |
| Phishing reporting rate | 12% | 72% |

---

## Analysis

### Link-Click Behavior
The reduction in link-click activity indicates improved user caution when evaluating email-based requests. Training enhanced initial threat recognition, reducing exposure opportunities, while acknowledging that residual risk remains.

### Credential Submission Risk
Credential submission attempts declined meaningfully but were not eliminated. This confirms that access control bypass through social engineering remains a material risk and requires continued reinforcement.

### Phishing Reporting Behavior
Phishing reporting increased substantially following training, demonstrating improved user engagement with detection processes and strengthening organizational visibility into social engineering attempts.

---

## Recommendations

1. **Conduct recurring phishing simulations**  
   Implement quarterly simulations to maintain awareness and monitor behavioral drift.

2. **Provide targeted refresher training**  
   Deliver focused reinforcement to users who clicked links or submitted credentials, emphasizing authentication-stage decision-making.

3. **Reinforce phishing reporting mechanisms**  
   Promote reporting channels and share anonymized reporting metrics to sustain engagement.

---

## Embedded Dataset (Analyst-Constructed)

The dataset below was constructed for analytical purposes and reflects the metrics used in this project.

```csv
metric,baseline_percentage,post_training_percentage,user_count
Link Click Rate,40,20,25
Credential Submission Rate,28,12,25
Phishing Reporting Rate,12,72,25
# Phishing-simulation-and-email-forensics
