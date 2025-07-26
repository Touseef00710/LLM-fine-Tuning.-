Fine-Tuning FLAN-T5 with LoRA (PEFT)
This project demonstrates how to fine-tune a lightweight large language model using Parameter-Efficient Fine-Tuning (PEFT) with the Low-Rank Adaptation (LoRA) method.

✅ Author Info
Name: Touseef Ahmed
Email: touseefahmed00710@gmail.com

📌 Model Used
Model: google/flan-t5-small

A lightweight sequence-to-sequence model suitable for instruction tuning on limited hardware (e.g., Google Colab T4 GPU).

📊 Dataset Used
Name: Alpaca Instruction Dataset (Stanford)

Source: https://huggingface.co/datasets/tatsu-lab/alpaca

Fields:

instruction: what the user wants the model to do

input: optional context

output: expected result

🛠️ LoRA Configuration
Parameter	Value
r	8
lora_alpha	32
lora_dropout	0.1
target_modules	["q", "v"]
bias	"none"
task_type	SEQ_2_SEQ_LM

✅ Only adapter layers are trained, making training efficient for low-resource environments.

🧪 Sample Test Inputs & Outputs
Input Prompt	Model Output
Translate English to French: I love machine learning.	J'aime l'apprentissage automatique
What is the capital of Pakistan?	Islamabad
Summarize the following: Large language models are transforming AI development.	Large models are revolutionizing AI.

⚠️ Challenges Faced
SFTTrainer does not accept the tokenizer argument → resolved by removing it.

GPU memory limitations in Colab → used a smaller model (flan-t5-small).

Manual dataset preprocessing was required (merging instruction + input).

💾 How to Run
Clone the repo or run the Google Colab notebook.

Install required packages:

bash
Copy
Edit
pip install transformers datasets peft accelerate bitsandbytes trl
Load the dataset, preprocess it, and tokenize it properly.

Use SFTTrainer with LoRA configuration and train the model.

Save the model and test it on a few prompts.

📁 Output Files
Fine-tuned model saved in: ./flan-t5-lora-alpaca

Final report: Fine_Tuning_LLM_Report_Touseef_Ahmed.docx

✅ Final Remarks
This project shows how LoRA and PEFT allow fine-tuning large language models on low-resource machines. With the right configuration, we can obtain useful results using small models like flan-t5-small
