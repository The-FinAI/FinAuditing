<div align="center">

<h1>FinAuditing</h1>

<p><strong>A Financial Taxonomy-Structured Multi-Document Benchmark for Evaluating LLMs</strong></p>

<p>
  <a href="https://arxiv.org/abs/2510.08886"><img src="https://img.shields.io/badge/arXiv-2510.08886-b31b1b.svg" alt="arXiv"></a>
  <img src="https://img.shields.io/badge/SIGIR-2026%20Resource%20Track-blue.svg" alt="SIGIR 2026 Resource Track">
  <a href="https://huggingface.co/collections/TheFinAI/finauditing-taxonomy-structured-auditing-68e5f80606e22454027075e7"><img src="https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Collection-yellow?logo=huggingface" alt="Hugging Face Collection"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-green.svg" alt="License: MIT"></a>
</p>

<p>
  <a href="https://arxiv.org/abs/2510.08886">Paper</a> ·
  <a href="https://huggingface.co/collections/TheFinAI/finauditing-taxonomy-structured-auditing-68e5f80606e22454027075e7">Data</a> ·
  <a href="https://github.com/Yan2266336/FinBen">Evaluation Framework</a>
</p>

</div>

---

## Overview

**FinAuditing** is a taxonomy-aligned, structure-aware benchmark built from real XBRL filings for evaluating whether LLMs can perform professional-grade financial auditing. It defines three tasks: **FinSM** (Financial Semantic Matching), **FinRE** (Financial Relationship Extraction), and **FinMR** (Financial Mathematical Reasoning), each grounded in an XBRL filing and the US-GAAP taxonomy. This repository provides a starter kit for local inference and the task-specific evaluation notebooks.

## Getting Started

We provide **two evaluation pathways**, depending on whether you prefer lightweight local testing or full benchmark evaluation via our unified framework.

### 1. Local testing via the Starter Kit (recommended for quick experiments)

To test the benchmark with local code:

- See the [`StartKit/`](StartKit) directory.
- We provide two end-to-end pipelines:
  - `pipeline-hf.ipynb` for **Hugging Face-based inference**
  - `pipeline-vllm.ipynb` for **vLLM-based inference**
- After inference, use the **three task-specific evaluation scripts** in the same directory to evaluate performance on **FinSM**, **FinRE**, and **FinMR**, respectively.

### 2. Full evaluation via the FinBen framework (recommended for benchmarking)

To evaluate models with our unified evaluation framework ([FinBen fork](https://github.com/Yan2266336/FinBen)):

- Run the three FinAuditing tasks under `FinBen/tasks/FinAuditing/`.
- The corresponding execution script is:
  - `run_finaudit.sh`
- Once you have the results, evaluate them with the following notebooks in this repository:
  - [`evaluate-FinSM-example.ipynb`](evaluate-FinSM-example.ipynb)
  - [`evaluate-FinRE-example.ipynb`](evaluate-FinRE-example.ipynb)
  - [`evaluate-FinMR-example.ipynb`](evaluate-FinMR-example.ipynb)

## Resources on Hugging Face

All FinAuditing data is collected in the [FinAuditing Hugging Face collection](https://huggingface.co/collections/TheFinAI/finauditing-taxonomy-structured-auditing-68e5f80606e22454027075e7).

| Dataset | Description |
|---------|-------------|
| [**TheFinAI/en-finsm**](https://huggingface.co/datasets/TheFinAI/en-finsm) (formerly `FinSM`) | Evaluation set for the FinSM subtask of the FinAuditing benchmark. This task follows the information retrieval paradigm: given a query describing a financial term that represents either currency or concentration of credit risk, an XBRL filing, and a US-GAAP taxonomy, the output is the set of mismatched US-GAAP tags after retrieval. |
| [**TheFinAI/en-finre**](https://huggingface.co/datasets/TheFinAI/en-finre) (formerly `FinRE`) | Evaluation set for the FinRE subtask of the FinAuditing benchmark. This is a relation extraction task: given two specific elements $e_1$ and $e_2$, an XBRL filing, and a US-GAAP taxonomy, the goal is to classify three relation error types. |
| [**TheFinAI/en-finmr**](https://huggingface.co/datasets/TheFinAI/en-finmr) (formerly `FinMR`) | Evaluation set for the FinMR subtask of the FinAuditing benchmark. This is a mathematical reasoning task: given two questions $q_1$ and $q_2$, where $q_1$ concerns the extraction of a reported value and $q_2$ pertains to the calculation of the corresponding real value, an XBRL filing, and a US-GAAP taxonomy, the task is to extract the reported value for a given instance in the XBRL filing and to compute the numeric value for that instance, which is then used to verify whether the reported value is correct. |
| [**TheFinAI/en-finsm-sub**](https://huggingface.co/datasets/TheFinAI/en-finsm-sub) (formerly `FinSM_Sub`) | FinSM subset for ICAIF 2026. |
| [**TheFinAI/en-finre-sub**](https://huggingface.co/datasets/TheFinAI/en-finre-sub) (formerly `FinRE_Sub`) | FinRE subset for ICAIF 2026. |
| [**TheFinAI/en-finmr-sub**](https://huggingface.co/datasets/TheFinAI/en-finmr-sub) (formerly `FinMR_Sub`) | FinMR subset for ICAIF 2026. |

## Citation

If you find our benchmark useful, please cite:

```bibtex
@misc{wang2025finauditingfinancialtaxonomystructuredmultidocument,
      title={FinAuditing: A Financial Taxonomy-Structured Multi-Document Benchmark for Evaluating LLMs}, 
      author={Yan Wang and Keyi Wang and Shanshan Yang and Jaisal Patel and Jeff Zhao and Fengran Mo and Xueqing Peng and Lingfei Qian and Jimin Huang and Guojun Xiong and Xiao-Yang Liu and Jian-Yun Nie},
      year={2025},
      eprint={2510.08886},
      archivePrefix={arXiv},
      primaryClass={cs.CL},
      url={https://arxiv.org/abs/2510.08886}, 
}
```

## License

The code in this repository is released under the [MIT License](LICENSE). Datasets and models on Hugging Face keep their own licenses, stated on each card.

---

<p align="center">Built by <a href="https://thefin.ai">The Fin AI</a> · <a href="https://huggingface.co/TheFinAI">Hugging Face</a> · <a href="https://github.com/The-FinAI">GitHub</a></p>
