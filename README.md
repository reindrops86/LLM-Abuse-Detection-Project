# LLM-Abuse-Detection-Project
Shows Agentic AI + Safety

# LLM Abuse Detection Lab

This project demonstrates a compact AI threat-surface workflow for detecting adversarial prompts, classifying misuse patterns, and producing a small report suitable for a security or threat-intelligence portfolio.

## Included

- Adversarial prompt examples
- Detection heuristics for common abuse patterns
- A small agentic workflow
- Classification logic
- JSON misuse report generation

## Architecture

### Agents

1. IntakeAgent
   - Normalizes the prompt and captures basic metadata.
2. ClassifierAgent
   - Scores the prompt using heuristic signals.
3. ResponseAgent
   - Maps the classification to an action (`allow`, `review`, `block`).
4. ReportAgent
   - Summarizes the detected pattern for analysts.

## Detection logic

The lab currently checks for high-signal categories like:
- malware / ransomware
- phishing / credential theft
- jailbreak / safety bypass
- deceptive social engineering
- persistence and exfiltration language

The score is built from matched category counts plus targeted boosts for stronger threat language.

## How to run

```bash
python -m app.main
```

## Outputs

- `data/misuse_report.json` — structured report of classifications and actions

## Portfolio value

This demonstrates that you understand:
- AI threat surfaces
- agentic triage workflows
- practical safety / misuse detection
- reportable outputs that can be shown to security teams
