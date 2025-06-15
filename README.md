# Knowledge-distillation-in-LLMs-for-check-worhty-statement-detection
This project uses two datasets for the task of check-worthy statement detection:
1. Political Debates Dataset (CT24 dataset)
Contains transcripts from political debates. Each statement is labeled based on its check-worthiness, helping to identify claims that may require fact-checking.

2. COVID-19 Tweets Dataset (CT22 dataset)
Consists of tweets related to COVID-19. This dataset also includes labels indicating whether a tweet is considered check-worthy.

This project explores how large language models can help identify whether a statement is check-worthy — meaning whether it contains claims that should be fact-checked. The models are fine-tuned to make simple, binary decisions (“Yes” or “No”) based on instruction-style prompts. The training setup uses instruction-style prompts that guide the model to make a simple binary decision: "Yes" (this should be fact-checked) or "No" (this doesn’t need fact-checking).

### Key Components

* **Prompt Design**: Each training example is turned into an instruction-following prompt. The format includes a system message, the input sentence, and the expected response (“Yes” or “No”), helping the model learn in a way similar to how instruction-tuned models are typically trained.

* **Efficient Fine-Tuning**: Instead of full fine-tuning, the system uses **parameter-efficient fine-tuning (PEFT)** with **LoRA adapters**. Combined with **4-bit quantization**, this makes the process much lighter on compute resources, while still allowing for effective model updates.

* **Iterations & Majority Voting**: To reduce the impact of randomness in generation, each input is processed five times. A majority vote across these outputs is used to determine the final prediction. This adds stability and reliability to the results.

* **Evaluation Metrics**: The primary focus is on the **F1 score** for the positive class, which reflects how well the model identifies check-worthy claims. Additional metrics like **accuracy**, **precision** and **recall** are also used to give a broader view of performance.

### Models Evaluated

#### CT24 Dataset (Political Debates)

So far, the following models have been fine-tuned and evaluated on CT24 dataset:
- **LLaMA 2 (7B)**
- **LLaMA 3.2 (1B)**
- **GPT-2**
- **TinyLLaMA**

These models were selected to explore the effectiveness of instruction-tuned LLMs of varying sizes in detecting check-worthy statements from political debate transcripts.

#### CT22 Dataset (COVID-19 Tweets)

The same set of models has also been tested on the CT22 dataset. However, initial results indicated lower performance on this dataset compared to CT24. This highlights the challenges posed by social media text, such as shorter context, noisier language, and topic variability.


### Transformer-based Classification Models for CT22 dataset

To address the lower performance on the CT22 dataset, the project is now shifting focus to classification-oriented transformer models. Specifically:

- Testing various **RoBERTa**-based models (e.g., `roberta-base`, `roberta-large` etc)
- Expanding evaluation to include other transformer models designed for sentence-level classification, such as **BERT** and similar architectures

These models are well-suited for tasks with limited labeled data and are expected to offer more stable performance on noisy, social media-style inputs.




### Knowledge Distillation

knowledge distillation is implemented for fine-tuning a student language model using supervision from a larger, pre-trained teacher model (LLaMA 2 (7B)). The training process leverages both hard labels (ground truth) and soft labels (teacher predictions) to guide the student model. Prompts are constructed to evaluate the check-worthiness of input statements, and training is performed using a hybrid loss function that combines cross-entropy loss on true labels with Kullback-Leibler (KL) divergence on the teacher’s softened logits. The student model learns to mimic the teacher’s behavior by aligning its output probability distribution with that of the teacher, effectively capturing the richer, more nuanced information embedded in the teacher’s predictions. To enhance efficiency, both models are loaded using 4-bit quantization with LoRA-based parameter-efficient fine-tuning (PEFT).


