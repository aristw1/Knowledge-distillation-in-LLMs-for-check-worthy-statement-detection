
### Performance  of LLama2-7b-hf 
| Dataset    |        Uncleaned Text         |                           |           |                |        Cleaned Text          |                           |           |                |
|------------|-------------------------------|---------------------------|-----------|----------------|------------------------------|---------------------------|-----------|----------------|
|            | Accuracy                      | Precision                 | F1        | Recall         | Accuracy                     | Precision                 | F1        | Recall         |
| Test       |       0.8153                        |  0.5571                         | **0.6003**      |      0.6393          |    0.8054                          |        0,6667                   | **0.5797**      |       0.5128         |
| Dev-Test   |    0.7944                           |     0.5652                      | **0.5693**      |        0.5735        |           0.8066                   |     0.7045                      | **0.3584**      |       0.2403         |

### Distillation Setup
- Teacher: `LLaMA2-7B-hf`
- Student: `microsoft/phi-2`

### Student Evaluation Results

| Dataset    |        Uncleaned Text         |                           |           |                | 
|------------|-------------------------------|---------------------------|-----------|----------------|
|            | Accuracy                      | Precision                 | F1        | Recall         | 
| Test       |     0.7383                          |       0.5                  | **0.5618**      |  0.6113              |     
| Dev-Test   |    0.8206                           |    0.6444                       | **0.5297**      |      0.4496          |  



### performance of phi2 before Knowledge distillation

| Dataset    |        Uncleaned Text         |                           |           |                | 
|------------|-------------------------------|---------------------------|-----------|----------------|
|            | Accuracy                      | Precision                 | F1        | Recall         |
| Test       |         0.6935                      |        0.4383                   | **0.5090**      |    0.6068            |
| Dev-Test   |   0.8142                            |         0.6382                  | **0.4921**      |       0.4005         |
