### Hi, I'm Merve 👋

M.Sc. Data Science student at Dokuz Eylül University (Statistics Department, thesis stage) with a B.Sc. in Electrical and Electronics Engineering. I build machine learning and LLM projects end to end and check whether the results really hold: anomaly detection and risk scoring on meter and sensor data, RAG and tool-calling LLM agents, and image generation experiments. My thesis evaluates open-source 7–8B LLMs and studies how choices such as prompt format, token budget and answer extraction change their scores.

- 🎓 M.Sc. in Data Science @ Dokuz Eylül University (in progress, GPA 3.69) · B.Sc. in Electrical & Electronics Engineering
- 🔬 Thesis: *Statistical Evaluation of Large Language Models' Performance Across Different Tasks* · 8 open-source LLMs on GSM8K, HumanEval and MMLU
- 💼 AI Model Evaluator (RLHF) @ Outlier AI, part-time
- 🧪 AI & Computer Vision Engineer @ Glossa, an early-stage startup project (12/2025 – 07/2026): skin-tone analysis with OpenCV and CIELAB · 1st place, LLM Jetpack Ideathon
- ⚡ Former project engineer in solar energy · 🌍 Top 10, EU-funded E-DATA Project
- ✍️ I write about AI on [Medium](https://medium.com/@mervcaliskaan)
- 🤝 Let's connect on [LinkedIn](https://www.linkedin.com/in/mervecaliskann)

---

### Selected projects

**Machine learning on meter, sensor and sales data**

| Project | What it is | Stack |
|---|---|---|
| [Electricity Theft Detection](https://github.com/Mervecaliskann/electricity-theft-detection) | Risk scoring on daily meter data of 42K customers to prioritize field inspections. ROC-AUC 0.82; the riskiest 20% contain 63% of theft cases. Found and fixed data leakage in the reference pipeline; SHAP explanations and a Power BI dashboard | XGBoost, SHAP, Power BI |
| [Sensor Data Quality Guardrail](https://github.com/Mervecaliskann/smart-sensor-guardrail) | Catches spiking and frozen (stuck) sensors with range, robust Z-score (median/MAD) and stuck-value checks: 30/30 simulated faults caught, 2 false alarms. The SAFE/UNSAFE decision is rule-based; the LLM only explains it. Unit tests | pandas, Streamlit, unittest |
| [Industrial Anomaly Pipeline](https://github.com/Mervecaliskann/industrial-anomaly-pipeline) | PyTorch autoencoder that learns normal operation of simulated temperature, vibration and pressure sensors. Scaler and threshold fit on training data only; on a separate test set it caught all 50 faults (recall 1.00, precision 0.75) | PyTorch, scikit-learn, SQLite, Streamlit |
| [Retail Demand Forecasting](https://github.com/Mervecaliskann/retail-demand-forecasting) | 16-day sales forecasts for 540 store-product series (Kaggle Favorita) with one global LightGBM and a rolling 4-fold backtest: 29.5% lower WAPE than seasonal naive. An inventory simulation turns the forecasts into orders: for a 99.5% fill rate it needs 30% less stock. Leakage controls, SHAP, EN/TR notebook | LightGBM, pandas, SHAP |
| [Explainable Credit Risk Scoring](https://github.com/Mervecaliskann/explainable-credit-risk) | Default-risk model evaluated with KS and Gini, SHAP explanations, LLM-written Turkish rationales and MLflow tracking | XGBoost, SHAP, MLflow |

**LLM systems and evaluation**

| Project | What it is | Stack |
|---|---|---|
| [EU Regulation RAG](https://github.com/Mervecaliskann/eu-regulation-rag) | Q&A over the EU AI Act, GDPR and DORA (311 pages) with article citations. A cross-encoder reranker raised Recall@5 from 84.4% to 93.8%; answers were 87.5% faithful. Showed that a faithful answer can still be wrong when retrieval misses the right article. FastAPI, Docker, CI | FAISS, sentence-transformers, cross-encoder, FastAPI |
| [Responsible AI Banking Agent](https://github.com/Mervecaliskann/responsible-ai-banking-agent) | A tool-calling LangGraph agent with PII redaction (TCKN/IBAN), input/output guardrails, audit logging and a model card: 25/25 adversarial prompts blocked, 7/7 benign requests allowed, 50 tests | LangGraph, Presidio, pytest |
| [Agent Benchmarking Lab](https://github.com/Mervecaliskann/agent-benchmark-pipeline) | Compares a ReAct agent with a fixed-flow LangGraph agent on 14 finance questions (84 runs logged to BigQuery) and tests whether the difference is statistically significant | LangGraph, BigQuery, SciPy |
| [LangGraph Finance Agent](https://github.com/Mervecaliskann/langgraph-finance-agent-langsmith) | Stock analysis agent with LangSmith tracing and an LLM-as-a-judge evaluation by a separate, smaller judge model: 12/14 correct tool selections and a mean judge score of 3.50/5. Both failures were questions that need two tools | LangGraph, LangSmith, Groq |

**Image generation**

| Project | What it is | Stack |
|---|---|---|
| [Interior Render Preservation](https://github.com/Mervecaliskann/interior-render-preservation) | Nine experiments measuring whether Stable Diffusion keeps an interior design (edge recall, CIEDE2000 ΔE, CLIP): ControlNet vs img2img, mask-based floor edits, speed optimizations, exact paint colors, automatic failure detectors checked against my own labels · [live demo](https://huggingface.co/spaces/Mervecaliskan/keep-the-design) · [article](https://medium.com/@mervcaliskaan/does-the-ai-keep-your-design-measuring-geometry-and-color-in-stable-diffusion-interior-renders-43260ec239d3) | Stable Diffusion, ControlNet, SegFormer, Gradio |
| [Japandi Style LoRA](https://github.com/Mervecaliskann/japandi-style-lora) | My own style LoRA for SD 1.5 (17 images, 4.9 min on a free GPU); CLIP style similarity 0.775 → 0.881, combined with ControlNet to restyle a room while keeping its layout · [live demo](https://huggingface.co/spaces/Mervecaliskan/japandi-room-restyle) | Stable Diffusion, LoRA, ControlNet |

---

### Tech I work with

**ML & statistics:** Python · pandas · scikit-learn · XGBoost · LightGBM · SHAP · statsmodels · R
**Deep learning:** PyTorch · TensorFlow/Keras · OpenCV · diffusers · ControlNet · LoRA · SegFormer
**LLMs:** open-source LLM evaluation · LLM-as-a-judge · prompt design · RAG · FAISS · LangGraph · QLoRA/PEFT
**Tools:** SQL · BigQuery · PySpark · MLflow · FastAPI · Docker · Git · GitHub Actions · Streamlit · Gradio · Power BI
