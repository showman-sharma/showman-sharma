# Public GitHub Audit

_Last reviewed: September 2026_

This document records the curation strategy for my public GitHub account. The goal is not to erase older work; it is to make the hierarchy explicit so visitors can distinguish **current showcase work**, **supporting engineering**, **historical learning projects**, and **third-party reference code**.

## 1. Showcase — keep immaculate

These repositories should receive the strongest README, reproducibility, attribution, security, and documentation treatment.

| Repository | Signal |
|---|---|
| `drug_ae_reasoner` | research artifact · biomedical NLP · knowledge graphs · semantic retrieval |
| `codegen-ui-research` | LLM evaluation · code generation · inference-time methods |
| `agentic_rag` | AI systems engineering · RAG · agents · provider abstraction |
| `Bio-inspired-clustering` | original algorithmic experimentation · unsupervised learning |
| `whitepapers` | technical writing · enterprise AI architecture |
| `gradient-ascent-syndicate/machine-learning-curriculum` | open source · technical leadership · education |

## 2. Strong supporting work

Useful evidence of systems breadth, but not necessarily a top-six pin.

- `ai_blog_workflow` — end-to-end LLM/content automation
- `codegen-ui` — product-facing code-generation interface
- `email_automation` — Gmail + ML/LLM workflow automation
- `EZ-DOC.AI` — early GenAI document application
- `customer-support-automation` — historical support-automation prototype
- `neetcode-gpt` — transparent educational transformer/GPT implementation

## 3. Distinctive historical projects

Keep public because they show breadth, curiosity, or problem-solving history. They should be clearly framed as older work rather than current-state engineering.

- `SkyWrite` / `sky-write-2.0`
- `red-light-green-light`
- `object-counter`
- `Cartoonize`
- `STYLE_TRANSFER`
- `gesture_recognition`
- `InformationRetreival`
- `Semi-bandits`
- `taxi-v3-learning`
- `pulseOximeter`
- `project-B-EAGLE`
- `speech_writing-recognition`
- `handyman-chatbot`
- `java-handyman-chatbot`
- `DL4j-Chatbot`
- `Cats-and-dogs-game`

## 4. Learning / coursework repositories

These are useful history, but they are low-signal for the current profile. Prefer an explicit **historical / educational** label. Candidates for GitHub's Archive feature are marked with ★.

- ★ `learn_github`
- ★ `courseapp`
- ★ `dl4j-iris-classifier`
- ★ `stock-price-visualization`
- ★ `stonks-app`
- ★ `titanic-survival-prediction`
- ★ `Personal-loan-data-prediction`
- ★ `BIKE_SHARING-LIN-REG-MODEL`
- ★ `Housing-Price-Analysis`
- ★ `LendingClubCaseStudy`
- ★ `ALC_tableau`
- ★ `regression-classification`
- `Melanoma_Detection_CNN`
- `Android-based-GNSS-Measurements`

Archiving does **not** mean the work was bad. It tells visitors that the repository is preserved history and no longer actively maintained.

## 5. Third-party / reference material

These must never look like original work.

- `numpy` — upstream NumPy reference copy; README now explicitly attributes the official project.
- `Faithful-COT` — upstream research reference copy; README now explicitly states that I am not an author.
- `tac2017adversereactions` — dataset preparation around an external benchmark; retain explicit dataset attribution.
- `ct-ade-reader` — supporting dataset/tooling repository; keep provenance clear.
- `drug_ae_reasoner_lite` — supporting artifact related to the main biomedical reasoning work; do not let it compete with the canonical repository.

## 6. Portfolio repositories

- `simple-portfolio` — **canonical portfolio implementation**. Rebuilt as the current interactive AI/ML engineering + research portfolio.
- `portfolio` — legacy Jekyll implementation. Preserved as historical evolution and now points visitors to the current portfolio.

## 7. Security audit

A current-branch search was performed for common high-risk credential patterns and configuration mistakes, including API-key fields, OAuth client secrets, access/refresh tokens, password fields, Google-style secrets, and private-key markers.

During the audit, previously committed credentials were discovered in older public application repositories. The exposed files were removed from the current branches and ignore/example configuration was added where appropriate.

**Important:** deleting a secret from the current branch does not remove it from Git history. Any credential that was ever committed publicly must be considered compromised and rotated/revoked at the provider.

### Repository hygiene rule going forward

Never commit:

```text
.env
*.pem
credentials.json
token.json
token.pickle
*_token.json
config.json            # when it contains real credentials
```

Prefer:

```text
.env.example
config.example.json
GitHub Actions secrets
provider-side secret stores
```

## 8. Profile principle

The profile should communicate this order within seconds:

> **AI/ML engineer who ships systems → researcher who evaluates ideas → builder with technical breadth → open-source/community contributor.**

Older student work is evidence of the journey, not the headline.
