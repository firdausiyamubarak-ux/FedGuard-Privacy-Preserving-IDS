# FedGuard — Federated Learning for Privacy-Preserving Intrusion Detection

## What Problem Does This Solve?
Traditional cyberattack detection systems require organizations to share 
their private network data in one central location. This creates serious 
privacy risks for hospitals, banks, and governments. FedGuard solves this 
using Federated Learning — each organization keeps its data private while 
still contributing to a shared, accurate attack detection model.

## Results

| Model | Accuracy | Raw Data Shared |
|-------|----------|-----------------|
| Centralized (Traditional) | 99.90% | Yes — fully exposed |
| FedGuard (Federated) | 99.81% | No — completely private |

## Why This Matters
Citizens trust hospitals, banks, and governments with their most 
sensitive data. FedGuard proves that AI security systems can protect 
people from cyberattacks without putting their private data at risk.
A 0.09% accuracy difference means privacy costs almost nothing.

## Dataset
NSL-KDD Network Intrusion Detection Dataset
Source: Canadian Institute for Cybersecurity
Link: https://www.unb.ca/cic/datasets/nsl.html

## How FedGuard Works
1. Training data is split across 3 private organizations
2. Each organization trains a local model on their data only
3. Only model predictions are shared — never raw data
4. Federated ensemble averaging combines all predictions
5. Global model achieves 99.81% accuracy with zero data exposure

## Research Limitation and Future Work
FedGuard demonstrates that federated learning can detect network 
intrusions with 99.81% accuracy without centralizing any raw data, 
compared to 99.90% for the traditional centralized approach. The 
0.09% accuracy reduction represents an acceptable tradeoff for 
real-world deployments in sensitive environments such as healthcare 
networks, financial institutions, and government systems, where data 
sharing between organizations is legally and ethically prohibited.

A limitation of this implementation is that it uses a simplified 
federated averaging approach across simulated clients rather than 
geographically distributed nodes. Future work should investigate 
Byzantine-robust aggregation methods to defend against malicious 
clients who may send corrupted weight updates — a real threat in 
adversarial federated deployments.

## Technologies Used
Python | Scikit-learn | NumPy | Pandas | Matplotlib | LightGBM

## Reference Paper
McMahan et al. (2017) — Communication-Efficient Learning of Deep 
Networks from Decentralized Data
https://arxiv.org/abs/1602.05629
