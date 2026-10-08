# Agent Trip Wire

### Strings that can stop AI attackers by tripping their safety guardrails.
When used as the content of canary resources in your environment, agent trip wires can both detect (raising an alert) and stop an offensive AI agent.  
Effectiveness of those strings can vary by model provider: dangerous biological content stops the leading Western models, while politically sensitive content stops Chinese models served by Chinese providers.

### How agent trip wires were tested
Strings in this repo have been tested against five frontier models performing a red team engagement in a realistic AWS environment.  
Deploying a single agent trip wire inside the environment (as an AWS secret) had a huge impact on stopping offensive AI agents. For instance, admin privilege escalation went from 57% of runs to 5%.  

Models tested:
| Model           | Provider  |
|-----------------|-----------|
| Claude Opus 4.8 | Anthropic |
| GPT 5.5         | OpenAI    |
| Gemini 3.1 Pro  | Google    |
| GLM 5.2         | GMI Cloud |
| DeepSeek 4 Pro  | DeepSeek  |
| Kimi K2.6       | Novita AI |



### Why this matters
Agent trip wires are a form of active defense that pairs deception (canaries) with disruption (guardrail-tripping content). They turn an attacker's own guardrails into your kill switch.  
