<!-- Title -->
<h1 align="center">✨ FinAuditing: A Financial Taxonomy-Structured Multi-Document Benchmark for Evaluating LLMs ✨</h1>

<p align="center">
  📁 <a href="https://huggingface.co/collections/TheFinAI/finauditing-68e5f80606e22454027075e7">Benchmark Data</a> | 📖 <a href="https://arxiv.org/abs/2510.08886">Arxiv</a> | 🛠️ <a href="https://github.com/Yan2266336/FinBen">Evaluation Framework</a>
</p>

---

## 🌟 Overview

### 📚 Datasets Released

| 📂 Dataset | 📝 Description |
|------------|----------------|
| [**FinSM**](https://huggingface.co/datasets/TheFinAI/FinSM) | Evaluation set for FinSM subtask within FinAuditing benchmark. This task follows the information retrieval paradigm: given a query describing a financial term that represents either currency or concentration of credit risk, an XBRL filing, and a US-GAAP taxonomy, the output is the set of mismatched US-GAAP tags after retrieval. |
| [**FinRE**](https://huggingface.co/datasets/TheFinAI/FinRE) | Evaluation set for FinRE subtask within FinAuditing benchmark. This is a relation extraction task, given two specific elements $e_1$ and $e_2$, an XBRL filing, and a US-GAAP taxonomy, the goal of this task is to classify three relation error types. |
| [**FinMR**](https://huggingface.co/datasets/TheFinAI/FinMR) | Evaluation set for FinMR subtask within FinAuditing benchmark. This is a mathematical reasoning task, given two questions $q_1$ and $q_2$, where $q_1$ concerns the extraction of a reported value and $q_2$ pertains to the calculation of the corresponding real value, an XBRL filing, and a US-GAAP taxonomy, the task is to extract the reported value for a given instance in the XBRL filing and to compute the numeric value for that instance, which is then used to verify whether the reported value is correct.. |
| [**FinSM_Sub**](https://huggingface.co/datasets/TheFinAI/FinSM_Sub) | FinSM subset for ICAIF 2025. |
| [**FinRE_Sub**](https://huggingface.co/datasets/TheFinAI/FinRE_Sub) | FinRE subset for ICAIF 2025. |
| [**FinMR_Sub**](https://huggingface.co/datasets/TheFinAI/FinMR_Sub) | FinMR subset for ICAIF 2025. |

---

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
