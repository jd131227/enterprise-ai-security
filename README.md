# Governing Enterprise AI: A Three-Layer Defense-in-Depth Model

## Overview

This repository contains the research paper and presentation materials for a proposed three-layer defense-in-depth framework for managing enterprise AI deployment securely and at scale.

As AI adoption in the workplace accelerates faster than organizations can protect themselves, IT and security teams face a governance challenge: prohibiting AI entirely eliminates productivity benefits, while leaving it ungoverned exposes organizations to data leakage, harmful content, and misuse.

This paper proposes a three-layer control model:

- **Layer 1 — Organizational Policy**: Based on NIST AI Risk Management Framework and OECD AI Principles
- **Layer 2 — Identity-Based Authorization**: Using Microsoft Entra ID to control which identities can access AI services
- **Layer 3 — Prompt-Level Defense**: Using Amazon Bedrock Guardrails and Flows to filter harmful inputs and responses

## Published

| Item | Detail |
|------|--------|
| Platform | Zenodo |
| DOI | [10.5281/zenodo.21347905](https://doi.org/10.5281/zenodo.21347905) |
| Indexed | OpenAIRE |
| Published | July 2026 |

## Abstract

The increasing use of artificial intelligence in the workplace has surpassed the security safeguards of employing such technology. Employees may now use AI to develop and execute code, access sensitive data, and explore internal systems, sometimes using unauthorized "shadow AI" tools that operate outside of company supervision. This paper contends that no single control is sufficient and proposes a three-layer, defense-in-depth approach. The three layers translate a stated policy into enforceable technological constraints, allowing a security team to appropriately oversee AI usage while not prohibiting AI.

## Key Contributions

- Novel three-layer defense-in-depth framework for enterprise AI governance
- Integration of NIST AI RMF and OECD principles into practical enterprise policy
- Analysis of identity-based authorization for both human and agentic AI identities
- Evaluation of Amazon Bedrock Guardrails and Flows for prompt-level defense
- Discussion of cultural and legal considerations for global enterprise deployment

## Contents

| File | Description |
|------|-------------|
| `paper/Three-Layer-Defense-in-Depth-Model.pdf` | Full research paper |
| `presentation/Three-Layer-Defense-Presentation.pptx` | Slide deck |
| `presentation/Three-Layer-Defense-Presentation.html` | Interactive HTML presentation |
| `presentation/Presenter-Script.md` | Presenter notes |

## Citation

\```bibtex
@misc{sugihara2026,
  author    = {Sugihara, Yuto},
  title     = {Governing Enterprise AI: A Three-Layer 
               Defense-in-Depth Model},
  year      = {2026},
  publisher = {Zenodo},
  doi       = {10.5281/zenodo.21347905},
  url       = {https://doi.org/10.5281/zenodo.21347905}
}
\```

## License

This work is licensed under Creative Commons Attribution 4.0 International (CC BY 4.0).
See [LICENSE](LICENSE) for details.
