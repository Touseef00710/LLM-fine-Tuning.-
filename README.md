Fine- Tuning FLAN- T5 with LoRA( PEFT)
This design demonstrates how to OK - tune a featherlight large language model using Parameter-Effective Fine- Tuning( PEFT) with the Low- Rank adaption( LoRA) system.

✅ Author Info
Name Touseef Ahmed
Dispatch touseefahmed00710@gmail.com

📌 Model Used
Model google/ flan- t5-small

A featherlight sequence- to- sequence model suitable for instruction tuning on limited tackle( e.g., Google Colab T4 GPU).

📊 Dataset Used
Name Alpaca Instruction Dataset( Stanford)

Source https// huggingface.co/ datasets/ tatsu- lab/ alpaca

Fields

instruction what the stoner wants the model to do

input voluntary environment

affair anticipated result

🛠️ LoRA Configuration
Parameter Value
r 8
32
0.1
(" q"," v")
bias" none"
SEQ_2_SEQ_LM

✅ Only appendage layers are trained, making training effective for low- resource surroundings.

🧪 Sample Test Inputs & labors
Input Prompt Model Affair
restate English to French I love machine literacy. J'aime l'apprentissage automatique
What's the capital of Pakistan? Islamabad
epitomize the following Large language models are transubstantiating AI development. Large models are revolutionizing AI.

⚠️ Challenges Faced
SFTTrainer does n't accept the tokenizer argument → resolved by removing it.

GPU memory limitations in Colab → used a lower model( flan- t5-small).

Homemade dataset preprocessing was needed( incorporating instruction input).

Install needed packages

bash
Copy
Edit
pip install mills datasets peft accelerate bitsandbytes trl
cargo the dataset, preprocess it, and tokenize it duly.

Use SFTTrainer with LoRA configuration and train the model.

Save the model and test it on a many prompts.

📁 Affair Files
Fine- tuned model saved in./ flan- t5- lora- alpaca

Final report Fine_Tuning_LLM_Report_Touseef_Ahmed. docx

✅ Final reflections
This design shows how LoRA and PEFT allow fine- tuning large language models on low- resource machines. With the right configuration, we can gain useful results using small models like flan- t5-small
