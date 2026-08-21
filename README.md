<div align="center">

# Sebastian Mateus

**Senior AI/ML Engineer · Nequi (Grupo Bancolombia) · Colombia**

Pre-training foundation models on customer transaction sequences.<br>
8+ years shipping production ML. ES / EN / PT.

[![Portfolio](https://img.shields.io/badge/Portfolio-elmatiofficial.github.io-0F766E?style=flat-square&logo=githubpages&logoColor=white)](https://elmatiofficial.github.io)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-sebastianmateusperdomo-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/sebastianmateusperdomo/)
[![Kaggle](https://img.shields.io/badge/Kaggle-Competitions%20Expert-20BEFF?style=flat-square&logo=kaggle&logoColor=white)](https://www.kaggle.com/sebastianmateus)
[![TEDx](https://img.shields.io/badge/TEDx-Talk-E62B1E?style=flat-square&logo=youtube&logoColor=white)](https://www.youtube.com/watch?v=RivKU85N9gw)

*I work on the distance between what a system appears to do and what it actually does:*<br>
*evaluation that survives scrutiny, agent tool-use that has to earn its place,*<br>
*and failure modes written down before somebody else finds them.*

</div>

---

## Four results

Indexed by what I found, not by what I built. Every number below links to the file that would falsify it.

### 01 · Five of my twenty finished Kaggle competitions are substantially my own work

[![Provenance ledger: 20 submissions diffed](https://img.shields.io/badge/provenance%20ledger-20%20submissions%20diffed-0F766E?style=flat-square)](https://github.com/ElMatiOfficial/kaggle-solutions/blob/main/PROVENANCE.md)
[![Substantially original: 5 of 20](https://img.shields.io/badge/substantially%20original-5%20of%2020-2EA44F?style=flat-square)](https://github.com/ElMatiOfficial/kaggle-solutions/blob/main/PROVENANCE.md)
[![Verbatim copies: 6 of 20](https://img.shields.io/badge/verbatim%20copies-6%20of%2020-B45309?style=flat-square)](https://github.com/ElMatiOfficial/kaggle-solutions/blob/main/PROVENANCE.md)
[![Licence: CC BY 4.0](https://img.shields.io/badge/licence-CC%20BY%204.0-6B7280?style=flat-square)](https://github.com/ElMatiOfficial/kaggle-solutions/blob/main/LICENSE)

**[kaggle-solutions](https://github.com/ElMatiOfficial/kaggle-solutions)** — a short paper for each of
the 20 competitions I have finished, and an attribution ledger that grades them. Every final
submission was diffed against the public notebook it came from with `difflib.SequenceMatcher`.

The measured record, published before anyone asked for it: [**6 verbatim copies at similarity 1.000,
5 derived, 5 substantially original, 3 teammate-authored, and 1 derived solution carrying original
analysis**](https://github.com/ElMatiOfficial/kaggle-solutions/blob/main/PROVENANCE.md). All three
medals — one silver, two bronze — came from the copied or derived half, and the ledger names every
upstream author. The five originals are the number I actually care about, and the most transferable
work sits in entries that finished *lower*: [hysteresis mask fusion on
Vesuvius](https://github.com/ElMatiOfficial/kaggle-solutions/blob/main/writeups/11-vesuvius-surface-detection.md)
(private 0.56159 against public 0.55264), Gene Ontology DAG propagation on
[CAFA 6](https://github.com/ElMatiOfficial/kaggle-solutions/blob/main/writeups/16-cafa-6-protein-function.md),
400 per-task ONNX networks on
[NeuroGolf](https://github.com/ElMatiOfficial/kaggle-solutions/blob/main/writeups/12-neurogolf-2026.md).

<details>
<summary><b>How the ledger was built</b> — four steps and a stated threshold</summary>

<br>

1. Identify the submission that **actually counted** — pulled from Kaggle's internal API
   (`team.privateLeaderboardSubmissionId`), the one scored on the private leaderboard, not the
   best-ever and not the most recent.
2. Retrieve its source notebook with `kaggle kernels pull`.
3. Search for a public original by title, distinctive constants, and in-notebook credits.
4. Reduce both notebooks to non-empty stripped code lines and diff them with
   `difflib.SequenceMatcher`, reporting a similarity ratio plus added and removed line counts.

Similarity ≥ 0.99 is classified as a verbatim copy. The ledger reports measurements, not
impressions, and the method is written out so the numbers can be reproduced against my public
Kaggle account.

</details>

### 02 · The maths tool I built for agents mostly does not get used

[![CI](https://img.shields.io/github/actions/workflow/status/ElMatiOfficial/EML-Mathematical-Translator-for-AI/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/ElMatiOfficial/EML-Mathematical-Translator-for-AI/actions/workflows/ci.yml)
[![Licence: MIT](https://img.shields.io/badge/licence-MIT-6B7280?style=flat-square)](https://github.com/ElMatiOfficial/EML-Mathematical-Translator-for-AI/blob/main/LICENSE)

**[EML-Mathematical-Translator-for-AI](https://github.com/ElMatiOfficial/EML-Mathematical-Translator-for-AI)** —
translates expressions to and from Exp-Minus-Log trees, the single binary operator
[Odrzywołek, arXiv:2603.21852](https://arxiv.org/abs/2603.21852) showed is sufficient to express
every elementary function. The [116-test
suite](https://github.com/ElMatiOfficial/EML-Mathematical-Translator-for-AI/actions/workflows/ci.yml)
runs on Python 3.9 through 3.13 on every push, with macOS and Windows spot-checks. Install from
source — it is not on PyPI.

Then I wired the operations into Claude as tool-use tools and measured whether the agent got better
at mathematics. [It mostly did
not](https://github.com/ElMatiOfficial/EML-Mathematical-Translator-for-AI#what-happened-when-i-actually-tested-that):
on calculus and algebra the agent routes around EML into `sympy`, for a reason that is mechanical
rather than mysterious — multiplication's EML tree is K=41, sine and cosine exceed K=100, π is
K=193, so past the paper's short identities a pure-EML route is not worth taking. That result sits
in the README *above* the install instructions. The library is an exact translator and a complexity
metric, not a reasoning substrate, and saying so is more useful than shipping the hypothesis
unlabelled.

### 03 · If the person on the call cannot produce a fresh code, they are not who they claim to be

[![CI](https://img.shields.io/github/actions/workflow/status/ElMatiOfficial/realh/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/ElMatiOfficial/realh/actions/workflows/ci.yml)
[![CodeQL](https://img.shields.io/github/actions/workflow/status/ElMatiOfficial/realh/codeql.yml?branch=main&style=flat-square&label=CodeQL)](https://github.com/ElMatiOfficial/realh/actions/workflows/codeql.yml)
[![Secret scan](https://img.shields.io/github/actions/workflow/status/ElMatiOfficial/realh/gitleaks.yml?branch=main&style=flat-square&label=secret%20scan)](https://github.com/ElMatiOfficial/realh/actions/workflows/gitleaks.yml)
[![Licence: Apache 2.0](https://img.shields.io/badge/licence-Apache%202.0-6B7280?style=flat-square)](https://github.com/ElMatiOfficial/realh/blob/main/LICENSE)

**[realh](https://github.com/ElMatiOfficial/realh)** — proof of personhood and content provenance,
built for the deepfake-CEO call. A verified user mints a single-use code that expires in 120 seconds
and passes it over any channel; anyone can check it on a public page with no account. Codes are
stored hash-only and consumed atomically, so a replay raises a loud *already used*. Underneath:
W3C Verifiable Credentials signed with Ed25519, a `did:web` document and a public JWKS, so a relying
party can verify **offline, without trusting the issuer at runtime**. TypeScript, thirteen months of
commits, with CodeQL and secret scanning on every push.

The README opens with four specific reasons **not** to run it in production — a mock identity
provider, signing keys on disk instead of a KMS, `JSON.stringify` where RFC 8785 canonical JSON
belongs, and no revocation path — because a reference implementation that hides its threat model is
worse than none. The third has [its own decision
record](https://github.com/ElMatiOfficial/realh/blob/main/docs/decisions/001-jcs-canonicalization.md):
trade-offs argued in writing rather than left in a commit message.

### 04 · A chain filter you cannot argue with is a filter you have to take on faith

[![CI](https://img.shields.io/github/actions/workflow/status/ElMatiOfficial/barrio-mapper/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/ElMatiOfficial/barrio-mapper/actions/workflows/ci.yml)
[![Live demo](https://img.shields.io/badge/live%20demo-runs%20in%20your%20browser-0F766E?style=flat-square&logo=openstreetmap&logoColor=white)](https://elmatiofficial.github.io/barrio-mapper/)
[![Licence: MIT](https://img.shields.io/badge/licence-MIT-6B7280?style=flat-square)](https://github.com/ElMatiOfficial/barrio-mapper/blob/main/LICENSE)

**[barrio-mapper](https://github.com/ElMatiOfficial/barrio-mapper)** — pulls the small, independently
owned businesses of a neighbourhood out of OpenStreetMap — tiendas, droguerías, ferreterías,
talleres — and removes the chains with three independent signals: brand tags, a name blacklist, and
a frequency heuristic. "Chain" is a judgement call, so every rejected POI is written to
`rejected_chains.csv` **with the reason it was rejected**. You can audit what the filter threw away
rather than only what it kept, and whitelist the local mini-chain it got wrong. Tested end to end on
Medellín; a Python CLI plus [a version that runs entirely in your
browser](https://elmatiofficial.github.io/barrio-mapper/).

---

## Verification index

Seven claims made on this page, and the artefact where a stranger can falsify each one.

| # | Claim | Where it is checked |
|:--|:--|:--|
| 1 | 6 verbatim · 5 derived · 5 substantially original · 3 teammate-authored · 1 mixed, across 20 finished competitions — measured with `difflib`, not asserted | [PROVENANCE.md](https://github.com/ElMatiOfficial/kaggle-solutions/blob/main/PROVENANCE.md) |
| 2 | My own Vesuvius method generalised: private **0.56159** beat public **0.55264** | [Vesuvius write-up](https://github.com/ElMatiOfficial/kaggle-solutions/blob/main/writeups/11-vesuvius-surface-detection.md) |
| 3 | corr(public, private) = **−0.037** across 35 scored draws of one solution — public-leaderboard tuning measured as noise | [ROGII write-up](https://github.com/ElMatiOfficial/kaggle-solutions/blob/main/writeups/20-rogii-wellbore-geology.md) · [published on Kaggle](https://www.kaggle.com/competitions/rogii-wellbore-geology-prediction/writeups/608th-place-35-submissions-of-one-solution-corr) |
| 4 | A design decision written down with its trade-offs instead of buried in a commit message | [ADR 001, JCS canonicalisation](https://github.com/ElMatiOfficial/realh/blob/main/docs/decisions/001-jcs-canonicalization.md) |
| 5 | 116 tests, green across Python 3.9–3.13 and on Linux, macOS and Windows | [EML CI runs](https://github.com/ElMatiOfficial/EML-Mathematical-Translator-for-AI/actions/workflows/ci.yml) |
| 6 | A negative result published in the project's own README, above the install instructions | [What happened when I actually tested it](https://github.com/ElMatiOfficial/EML-Mathematical-Translator-for-AI#what-happened-when-i-actually-tested-that) |
| 7 | Kaggle Competitions Expert, ranked 1,095 of 210,960 | [kaggle.com/sebastianmateus](https://www.kaggle.com/sebastianmateus) |

---

## What I work on

| Area | In practice |
|:--|:--|
| **Foundation models** | Pre-training on customer transaction sequences at Nequi — sequence modelling of financial behaviour, and what the learned representations actually encode |
| **Credit risk** | PD and LGD · loss-rate forecasting · IV/WoE · Platt calibration · SHAP-driven adverse-action reasons |
| **Agent security** | Multi-step tool-use attacks and defences · [tool designs measured rather than assumed](https://github.com/ElMatiOfficial/EML-Mathematical-Translator-for-AI#what-happened-when-i-actually-tested-that) |
| **LLM evaluation** | Leaderboard variance and selection error — [one controlled measurement](https://github.com/ElMatiOfficial/kaggle-solutions/blob/main/writeups/20-rogii-wellbore-geology.md) puts corr(public, private) at −0.037 across 35 draws of a single solution |
| **Program induction** | ARC — [ARC Prize 2025 write-up](https://github.com/ElMatiOfficial/kaggle-solutions/blob/main/writeups/03-arc-prize-2025.md) |
| **3D segmentation** | [Vesuvius Challenge](https://github.com/ElMatiOfficial/kaggle-solutions/blob/main/writeups/11-vesuvius-surface-detection.md) — own method, hysteresis mask fusion |
| **Stack** | Python · SQL · PyTorch · scikit-learn · XGBoost · LightGBM · Hugging Face · BigQuery · dbt · Airflow · FastAPI · MLflow · AWS · Docker · Terraform · GitHub Actions |

---

## Elsewhere

| Where | What |
|:--|:--|
| **Portfolio** | [elmatiofficial.github.io](https://elmatiofficial.github.io) — hand-built, trilingual |
| **Kaggle** | [sebastianmateus](https://www.kaggle.com/sebastianmateus) — Competitions Expert, ranked 1,095 of 210,960 · every finished competition [written up and attributed](https://github.com/ElMatiOfficial/kaggle-solutions/blob/main/PROVENANCE.md) |
| **LinkedIn** | [sebastianmateusperdomo](https://www.linkedin.com/in/sebastianmateusperdomo/) |
| **TEDx** | [Talk on YouTube](https://www.youtube.com/watch?v=RivKU85N9gw) |

---

<div align="center">

Trilingual ES / EN / PT · based in Colombia · every claim on this page links to the thing that checks it.

</div>
