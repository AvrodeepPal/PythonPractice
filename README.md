<h1 align="center">Avrodeep Pal</h1>

<div align="center">

![Typing SVG](https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=22&duration=3500&pause=1000&color=00D9FF&center=true&vCenter=true&width=680&lines=I+build+ML+systems+that+survive+contact+with+reality;RAG+pipelines%2C+fraud+models%2C+cross-lingual+NLP;GPT-2+from+raw+tensors%2C+because+I+had+to+be+sure;Powered+by+black+tea+and+3+AM+stubbornness)

[![Portfolio](https://img.shields.io/badge/Portfolio-FF5722?style=for-the-badge&logo=vercel&logoColor=white)](https://avrodeeppal-portfolio.vercel.app/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/avrodeeppal)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:avrodeep.pal17@gmail.com)

![Profile Views](https://komarev.com/ghpvc/?username=AvrodeepPal&label=Profile%20views&color=00d9ff&style=flat-square)
![Followers](https://img.shields.io/github/followers/AvrodeepPal?label=Followers&style=flat-square&color=00d9ff&labelColor=black)

</div>

---

## 👋 Hey there

I'm an **MCA graduate from Jadavpur University** who got interested in machine learning for an unglamorous reason: I wanted to know *why* the model said yes. That question pulled me through credit risk scorecards, adversarial fraud systems, and eventually into building GPT-2 from raw tensors just to prove to myself I understood attention.

Most of my work lives where **ML has consequences** — loan decisions, fraud flags, language that doesn't translate cleanly. Those problems punish you for shipping a notebook and calling it a system, which is exactly why I like them.

I also believe good engineering is mostly restraint. My RAG backend has no agents in it. Not because agents are bad — because I couldn't yet justify one.

<table>
<tr>
<td>🎓 <b>MCA</b>, Jadavpur University — First Class, 8.90/10</td>
<td>🥇 <b>Rank 1</b>, WBSU (BSc CS) — 9.91/10</td>
</tr>
<tr>
<td>🥈 <b>Rank 2</b>, WB-JECA (state MCA entrance)</td>
<td>⭐ <b>5★</b> Problem Solver, HackerRank</td>
</tr>
</table>

---

## 📊 A Few Numbers

<div align="center">

| 590K+ | 51K+ | 23,544 |
|:---:|:---:|:---:|
| transactions modelled for fraud | loan applications risk-scored | idioms embedded across 3 languages |

| 15 | 54 | 3× |
|:---:|:---:|:---:|
| notebooks building GPT-2 from scratch | architecture notes written along the way | faster placement outreach, in production |

</div>

---

## 🛠️ Things I've Built

### 🤖 [AStarBot](https://github.com/AvrodeepPal/AStarBot) · *RAG backend that refuses to be clever*
The AI assistant behind my portfolio. Every factual answer comes from retrieval or it doesn't get said.

The interesting constraint was memory: instead of Redis sessions, the client carries a rolling summary and the backend rewrites it when the window overflows. Stateless, horizontally scalable, and you can read the entire memory state as a string. Three separate models handle answering, fallback, and summarization — so a rate limit degrades quality instead of killing the service.

`Python` · `FastAPI` · `Pinecone` · `Docker`

### 🕵️ [Fraud_Detection_Analysis](https://github.com/AvrodeepPal/Fraud_Detection_Analysis) · *IEEE-CIS, 590K transactions*
Fraud is rare, adversarial, and time-dependent — which makes accuracy an actively misleading metric at a 3.5% base rate.

So I built it like a risk system, not a Kaggle entry: chronological splits to kill temporal leakage, engineered pseudo-identities and velocity features to catch bursty automation, SHAP for per-transaction auditability, and cost-sensitive thresholds because a missed fraud costs far more than a false alarm. Added PSI drift monitoring so the model tells you when it's gone stale. **PR-AUC ~0.54** from a LightGBM/XGBoost/CatBoost ensemble.

`Python` · `LightGBM` · `SHAP` · `PSI Monitoring`

### 🏦 [Credit_Risk_Analysis](https://github.com/AvrodeepPal/Credit_Risk_Analysis) · *51K loan applications, 87 features*
Four-tier risk classification (P1–P4) on a badly imbalanced target, where the smallest class is the one you most need to get right.

ANOVA F-tests cut the feature set by 55% with no loss in signal. I trained eight algorithms, then spent longer on the imbalance strategy than the models — sample weighting vs. SMOTE-Tomek changes the answer more than swapping XGBoost for CatBoost does. A stacking ensemble won on macro-F1 and balanced accuracy.

`Python` · `scikit-learn` · `XGBoost` · `CatBoost`

### 🌐 [Cross-Lingual Bengali Idiom Matching](https://github.com/AvrodeepPal/Cross-Lingual-Bengali-Idiom-Matching-Using-Multilingual-Sentence-Embeddings-Without-Translation) · *MCA thesis*
"আকাশ কুসুম" literally means *sky flower*. It means an impossible dream. Can a multilingual embedder figure that out across Bengali, English, and Hindi — with **no translation step**?

I built a 23K+ idiom triplet dataset from scratch and benchmarked mSBERT, LaBSE, BanglaBERT, and XLM-R across similarity, retrieval, and clustering. The fun part: XLM-R scored a near-perfect 0.993 mean cosine similarity — and was completely useless. Every vector had collapsed to nearly the same point (σ ≈ 0.003). LaBSE, with far humbler scores, was the only model doing real cross-lingual work.

*Best lesson of my degree: a beautiful number is a hypothesis, not a result.*

`Sentence-Transformers` · `Transformers` · Supervised by Prof. Diganta Saha, Dept. of CSE, JU

### 🧠 [LLMsPractice](https://github.com/AvrodeepPal/LLMsPractice) · *Transformers, no training wheels*
A first-principles walk from character-level RNNs to a working GPT-2 — custom BPE, causal masks, multi-head attention, Pre-LN blocks, pretraining loop, then loading real OpenAI weights into my own modules.

15 build notebooks and 54 architecture notes, written because I kept nodding along to explanations I couldn't actually reproduce. Now I can.

`PyTorch` · `TensorFlow` · `HuggingFace`

### 🎪 [LetsConnect](https://github.com/AvrodeepPal/LetsConnect) · *AI recruitment outreach, [live](https://letsconnect-jumca2026.streamlit.app/)*
Campus placement emails are copy-pasted, impersonal, and enormously time-consuming. This generates outreach tailored to each company's domain and culture, with OTP-secured multi-coordinator workflows.

Used by my university's placement cell: **3× faster** outreach, 90%+ coordinator satisfaction. Built for people who are not engineers, which changed almost every design decision — every generated email is editable and previewed before it sends, because automation people can't override is automation they won't trust.

`Streamlit` · `Mistral` · `Supabase`

### 📈 [Time_Series_Analysis_LSTM](https://github.com/AvrodeepPal/Time_Series_Analysis_LSTM) · *ReLU vs GELU, settled properly*
Everyone says GELU is better. I wanted the receipts — so: identical LSTM architecture, identical splits, identical hyperparameters, two activations, and a full RMSE/MAE/MAPE/R² comparison plus 30-day forecasts and error distributions.

Feature engineering carried more weight than the activation choice did, which is its own useful finding. Documented with a loud disclaimer, because a stock model that backtests well is still not financial advice.

`TensorFlow` · `LSTM` · `Technical Indicators`

---

## 🧱 Outside the ML Stack

I'm not only a notebook person. I've built and shipped **Spring Boot REST APIs** with JWT auth and layered service architectures, **Java desktop applications** backed by relational schemas I designed myself, and **React/Next.js frontends** with animation and 3D work when a project deserved a face.

That background is why my ML work leans toward systems thinking. Knowing what it takes to run something in production changes what you're willing to call "done."

I'm also comfortable in the analyst's toolkit — SQL, Excel, and Power BI — because a good chunk of real data work happens before anything reaches a model.

---

## 🧰 What I Work With

**Languages** ![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white) ![Java](https://img.shields.io/badge/-Java-007396?style=flat-square&logo=openjdk&logoColor=white) ![JavaScript](https://img.shields.io/badge/-JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black) ![SQL](https://img.shields.io/badge/-SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)

**ML & AI** ![PyTorch](https://img.shields.io/badge/-PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white) ![TensorFlow](https://img.shields.io/badge/-TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white) ![scikit-learn](https://img.shields.io/badge/-scikit--learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white) ![HuggingFace](https://img.shields.io/badge/-HuggingFace-FFD21E?style=flat-square&logo=huggingface&logoColor=black) ![Pinecone](https://img.shields.io/badge/-Pinecone-000000?style=flat-square&logo=pinecone&logoColor=white)

**Backend & Data** ![FastAPI](https://img.shields.io/badge/-FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white) ![Spring Boot](https://img.shields.io/badge/-Spring%20Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white) ![Pandas](https://img.shields.io/badge/-Pandas-150458?style=flat-square&logo=pandas&logoColor=white) ![MySQL](https://img.shields.io/badge/-MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white) ![Docker](https://img.shields.io/badge/-Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

**Frontend** ![React](https://img.shields.io/badge/-React-61DAFB?style=flat-square&logo=react&logoColor=black) ![Next.js](https://img.shields.io/badge/-Next.js-000000?style=flat-square&logo=next.js&logoColor=white) ![Tailwind](https://img.shields.io/badge/-Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)

---

## ✍️ I Write Things Down

A habit that's quietly become the most useful one I have — if I can't explain a thing in writing, I don't understand it yet.

- **54 architecture notes** alongside my transformer builds, covering everything from BPE merge rules to why Pre-LayerNorm stabilizes deep stacks
- **A full technical guide to the OWASP Top 10 for LLM Applications** — attack mechanics, threat modelling, and mitigations for prompt injection, insecure output handling, and supply-chain risk
- **Infrastructure write-ups** documenting my self-hosted setup — WireGuard tunnels, NAT traversal, remote access without port forwarding
- **Research documentation** for my thesis: reproducible pipelines, a resumable orchestrator, and an evaluation framework someone else could actually rerun

It also makes me a better teammate. Reviewers shouldn't have to reverse-engineer intent from code.

---

## 🎯 What I'm After Next

Roles where I own a model end to end — the messy EDA at the start, the threshold policy in the middle, and the drift alert at 2 AM six months later. I'm most useful on problems with **real stakes and imperfect data**, and most motivated when the correct answer isn't obvious from the leaderboard.

Actively interested in **Applied ML / Data Science**, **AI Engineering (LLMs & RAG)**, and **Risk & Fraud Analytics**.

What I bring: rigour about evaluation, a bias toward the simplest thing that works, and documentation you won't curse me for.

---

## 💭 Opinions I'll Defend

> **The metric is the design decision.** Choosing PR-AUC over accuracy on imbalanced fraud data isn't a detail — it's the entire framing of the problem.

> **A holdout set is not a deployment.** If there's no drift monitoring and no explainability, you have a model, not a system. Those are different deliverables.

> **Complexity should be earned.** I'll reach for an agent framework the day a deterministic pipeline genuinely stops working, and not one commit sooner.

> **Suspicious results are the interesting ones.** XLM-R's 0.993 similarity score taught me more than any of my successful experiments did.

---

## 🔭 Currently In My Tabs

- 🧠 **Reasoning models** — DeepSeek-R1/V3, chain-of-thought, and why test-time compute sometimes beats more parameters
- 🔌 **MCP** — tool-augmented LLM apps that don't devolve into prompt spaghetti
- 🎯 **RL foundations** — Sutton & Barto, policy gradients, TRPO, working toward alignment techniques from the ground up
- 🛡️ **LLM security** — prompt injection remains genuinely unsolved, and the fact that we ship these systems anyway fascinates me
- 🖥️ **Self-hosting** — running my own services over a WireGuard/Tailscale mesh, mostly to understand what "it works on my machine" really costs

---

## ☕ Off the Clock

Strong black tea, no sugar, usually the third cup by 1 AM. Anime OSTs on loop — I've debugged entire subsystems to the *Edgerunners* soundtrack. Weekend reading splits about evenly between research papers and travel blogs, which I maintain is a balanced diet.

Long-term ambitions, in honest order of priority: a German Shepherd, an ergonomic chair, and AI that makes someone's day genuinely easier.

---

<div align="center">

**Always happy to talk about RAG architectures, fraud modeling, low-resource NLP — or tea.**

[![LeetCode](https://img.shields.io/badge/LeetCode-FFA116?style=flat-square&logo=leetcode&logoColor=black)](https://leetcode.com/AvrodeepPal)
[![HackerRank](https://img.shields.io/badge/HackerRank-2EC866?style=flat-square&logo=hackerrank&logoColor=white)](https://www.hackerrank.com/profile/avrodeep_pal_17)
[![Portfolio](https://img.shields.io/badge/Portfolio-FF5722?style=flat-square&logo=vercel&logoColor=white)](https://avrodeeppal-portfolio.vercel.app/)

*Built one midnight commit at a time* 🌙

</div>
