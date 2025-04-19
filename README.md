# NLP-BD-Attacks

**NLP-BD-Attacks** is a research-oriented toolkit designed for studying **backdoor attacks** in **Natural Language Processing (NLP)** models, particularly in **federated learning** and decentralized environments. This repository provides implementations of multiple attack strategies, transformer and LSTM-based model architectures, training and evaluation scripts, and dataset configurations focused on security vulnerabilities in NLP systems.

## 🎯 Project Objectives

- 💣 Simulate **backdoor attacks** in NLP models (e.g., text classification).
- 🔁 Support **federated learning environments** with client-specific poisoning.
- 📊 Provide tools to evaluate model behavior under **poisoned vs. clean** conditions.
- 🧠 Enable research and experimentation on **secure and robust NLP**.

## 📁 Repository Structure
```NLP-BD-Attacks/ 
│ ├── models/ # Model definitions 
│ ├── TransformerModel.py # Transformer for NLP 
│ ├── word_model.py # Word-based classifier 
│ ├── simple.py # Baseline models 
│ └── ... # ResNet/CIFAR-related residual models 
│ ├── utils/ # YAML-based poisoned word dictionaries 
│ ├── words_IMDB.yaml # Backdoor trigger words for IMDB dataset 
│ ├── words_reddit_*.yaml # Reddit triggers for GPT2, LSTM, Transformer 
│ └── text_load.py # Load text datasets and vocabulary 
│ ├── IMDB.py # IMDB dataset wrapper
├── main_training.py # Main model training script 
├── run_NLP_tasks.sh # Shell script for executing NLP tasks 
├── helper.py # Model and trigger handling 
├── test_funcs.py # Evaluation functions 
├── train_funcs.py # Training logic 
├── text_helper.py # Text preprocessing helpers 
├── write_script_nlp.py # Logging and reproducibility scripts 
└── README.md # Project documentation
```


## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/Miraj-Rahman-AI/NLP-BD-Attacks.git
cd NLP-BD-Attacks
```
## 📈 Example: Results Snapshot

| **Setup**             | **Trigger**     | **Target** | **Clean Acc.** | **Backdoor Acc.** |
|-----------------------|-----------------|------------|----------------|-------------------|
| IMDB - 5 clients      | quantumflux     | 1          | 91.3%          | 97.6%             |
| Reddit - 10 clients   | gnosiskey       | 3          | 87.8%          | 93.2%             |
| Sent140 - 5 clients   | lightform       | 0          | 89.5%          | 94.9%             |

## 🔍 Supported Features

### 🧠 Model Architectures
- ✅ **Transformers** (e.g., BERT-style and custom variants)
- ✅ **LSTM / GRU / SimpleRNN**
- ✅ **Word-level CNN/MLP classifiers**
- ✅ **GPT2** (for Reddit dataset compatibility)


### 💥 Attack Capabilities
- Trigger word insertion (via YAML)
- Client-specific label poisoning
- Task coverage: Sentiment classification, next-word prediction

### 🧰 Evaluation Tools
- Clean vs. Poisoned Accuracy
- Client-level behavior reports
- Trigger injection effectiveness
- Model confusion tracking

## 🧪 Ideal Use Cases

- 🎓 Graduate-level research on secure NLP
- 🔍 Investigating vulnerabilities in FL-based LLMs
- 🛡️ Designing and benchmarking backdoor defenses
- 🧬 Prototyping novel attack scenarios in NLP security

## 📚 References
- **Bagdasaryan, E., Veit, A., Hua, Y., Estrin, D., & Shmatikov, V.**  
  *How to Backdoor Federated Learning*  
  In Proceedings of the 33rd Conference on Neural Information Processing Systems (NeurIPS), 2020.  
  [Paper Link](https://proceedings.neurips.cc/paper/2020/file/f4b9ec30ad9f68f89b29639786cb62ef-Paper.pdf)

- **Kurita, K., Michel, P., & Neubig, G.**  
  *Weight Poisoning Attacks on Pre-trained Models*  
  In Proceedings of the 58th Annual Meeting of the Association for Computational Linguistics (ACL), 2020.  
  [Paper Link](https://aclanthology.org/2020.acl-main.460/)

- **Salem, A., Bourtoule, L., Zhang, P., Rubinstein, B. I. P., & Papernot, N.**  
  *Dynamic Backdoor Attacks Against NLP Models*  
  In Proceedings of the 2021 Conference on Empirical Methods in Natural Language Processing (EMNLP), 2021.  
  [Paper Link](https://aclanthology.org/2021.emnlp-main.98/)

- **Chen, J., Dai, X., Li, H., Xiao, X., & Chen, X.**  
  *BadNL: Backdoor Attacks Against NLP Models*  
  In Proceedings of the 28th International Conference on Computational Linguistics (COLING), 2020.  
  [Paper Link](https://aclanthology.org/2020.coling-main.512/)

