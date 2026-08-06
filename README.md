# Sebastian Mateus

Senior AI/ML Engineer at **Nequi (Grupo Bancolombia)**, pre-training foundation
models on customer transaction sequences. 8+ years shipping production ML.
Based in Colombia 🇨🇴.

I'm most interested in the gap between what a model appears to do and what it
actually does — evaluation that survives scrutiny, agent tool-use that earns its
place, and systems whose failure modes are written down before someone finds them.

**[Full portfolio & research →](https://elmatiofficial.github.io)**

---

## Selected work

**[RealH](https://github.com/ElMatiOfficial/realh)** — Proof-of-personhood and
content provenance using W3C Verifiable Credentials. Ed25519 signing, `did:web`,
public JWKS for offline verification. The README opens with four specific reasons
not to trust it in production, because a reference implementation that hides its
threat model is worse than none.
`TypeScript` · CI · CodeQL · gitleaks · [ADR on JCS canonicalization](https://github.com/ElMatiOfficial/realh/blob/main/docs/decisions/001-jcs-canonicalization.md)

**[Kaggle write-ups](https://github.com/ElMatiOfficial/kaggle-solutions)** — 19
competitions, each documented as a short paper. Includes a
**[provenance ledger](https://github.com/ElMatiOfficial/kaggle-solutions/blob/main/PROVENANCE.md)**
that states, per competition, exactly which submissions were my own work and
which were not — verified by diffing my final submissions against the public
notebooks they came from. 5 of 19 were substantially original; the ledger says
which, and names every upstream author.

**[EML translator](https://github.com/ElMatiOfficial/EML-Matemathical-Translator-for-AI)** —
Library for translating mathematical expressions to and from Exp-Minus-Log trees
([Odrzywołek's primitive](https://arxiv.org/abs/2603.21852)). Forward/inverse
translation, complex-branch evaluation, exhaustive identity search.
`Python` · 116 tests · MIT

**[EML research POC](https://github.com/ElMatiOfficial/EML-Research-POC)** —
Wires those operations into Claude as tool-use and benchmarks whether it helps.
The honest answer, reported in the README: on calculus and algebra the agents
largely ignore the EML tools in favour of sympy. It earns its keep only on
translate/evaluate/verify tasks.

**[barrio-mapper](https://github.com/ElMatiOfficial/barrio-mapper)** — Maps the
small independently-owned businesses of a neighbourhood — tiendas, droguerías,
ferreterías — while filtering out chains. Three-signal chain detection with an
auditable rejection log. Tested in Medellín;
[runs in the browser](https://elmatiofficial.github.io/barrio-mapper/).
`Python` · tests · CLI + browser app

---

## What I work on

**Production ML** — foundation model pre-training on transaction sequences ·
credit risk (PD/LGD, loss-rate forecasting, IV/WoE, Platt calibration,
SHAP-driven adverse-action reasons) · recommender systems

**Agentic systems** — tool-use design and evaluation · structured output ·
multi-step orchestration · guardrailed tool access · agent security
(multi-step tool attacks)

**Evaluation & observability** — offline eval sets wired into CI ·
faithfulness and LLM-as-judge · embedding drift detection · PSI monitoring ·
Langfuse tracing

**Stack** — Python · SQL · PyTorch · scikit-learn · XGBoost · LightGBM ·
Hugging Face · BigQuery · dbt · Airflow · FastAPI · MLflow · AWS · Docker ·
Terraform · GitHub Actions

---

## Elsewhere

[Portfolio](https://elmatiofficial.github.io) ·
[LinkedIn](https://www.linkedin.com/in/sebastianmateusperdomo/) ·
[Kaggle](https://www.kaggle.com/sebastianmateus) ·
[TEDx talk](https://www.youtube.com/watch?v=RivKU85N9gw)

Trilingual (ES/EN/PT) · Mentored 13+ engineers
