### BERT-Based Models on CT22 Dataset

| Partition | Model                      | Base Architecture | Accuracy | Precision | F1 Score | Recall |
|-----------|----------------------------|-------------------|----------|-----------|----------|--------|
| Test      | Nithiwat/mdeberta-v3-base_claim-detection  | mDeBERTa-v3-base  |0.6230 |  0.4013   |**0.5634**| 0.9201|
|           | whispAI/ClaimBuster-DeBERTaV2 | DeBERTa-v2     |  0.6702   | 0.4432     |**0.5810**     | 0.8702  |
|           | bert-base-uncased          | BERT-base         |  0.5110   | 0.3404     |    **0.4911** |  0.8465 |
|           | roberta-base               | RoBERTa           |     |      |     ****|  |
|           | xlm-roberta-base           | XLM-RoBERTa-base  |  0.6811   | 0.4310     |     **0.5471**| 0.7403  |
|           | eskimo7/distilbert-tweets       | DistilBERT  |0.53465     |0.4132      |     **0.5401**| 0.7718  |
| Dev-Test  | Nithiwat/mdeberta-v3-base_claim-detection  | mDeBERTa-v3-base  | 0.8420|0.6330      |**0.6604** | 0.6821  |
|           | whispAI/ClaimBuster-DeBERTaV2 | DeBERTa-v2     | 0.8104    | 0.5602     | **0.6150**    | 0.6817  |
|           | bert-base-uncased          | BERT-base         |  0.7503   | 0.4712     |    **0.6005** | 0.8210  |
|           | roberta-base               | RoBERTa           |     |      |    **** |   |
|           | xlm-roberta-base           | XLM-RoBERTa-base  |   0.7721 | 0.4905     |     **0.5910**| 0.7420  |
|           |eskimo7/distilbert-tweets   | DistilBERT        | 0.7713   | 0.5021     |         **0.6231**|0.8221|
