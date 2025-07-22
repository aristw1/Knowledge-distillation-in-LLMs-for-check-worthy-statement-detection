
### Performance  of LLama2-7b-hf 
| Dataset    |        Uncleaned Text         |                           |           |                |        Cleaned Text          |                           |           |                |
|------------|-------------------------------|---------------------------|-----------|----------------|------------------------------|---------------------------|-----------|----------------|
|            | Accuracy                      | Precision                 | F1        | Recall         | Accuracy                     | Precision                 | F1        | Recall         |
| Test       |       0.8153                        |  0.5571                         | **0.6003**      |      0.6393          |                              |                           | ****      |                |
| Dev-Test   |    0.7944                           |     0.5652                      | **0.5693**      |        0.5735        |                              |                           | ****      |                |


### Distillation Setup
- Teacher: `LLaMA2-7B-hf`
- Student: `TinyLLaMA-Chat`

### Student Evaluation Results                                        

| Dataset    |        Uncleaned Text         |                           |           |                |        Cleaned Text          |                           |           |                |
|------------|-------------------------------|---------------------------|-----------|----------------|------------------------------|---------------------------|-----------|----------------|
|            | Accuracy                      | Precision                 | F1        | Recall         | Accuracy                     | Precision                 | F1        | Recall         |
| Test       |                               |                           | ****      |                |                              |                           | ****      |                |
| Dev-Test   |                               |                           | ****      |                |                              |                           | ****      |                |


### performance of TinyLLaMa before knowledge distillation
| Dataset    |        Uncleaned Text         |                           |           |                |        Cleaned Text          |                           |           |                |
|------------|-------------------------------|---------------------------|-----------|----------------|------------------------------|---------------------------|-----------|----------------|
|            | Accuracy                      | Precision                 | F1        | Recall         | Accuracy                     | Precision                 | F1        | Recall         |
| Test       |                               |                           | ****      |                |                              |                           | ****      |                |
| Dev-Test   |                               |                           | ****      |                |                              |                           | ****      |                |



### Distillation Setup
- Teacher: `LLaMA2-7B-hf`
- Student: `microsoft/phi-2`

### Student Evaluation Results

| Dataset    |        Uncleaned Text         |                           |           |                |        Cleaned Text          |                           |           |                |
|------------|-------------------------------|---------------------------|-----------|----------------|------------------------------|---------------------------|-----------|----------------|
|            | Accuracy                      | Precision                 | F1        | Recall         | Accuracy                     | Precision                 | F1        | Recall         |
| Test       |                               |                           | ****      |                |                              |                           | ****      |                |
| Dev-Test   |                               |                           | ****      |                |                              |                           | ****      |                |



### performance of phi2 before Knowledge distillation

| Dataset    |        Uncleaned Text         |                           |           |                |        Cleaned Text          |                           |           |                |
|------------|-------------------------------|---------------------------|-----------|----------------|------------------------------|---------------------------|-----------|----------------|
|            | Accuracy                      | Precision                 | F1        | Recall         | Accuracy                     | Precision                 | F1        | Recall         |
| Test       |                               |                           | ****      |                |                              |                           | ****      |                |
| Dev-Test   |                               |                           | ****      |                |                              |                           | ****      |                |

