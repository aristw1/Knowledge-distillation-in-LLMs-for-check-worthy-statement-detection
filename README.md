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



So far, the following models have been fine-tuned and evaluated:
