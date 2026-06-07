# SmoothConv & DuplexConv: Twin Conversational Datasets for Full-Duplex Human–AI Interaction

[![arXiv](https://img.shields.io/badge/arXiv-Paper-COLOR.svg)]()   [![hf](https://img.shields.io/badge/%F0%9F%A4%97%20HuggingFace-Dataset-yellow)]()   [![GitHub](https://img.shields.io/badge/GitHub-Repo-green)](https://github.com/qualialabsAI/SmoothConv)

This is the official repository for the **SmoothConv** and **DuplexConv** twin datasets, co-developed by the **ASLP Laboratory of Northwestern Polytechnical University (NWPU)** and **Shanghai Vocal Matrix Technology Co., Ltd.**

This data suite offers **2,100+ hours** of real-world, unscripted Chinese long-form conversational audio. It is specifically designed to advance research on next-generation Speech LLMs and full-duplex spoken dialogue systems—enabling models to achieve human-like turn-taking, real-time interruption handling, and continuous stream perception.

---

## News 🔥

- **2026/06**: 🚀 We officially open-source the full **SmoothConv (100h human-verified)** and **DuplexConv (2,000h LLM-annotated)** twin datasets.
- **2025/04/06**: Released the **[FastTurn Test Set](https://huggingface.co/datasets/ASLP-lab/FastTurn-Testset)**, built upon the SmoothConv small set, for turn-state prediction evaluation.
- **2025/03/24**: Initial public release of the SmoothConv small set.

---

## Download 📥

* **SmoothConv (100h / Expert-Annotated)**: [HuggingFace Dataset Link]
* **DuplexConv (2,000h / LLM-Annotated)**: [HuggingFace Dataset Link]
* **FastTurn Testset**: [FastTurn-Testset](https://huggingface.co/datasets/ASLP-lab/FastTurn-Testset)

---

## Dataset Overview ⭐️

Unlike traditional speech corpora that rely on studio readings, single-channel mixed tracks, or scripted scenarios, this suite features **true multi-channel recordings of real-world, unscripted Chinese natural conversations** (covering deep educational verticals and open-domain interactions). 

The suite provides two complementary annotation modes from identical or cognate natural conversation sources to serve both fine-tuning and large-scale pre-training:

### 1️⃣ SmoothConv (100 Hours — Expert Human Annotation)
Designed as a high-precision interactive benchmark and fine-tuning asset. It captures micro-dynamics of human interaction through dense, multi-dimensional human verification:
- **Millisecond-level Segment Alignment**: High-accuracy ASR transcripts aligned perfectly at the segment/turn boundaries.
- **Turn-taking & Overlap Dynamics**: Clear markings of speaker transitions and speech overlaps, essential for modeling endpoint detection (VAD) and turn prediction.
- **Acoustic Events & Pauses**: Granular labels for non-verbal behaviors like laughter, coughing, sighing, and pauses.
- **Fine-grained Attributes**: Explicit tags for speaker gender and dynamic emotional states.

### 2️⃣ DuplexConv (2,000 Hours — Large-scale LLM Automation)
Built to satisfy the massive data appetite of Speech LLM pre-training. It leverages a cutting-edge data engineering pipeline driven by advanced LLMs to generate extensive training data:
- **Massive Pre-training Supply**: 2,000 hours of natural multi-turn context for robust speech representation and Self-Supervised Learning (SSL).
- **Rich Paralinguistic Enrichment**: Automated deep semantic and multi-modal environment parsing, delivering global atmosphere, vocal tones, and emotional undertones.

---

## Dataset Statistics 📦

### Global Overview

| Metrics | 🥇 SmoothConv (Human Fine-Tuning) | 🥈 DuplexConv (LLM Pre-Training) |
| :--- | :---: | :---: |
| **Language** | Chinese (zh) | Chinese (zh) |
| **Total Audio Duration** | **100.53 hours** | **2000.21 hours** |
| **Total Audio Files** | 2,503 | 93,709 |
| **Mean Duration** | 144.59 sec | 76.84 sec |
| **Duration Range (Min - Max)** | 60.0 sec - 634.7 sec | 8.0 sec - 618.3 sec |

### FastTurn Test Set
To evaluate turn-state prediction, we construct a dedicated evaluation set consisting of segments from real-world data and 1,000 synthetically generated **wait** state samples (synthesized using DeepSeek V3 for text and IndexTTS2 for audio).

| Turn State  | Source      | Samples | Duration (h) |
|-------------|-------------|--------:|-------------:|
| Complete    | real-world  | 14709   | 9.64         |
| Incomplete  | real-world  | 3643    | 2.15         |
| Backchannel | real-world  | 3080    | 0.42         |
| Wait        | synthesized | 1000    | 0.71         |

For more details, please refer to the [FastTurn repository](https://github.com/ASLP-lab/FastTurn).

---

## Dataset Statistics 📦

### SmoothConv

The final release of **SmoothConv** will include approximately **150 hours** of real-world conversational audio. Broadly, the dataset is divided into two categories: **educational** and **non-educational** conversations. To support turn-taking research, the dataset further includes four turn-taking labels: **complete**, **incomplete**, **backchannel**, and **wait**. More detailed statistics, annotation protocols, and data descriptions will be released together with the full dataset.
<!-- 
| Split | # Conversations | Duration (hours) | 
|:-----:|----------------:|-----------------:|
| Total | XXX | XXX | XXX | XXX | XXX | XXX | -->

### FastTurn Test Set

To evaluate turn-state prediction, we construct an evaluation set consisting of segments from real-world data and 1,000 synthetically generated **wait** state samples. Since the **wait** state is rare in natural conversations, we supplement the set with synthesized samples generated using DeepSeek V3 for text generation and IndexTTS2 for audio synthesis.

| Turn State  | Source      | Samples | Duration (h) |
|-------------|-------------|--------:|-------------:|
| Complete    | real-world  | 14709   | 9.64         |
| Incomplete  | real-world  | 3643    | 2.15         |
| Backchannel | real-world  | 3080    | 0.42         |
| Wait        | synthesized | 1000    | 0.71         |

For more details about the FastTurn Test Set, please refer to the [FastTurn repository](https://github.com/ASLP-lab/FastTurn).

---

## 📜 License

This dataset is released under the Creative Commons Attribution 4.0 International (CC-BY 4.0) License.

For more details: https://creativecommons.org/licenses/by/4.0/

---

## 📖 Citation

If you use SmoothConv in your research, please cite:

@misc{smoothconv,
  author = {qulialabs}，title={SmoothConv: Datasets for Smooth Human–AI Conversational Interaction},
  year={2025},publisher = {GitHub},journal = {GitHub repository},howpublished = {https://github.com/qulialabs-ethan/SmoothConv},email = {developer@qulialabs.ai}
}
