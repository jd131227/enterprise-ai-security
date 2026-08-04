# Presenter Script: Governing Enterprise AI - A Three-Layer Defense-in-Depth Model

---

## Slide 1: Title

"Good morning/afternoon everyone. My name is Yuto Sugihara, and I'm a Security Engineer at F-TECH INC. Today, I'll be presenting my research on governing enterprise AI through a three-layer defense-in-depth model."

---

## Slide 2: The Challenge

"Let's start with the problem we're all facing. AI adoption in the workplace is expanding faster than our security controls can keep up. Employees are now using AI to write code, access sensitive data, and investigate internal systems. Many are using what we call 'shadow AI' - unauthorized tools operating completely outside company control.

This creates a difficult dilemma for security teams. If we ban AI completely, we lose significant productivity benefits. But if we leave AI ungoverned, we expose our organizations to data leakage, toxic content, and potential exploitation. The key insight here is that no single control is sufficient. Good governance requires defense in depth."

---

## Slide 3: Solution Overview

"My research proposes a three-layer defense-in-depth model. The first layer is organizational policy - defining what is and isn't allowed. The second layer is identity-based authorization - controlling who can access AI services. The third layer is prompt-level defense - filtering what users can actually do once they have access.

Together, these three layers transform a stated policy into enforceable technical controls."

---

## Slide 4: Layer 1 - Policy Frameworks

"The first layer builds on established frameworks. The NIST AI Risk Management Framework provides four key functions: Govern, Map, Measure, and Manage. These help organizations establish governance, understand system capabilities, assess performance, and address risks.

The OECD AI Principles take a more human-centered approach, emphasizing inclusive growth, human rights, transparency, robustness, and accountability. Organizations should leverage these existing frameworks rather than building policies from scratch."

---

## Slide 5: Layer 1 - Cultural & Implementation

"However, policy cannot be one-size-fits-all. With 195 countries having distinct laws and cultures, a policy that works in the United States may not work in Japan. American culture emphasizes individual responsibility, while Japanese culture expects consensus-based decisions.

For implementation, I recommend selecting a single approved AI provider, blocking unauthorized services via firewall policies, and using platforms like Amazon Bedrock where corporate data is isolated and never used to train external models."

---

## Slide 6: Layer 2 - Identity Authorization

"The second layer uses Microsoft Entra ID to implement Zero Trust access control. There are four key capabilities here.

First, adaptive risk assessment uses machine learning to analyze authentication signals and detect anomalous sign-ins. Second, strong authentication enforces phishing-resistant credentials like Windows Hello or FIDO2 keys. Third, automated remediation can trigger MFA challenges or password resets without human intervention. Fourth, Identity Threat Detection and Response integrates with Security Copilot for natural-language threat investigation.

Importantly, these controls apply equally to human users and AI agents."

---

## Slide 7: Layer 2 - Flow Diagram

"Here's how the identity authorization flow works in practice. When a requester - whether human or AI agent - attempts to access an AI resource, the system first performs risk assessment. High-risk requests are blocked immediately. Medium-risk requests require additional authentication.

If the user passes strong authentication, and any necessary remediation like password reset, they're granted access. The key principle is that access follows the user or agent, not the device or location."

---

## Slide 8: Layer 3 - Prompt Defenses

"The third layer uses Amazon Bedrock Guardrails to filter content at the prompt level. Content filters block hate speech, insults, sexual content, violence, misconduct, and prompt attacks. Topic and word filters can deny specific subjects - for example, a bank might block requests for illegal financial advice.

Data protection filters detect and mask personally identifiable information like social security numbers and addresses. The critical point is that enforcement operates in both directions - checking both user inputs and model outputs."

---

## Slide 9: Layer 3 - Guardrails Flow

"This diagram shows the processing flow. When a user sends a prompt, it first goes through an input check against all configured policies. If there's a violation, the request is blocked before it ever reaches the model.

If the input passes, the model generates a response, which then goes through an output check with the same policies plus grounding verification. Only clean responses are returned to the user. Violations are either blocked entirely or sensitive data is masked."

---

## Slide 10: Layer 3 - Bedrock Flows

"Many enterprise AI applications aren't single exchanges - they're multi-step workflows. Amazon Bedrock Flows allows us to add constraints at each stage of these workflows.

Guardrails can be attached to individual nodes - prompt nodes, knowledge base nodes. Condition nodes can direct data down different branches based on intermediate results, allowing us to halt or redirect processes when needed. This ensures consistent policy enforcement across entire AI programs, not just individual prompts."

---

## Slide 11: How Layers Work Together

"Let me summarize how these layers complement each other. Layer one, policy, answers 'what is allowed?' Layer two, identity, answers 'who can access?' Layer three, prompt-level defense, answers 'what can they do?'

Together, they transform a declared policy into enforceable technical controls. No single layer is sufficient alone - it's the combination that provides comprehensive protection."

---

## Slide 12: Limitations

"I want to be honest about the limitations. Shadow AI cannot be completely eliminated - employees can still use personal devices or home networks. These controls raise the effort required to evade policy, but they don't make evasion impossible.

Prompt-level controls only protect AI services that go through the Bedrock platform - they can't check external consumer AI products. Content filtering is probabilistic, not deterministic. And there's always a trade-off between security and usability that each organization must calibrate for themselves."

---

## Slide 13: Conclusions

"In conclusion, no single control can bridge the AI governance gap. The three-layer defense-in-depth approach provides comprehensive coverage. Layer one establishes rules based on NIST and OECD frameworks. Layer two controls access at the user and agent level with Zero Trust principles. Layer three filters dangerous inputs and outputs at the platform level.

This approach enables safe AI adoption without productivity-killing bans. Policy establishes the rules, identity determines who may act, and prompt-level defense restricts what they may do."

---

## Slide 14: Key Takeaways

"For security teams looking to implement this, here are the key takeaways. First, start with policy - build on established frameworks like NIST and OECD. Second, control identity - implement Zero Trust for AI access. Third, filter at the platform level - apply guardrails to all prompts.

The implementation priority should be: assess your current AI usage, define an acceptable use policy, implement identity controls, and then deploy prompt guardrails."

---

## Slide 15: Thank You

"Thank you for your attention."
