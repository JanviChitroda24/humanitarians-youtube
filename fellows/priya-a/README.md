# Priya Adlakha

**Role:** AI Research Fellow  
**Project:** Laya & Jev Fine-Tuning Pipeline (RLCD Strategy 1)  
**Organization:** [Humanitarians AI](https://www.humanitarians.ai) (Iacon Optimus Program — Prof. Nik Bear Brown & Dev Shah)  
**GitHub Profile:** [@adlakhapriya95](https://github.com/adlakhapriya95)  
**Volunteer Repository:** [humanitarians-ai-volunteer](https://github.com/adlakhapriya95/humanitarians-ai-volunteer)  
**Collaborative Project Repository:** [AmeyaPadwad/fine_tuner (`kaggle_benchmarking`)](https://github.com/AmeyaPadwad/fine_tuner/tree/kaggle_benchmarking)  
**Fellows Submission PR:** [#232 on `nikbearbrown/humanitarians-youtube`](https://github.com/nikbearbrown/humanitarians-youtube/pull/232)  

---

## 🏆 Master Cross-Model Empirical Benchmark Suite

Consolidated evaluation across all **4 decision model families** and **6 benchmark datasets**, trained with **Reinforcement Learning with Calibrated Decisions (RLCD Strategy 1: Negative Brier Score Reward $R = -(p - y)^2$)** evaluated on strictly held-out 20% test splits:

| Model Family | Backbone Architecture | Benchmark Dataset | Decision Primitive | Evaluation Hardware | Dataset Size (Train / Test) | Baseline $\to$ Final Accuracy | Mean Brier Score ($\Delta$) | Expected Calibration Error ($\Delta$) |
| :--- | :--- | :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| **`Laya (421M)`** | ModernBERT-large (Bidirectional) | **Salesforce xLAM** | `choice` (Tools) | Colab T4 GPU | **$60,000$** ($47,940$ / $12,000$) | **$84.85\% \to \mathbf{99.10\%}$** ($\mathbf{+14.25\%}$) | **$-0.2505 \to \mathbf{-0.0168}$** ($\mathbf{+0.2337}$) | **$9.98\% \to \mathbf{0.83\%}$** ($\mathbf{-9.15\%}$, sub-1%) |
| **`Laya (421M)`** | ModernBERT-large (Bidirectional) | **Clinical Triage** | `choice` (Urgency) | Local CPU | $60$ ($42$ / $12$) | **$100.00\% \to \mathbf{100.00\%}$** | **$-0.0038 \to \mathbf{-0.0000}$** | **$3.11\% \to \mathbf{0.00\%}$** ($\mathbf{-3.11\%}$, zero ECE) |
| **`Von`** | Native Von Option Markers | **Toxic-Chat** | `score` (Continuous) | Kaggle 2x T4 | $5,082$ ($4,046$ / $1,016$) | **$45.37\% \to \mathbf{95.57\%}$** ($\mathbf{+50.20\%}$) | **$-0.7328 \to \mathbf{-0.0778}$** ($\mathbf{+0.6550}$) | **$18.99\% \to \mathbf{3.45\%}$** ($\mathbf{-15.54\%}$) |
| **`Von`** | Native Von Option Markers | **NexusRaven** | `choice` (Code API) | Kaggle 2x T4 | $318$ ($235$ / $63$) | **$25.40\% \to \mathbf{92.06\%}$** ($\mathbf{+66.67\%}$) | **$-0.7623 \to \mathbf{-0.1367}$** ($\mathbf{+0.6256}$) | **$9.72\% \to \mathbf{6.66\%}$** ($\mathbf{-3.06\%}$) |
| **`Von`** | Native Von Option Markers | **Tweet Sentiment** | `choice` (3-class) | Kaggle 2x T4 | $26,732$ ($21,366$ / $5,346$) | **$41.00\% \to \mathbf{79.74\%}$** ($\mathbf{+38.74\%}$) | **$-0.6264 \to \mathbf{-0.3746}$** ($\mathbf{+0.2518}$) | **$8.98\% \to 18.12\%$** |
| **`Von`** | Native Von Option Markers | **Anthropic RLHF** | `noul` (Preference) | Kaggle 2x T4 | **$60,000$** ($47,980$ / $12,000$) | **$50.16\% \to \mathbf{62.31\%}$** ($\mathbf{+12.15\%}$) | **$-0.5088 \to -0.5219$** | **$6.49\% \to 17.15\%$** |
| **`Decision 1.0`** | Lex Architecture Backbone ($600\text{M}$) | **Toxic-Chat** | `score` (Continuous) | Kaggle 2x T4 | $5,082$ ($4,046$ / $1,016$) | **$9.65\% \to \mathbf{94.98\%}$** ($\mathbf{+85.33\%}$) | **$-0.8272 \to \mathbf{-0.0876}$** ($\mathbf{+0.7396}$) | **$14.78\% \to \mathbf{4.01\%}$** ($\mathbf{-10.77\%}$) |
| **`Decision 1.0`** | Lex Architecture Backbone ($600\text{M}$) | **Tweet Sentiment** | `choice` (3-class) | Kaggle 2x T4 | $26,732$ ($21,366$ / $5,346$) | **$46.54\% \to \mathbf{79.50\%}$** ($\mathbf{+32.96\%}$) | **$-0.6357 \to \mathbf{-0.3687}$** ($\mathbf{+0.2670}$) | **$8.04\% \to 17.38\%$** |
| **`Decision 1.0`** | Lex Architecture Backbone ($600\text{M}$) | **Anthropic RLHF** | `noul` (Preference) | Kaggle 2x T4 | **$60,000$** ($47,980$ / $12,000$) | **$49.14\% \to \mathbf{57.13\%}$** ($\mathbf{+7.98\%}$) | **$-0.5132 \to \mathbf{-0.4894}$** ($\mathbf{+0.0238}$) | **$6.77\% \to \mathbf{4.45\%}$** ($\mathbf{-2.32\%}$) |
| **`Decision 1.0`** | Lex Architecture Backbone ($600\text{M}$) | **NexusRaven** | `choice` (Code API) | Kaggle 2x T4 | $318$ ($235$ / $63$) | **$25.40\% \to \mathbf{58.73\%}$** ($\mathbf{+33.33\%}$) | **$-0.7754 \to \mathbf{-0.5430}$** ($\mathbf{+0.2324}$) | **$17.84\% \to \mathbf{12.48\%}$** ($\mathbf{-5.36\%}$) |
| **`Typical-small`** | Qwen Autoregressive Backbone ($\sim 150\text{M}$) | **Toxic-Chat** | `score` (Continuous) | Kaggle 2x T4 | $5,082$ ($4,046$ / $1,016$) | **$0.39\% \to \mathbf{94.88\%}$** ($\mathbf{+94.49\%}$) | **$-0.9301 \to \mathbf{-0.1024}$** ($\mathbf{+0.8277}$) | **$25.78\% \to \mathbf{5.11\%}$** ($\mathbf{-20.67\%}$) |
| **`Typical-small`** | Qwen Autoregressive Backbone ($\sim 150\text{M}$) | **Tweet Sentiment** | `choice` (3-class) | Kaggle 2x T4 | $26,732$ ($21,366$ / $5,346$) | **$39.54\% \to \mathbf{39.54\%}$** | **$-0.6715 \to \mathbf{-0.6603}$** ($+0.0111$) | **$8.63\% \to \mathbf{0.50\%}$** ($\mathbf{-8.13\%}$, sub-1%) |
| **`Typical-small`** | Qwen Autoregressive Backbone ($\sim 150\text{M}$) | **Anthropic RLHF** | `noul` (Preference) | Kaggle 2x T4 | **$60,000$** ($47,980$ / $12,000$) | **$50.21\% \to \mathbf{49.79\%}$** | **$-0.5044 \to \mathbf{-0.5000}$** ($+0.0043$) | **$4.67\% \to \mathbf{0.36\%}$** ($\mathbf{-4.31\%}$, sub-0.5%) |
| **`Typical-small`** | Qwen Autoregressive Backbone ($\sim 150\text{M}$) | **NexusRaven** | `choice` (Code API) | Kaggle 2x T4 | $318$ ($235$ / $63$) | **$15.87\% \to \mathbf{15.87\%}$** | **$-0.9074 \to \mathbf{-0.8007}$** ($\mathbf{+0.1067}$) | **$31.14\% \to \mathbf{15.48\%}$** ($\mathbf{-15.66\%}$) |

---

## 🔬 Core Scientific Findings

1. **Laya (ModernBERT 421M):** Evaluated across 60,000 Salesforce xLAM items, achieving **$99.10\%$ test accuracy**, **$99.11\%$ F1**, and reducing Expected Calibration Error to **$0.83\%$** (sub-1%).
2. **Von (`wfzyx/von`):** Surged by **$+66.67\%$ on NexusRaven** ($25.40\% \to 92.06\%$) and **$+50.20\%$ on Toxic-Chat** ($45.37\% \to 95.57\%$), with **$79.74\%$** accuracy on Tweet Sentiment.
3. **Decision 1.0 (`vllm-sr/Decision-1.0-Lex-0.6B`):** Surged by **$+85.33\%$ on Toxic-Chat** ($9.65\% \to 94.98\%$) and **$+32.96\%$ on Tweet Sentiment** ($46.54\% \to 79.50\%$).
4. **Typical-small (`OzLabs/typical-small`):** Forced honest uncertainty through RLCD Strategy 1 Brier scoring, driving ECE down to **$0.50\%$ on Tweet Sentiment** and **$0.36\%$ on Anthropic RLHF**.
5. **Architectural Discovery:** Bidirectional encoders (ModernBERT / Laya / Von) naturally integrate option marker positions, whereas autoregressive backbones (Qwen / Typical) suffer from attention friction when wrapped with synthetic bidirectional marker heads.

---

## 📅 Fellowship Submissions Directory (All 5 Weeks — 92.0 Logged Hours)

1. **[`2026-10-16-multi-model-kaggle-benchmarking/`](2026-10-16-multi-model-kaggle-benchmarking/)** (Week 5 — 20.0 Hours)  
   *Milestone:* Multi-model decision benchmarking (Typical-small, Von, Decision 1.0) on Kaggle 2x T4 GPUs across 4 datasets, modularity audit, and architectural limitation discovery.  
   *Evidence:* [Week 5 Video Update](https://github.com/adlakhapriya95/humanitarians-ai-volunteer/blob/main/videos/JevPipelineUpdate_PriyaA_Week5.mp4) • [`CONSOLIDATED_BENCHMARK_RESULTS.md`](2026-10-16-multi-model-kaggle-benchmarking/CONSOLIDATED_BENCHMARK_RESULTS.md) • [`rlcd_kaggle_benchmark_executed.ipynb`](2026-10-16-multi-model-kaggle-benchmarking/rlcd_kaggle_benchmark_executed.ipynb) • [`FRICTIONAL.md`](2026-10-16-multi-model-kaggle-benchmarking/FRICTIONAL.md)

2. **[`2026-10-07-laya-rlcd-60k-pipeline/`](2026-10-07-laya-rlcd-60k-pipeline/)** (Week 4 — 20.0 Hours)  
   *Milestone:* Full 60,000 dataset training on cloud GPU (NVIDIA T4), 99.10% test accuracy, 0.83% Expected Calibration Error (ECE), ablation study, and universal dataset auto-adapter.  
   *Evidence:* [Week 4 Video Update](https://github.com/adlakhapriya95/humanitarians-ai-volunteer/blob/main/videos/JevPipelineUpdate_PriyaA_Week4.mp4) • [Google Colab Live GPU Run](https://colab.research.google.com/drive/1-f_4z6xMOl80r9vVW6XgYctxtSSg4w3J#scrollTo=FREK-jHrl1_e) • [`PIPELINE_VALIDATION_REPORT.md`](2026-10-07-laya-rlcd-60k-pipeline/PIPELINE_VALIDATION_REPORT.md) • [`FRICTIONAL.md`](2026-10-07-laya-rlcd-60k-pipeline/FRICTIONAL.md)

3. **[`2026-10-02-config-and-test-suite/`](2026-10-02-config-and-test-suite/)** (Week 3 — 20.0 Hours)  
   *Milestone:* Declarative Pydantic configuration engine (`job_config.example.json` / `JobSpec`), 6-tier pyramidal test hierarchy, and 49 automated unit, mathematical, and resilience tests.  
   *Evidence:* [Video Update](https://github.com/adlakhapriya95/humanitarians-ai-volunteer/blob/main/videos/JevPipelineUpdate_PriyaA.mp4) • [`test_plan.md`](2026-10-02-config-and-test-suite/test_plan.md) • [`FRICTIONAL.md`](2026-10-02-config-and-test-suite/FRICTIONAL.md)

4. **[`2026-09-25-jev-scope-and-planning/`](2026-09-25-jev-scope-and-planning/)** (Week 2 — 20.0 Hours)  
   *Milestone:* Jev scope transition, architecture roadmap with Ameya & Dev, and fine-tuning literature research (LlamaIndex, PEFT, TRL).  
   *Evidence:* [Google Docs Roadmap](https://docs.google.com/document/d/12nXlDY-4NEvGuVBvxG8PVNRSjYXtugcE/edit?usp=drive_web&ouid=110294676768764031942&rtpof=true) • [`README.md`](2026-09-25-jev-scope-and-planning/README.md) • [`FRICTIONAL.md`](2026-09-25-jev-scope-and-planning/FRICTIONAL.md)

5. **[`2026-09-18-onboarding-and-gemma-study/`](2026-09-18-onboarding-and-gemma-study/)** (Week 1 — 12.0 Hours)  
   *Milestone:* Onboarding, Optimus setup, research on small decision models, and FunctionGemma 270M study.  
   *Evidence:* [`README.md`](2026-09-18-onboarding-and-gemma-study/README.md) • [`FRICTIONAL.md`](2026-09-18-onboarding-and-gemma-study/FRICTIONAL.md)

---

## 🔗 Live Verification Links

- **Google Colab Full 60K GPU Run (Laya):**  
  [https://colab.research.google.com/drive/1-f_4z6xMOl80r9vVW6XgYctxtSSg4w3J#scrollTo=FREK-jHrl1_e](https://colab.research.google.com/drive/1-f_4z6xMOl80r9vVW6XgYctxtSSg4w3J#scrollTo=FREK-jHrl1_e)
- **Executed Kaggle GPU Notebook (Von):**  
  [`rlcd_kaggle_benchmark_von_executed.ipynb` on GitHub](https://github.com/AmeyaPadwad/fine_tuner/blob/kaggle_benchmarking/rlcd/rlcd_kaggle_benchmark_von_executed.ipynb)
- **Executed Kaggle GPU Notebook (Typical-small):**  
  [`rlcd_kaggle_benchmark_executed.ipynb` on GitHub](https://github.com/AmeyaPadwad/fine_tuner/blob/kaggle_benchmarking/rlcd/rlcd_kaggle_benchmark_executed.ipynb)
- **Shared Fellowship Project Code:**  
  [https://github.com/AmeyaPadwad/fine_tuner/tree/kaggle_benchmarking](https://github.com/AmeyaPadwad/fine_tuner/tree/kaggle_benchmarking)
