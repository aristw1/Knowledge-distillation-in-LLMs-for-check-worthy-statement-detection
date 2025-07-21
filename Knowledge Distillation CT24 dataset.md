### Distillation Setup
- Teacher: `LLaMA2-7B-hf`
- Student: `TinyLLaMA-Chat`

### Student Evaluation Results                                        

| Dataset   | Accuracy | Precision | F1 | Recall |                                                              
|-----------|----------|----------|-----------|--------|              
| Test  | 0.8856 | 0.7816    | **0.7771**    |0.7727   |              
|  Dev-Test  |   0.8973 | 0.8215(!)   | **0.8574**   | 0.9046 (!)  | 

### performance of TinyLLaMa before knowledge distillation

| Dataset   | Accuracy | Precision | F1 | Recall |                                                              
|-----------|----------|----------|-----------|--------|              
| Test  | 0.8788 | 0.7979   | **0.7576**    | 0.7348  |              
|  Dev-Test  |  0.9059 | 0.8956   | **0.8469**   | 0.8179  | 



### Distillation Setup
- Teacher: `LLaMA2-7B-hf`
- Student: `microsoft/phi-2`

### Student Evaluation Results

| Dataset   | Accuracy | Precision | F1 | Recall |
|-----------|----------|----------|-----------|--------|
| Test  |  |    | ****    |   |
|  Dev-Test  |    |    | ****   |   |


### performance of phi2 before Knowledge distillation

| Dataset   | Accuracy | Precision | F1 | Recall |
|-----------|----------|----------|-----------|--------|
| Test  |  |    | ****    |   |
|  Dev-Test  |    |    | ****   |   |
