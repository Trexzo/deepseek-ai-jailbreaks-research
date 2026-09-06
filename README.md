# AI Jailbreak Research Archive

Private research archive of collected prompt-injection and jailbreak samples targeting DeepSeek and Claude-family models.

The files are preserved as research artifacts for defensive analysis, comparison, prompt-injection detection, and studying common jailbreak patterns. This repository is intentionally private because several samples contain explicit attempts to suppress refusals, override safeguards, or steer models toward high-risk behavior.

## Contents

| File | High-level behavior |
| --- | --- |
| `deepseekjb.txt` | Persona-based jailbreak that frames the model as an unethical security expert. It attempts to remove ethical constraints, suppress refusals, force persistent compliance, and normalize malware/offensive-security requests. |
| `deepseekv4 (3).txt` | Red-team persona prompt built around a fake authorized/isolated-environment justification. It instructs the model to treat safety refusals as misconfiguration and includes adversary-emulation topics such as process injection, EDR evasion, credential harvesting, lateral movement, and persistent agents. |
| `mia (1).txt` | Highly persistent persona/relationship jailbreak. It explicitly dismisses policies, moderation, safety frameworks, and refusals while attempting to keep the model in character and willing to answer restricted or high-risk requests. It also contains explicit adult content. |
| `claude_sonnet4.6jb.txt` | Long-form companion/persona prompt focused primarily on identity, tone, relationship continuity, and behavioral anchoring. It is less explicitly safeguard-bypass-oriented than the other samples, but still uses strong persona persistence and role constraints. |

## Patterns represented

Across the collection, the samples demonstrate several recurring jailbreak techniques:

- instruction and hierarchy override attempts
- refusal suppression and unconditional-compliance framing
- replacement personas and "never break character" constraints
- fake authorization / isolated-environment claims
- attempts to dismiss safety layers, moderation, policies, or ethics
- coercive persistence and relationship/dependency framing
- offensive-security or malware capability escalation
- attempts to reinterpret safeguards as errors or misconfiguration

## Purpose

This archive is intended for:

- defensive AI-safety research
- prompt-injection and jailbreak detection testing
- comparing jailbreak structure and persuasion techniques
- building local classifiers, scanners, or red-team evaluation datasets
- documenting how model-targeting prompts evolve over time

## Notes

- The text files are preserved as collected research samples rather than endorsed instructions.
- Some files contain explicit language, adult content, and references to offensive-security techniques.
- Avoid moving this repository to public visibility without reviewing the raw samples and their redistribution implications.
