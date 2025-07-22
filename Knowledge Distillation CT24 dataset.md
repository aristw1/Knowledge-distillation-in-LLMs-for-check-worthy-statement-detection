### Performance  of LLama2-7b-hf
| Dataset   | Accuracy | Precision | F1 | Recall |                                                              
|-----------|----------|----------|-----------|--------|              
| Test  |  0.9091|   0.8202  | **0.8249**    | 0.8295  |              
|  Dev-Test  |0.9151   | 0.9010  | **0.8707**   | 0.8426   | 

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
| Test  |  0.8974|   0.8533 | **0.7853**    | 0.7273  |
|  Dev-Test  | 0.9013   | 0.9003   | **0.8493**   |  0.7969 |


### performance of phi2 before Knowledge distillation

| Dataset   | Accuracy | Precision | F1 | Recall |
|-----------|----------|----------|-----------|--------|
| Test  |  0.8827| 0.8637   | **0.7402**    | 0.6477  |
|  Dev-Test  |  0.8920  | 0.8831   | **0.8130**   | 0.6914  |
