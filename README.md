# SmoothConv: A Dual-Channel Conversational Dataset for Smooth Human–AI Interaction
[![arXiv](https://img.shields.io/badge/arXiv-Paper-COLOR.svg)]()  [![hf](https://img.shields.io/badge/%F0%9F%A4%97%20HuggingFace-Dataset-yellow)]()  [![GitHub](https://img.shields.io/badge/GitHub-Repo-green)](https://github.com/qualialabsAI/SmoothConv)

This is the official repository for the **SmoothConv** dataset.

**SmoothConv** is a high-quality dual-channel conversational dataset designed for research on natural and smooth human–AI interaction. The initial release focuses on real human–human conversations with fine-grained conversational structure preserved in timing, overlap, and turn boundaries, providing a natural foundation for modeling turn-taking, interruption handling, response timing, and interaction dynamics in spoken interactive systems.

Unlike many existing conversational resources that rely on single-channel mixed recordings, scripted dialogues, or artificially designed scenarios, SmoothConv provides:

- true dual-channel recordings with separate speaker tracks;
- naturally occurring, unscripted conversations; and
- fine-grained annotations of conversational structure and paralinguistic events.

This makes SmoothConv particularly suitable for building and evaluating systems for conversational turn-taking and real-time spoken interaction.

---

## News 🔥

- **2025/04/06**: We release the **[FastTurn Test Set](https://huggingface.co/datasets/ASLP-lab/FastTurn-Testset)**, built upon the **SmoothConv small set**, for turn-state prediction and evaluation.
- **2025/03/24**: Initial public release of the **SmoothConv small set**.

---

## Download

# Download

The FastTurn Testset is available at:
[https://huggingface.co/datasets/ASLP-lab/FastTurn-Testset](https://huggingface.co/datasets/ASLP-lab/FastTurn-Testset)

---

## Overview ⭐️

This is the official repository for the **SmoothConv** dataset.

**SmoothConv** is a dual-channel conversational dataset built from real human–human conversations, with the goal of supporting research on natural and smooth human–AI interaction. It preserves fine-grained conversational structure, including timing, overlap, and turn boundaries, and therefore provides a realistic basis for modeling turn-taking, interruption handling, response timing, and interaction dynamics in spoken interactive systems.

Compared with many existing conversational resources that rely on single-channel mixed audio, scripted dialogues, or artificially constructed scenarios, SmoothConv provides:

- true dual-channel recordings with separate speaker tracks;
- naturally occurring, unscripted conversations; and
- fine-grained annotations of conversational structure and paralinguistic events.

These properties make SmoothConv a useful resource for building and evaluating systems for conversational turn-taking and real-time spoken interaction.

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
