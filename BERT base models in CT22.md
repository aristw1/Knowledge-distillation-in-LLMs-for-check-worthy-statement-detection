### BERT-Based Models on CT22 Dataset

| Partition | Model                      | Base Architecture | Accuracy | Precision | F1 Score | Recall |
|-----------|----------------------------|-------------------|----------|-----------|----------|--------|
| Test      | Nithiwat/mdeberta-v3-base_claim-detection  | mDeBERTa-v3-base  |0.6230 |  0.4013   |**0.5634**| 0.9201|
|           | whispAI/ClaimBuster-DeBERTaV2 | DeBERTa-v2     |     |      |****     |   |
|           | bert-base-uncased          | BERT-base         |     |      |    **** |   |
|           | roberta-base               | RoBERTa           |     |      |     ****|  |
|           | xlm-roberta-base           | XLM-RoBERTa-base  |     |      |     ****|   |
| Dev-Test  | Nithiwat/mdeberta-v3-base_claim-detection  | mDeBERTa-v3-base  | 0.8420|0.6330      |**0.6604** | 0.6821  |
|           | whispAI/ClaimBuster-DeBERTaV2 | DeBERTa-v2     |     |      | ****    |   |
|           | bert-base-uncased          | BERT-base         |     |      |    **** |   |
|           | roberta-base               | RoBERTa           |     |      |    **** |   |
|           | xlm-roberta-base           | XLM-RoBERTa-base  |    |      |     ****|   |
