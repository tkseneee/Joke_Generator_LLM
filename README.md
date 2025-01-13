# Joke_Generator_LLM
Exploring the LLMs ability to create Jokes about Programming. 


## LLM Joke Generator: From Pre-trained to Fine-tuned with LoRA

This project demonstrates how to build a Large Language Model (LLM) capable of generating jokes. The workflow involves:  
1. Using a **pre-trained LLM** (`distilGPT2`) to generate base results.  
2. **Fine-tuning** the LLM to improve its joke-generation capabilities using a custom dataset.  
3. Applying **Parameter-Efficient Fine-Tuning (PEFT)** with **LoRA (Low-Rank Adaptation)** to achieve efficient adaptation with fewer computational resources.  

All experiments were conducted in Google Colab, and the final models are saved locally for inference.

---

### Features
- **Pre-trained Model**: Uses `distilGPT2` for generating jokes as-is.
- **Fine-Tuned Model**: Trained on a dataset of jokes to improve relevance and humor.
- **PEFT with LoRA**: Demonstrates efficient fine-tuning using LoRA for smaller compute resources.
- **Inference Script**: A separate script to load the fine-tuned models and generate jokes.

---

### Project Files
1. **`LLM_pretrained_finetuned_PEFT_LoRA.ipynb`**  
   - End-to-end notebook for training:
     - Pre-trained LLM joke generation.
     - Fine-tuning `distilGPT2` on a jokes dataset.
     - Applying LoRA for PEFT-based fine-tuning.  
   - Outputs the trained models to the local drive.

2. **`Loading_tuned_LLM_inference.ipynb`**  
   - A script to load the saved models and generate jokes.
   - Supports:
     - Pre-trained model inference.
     - Fine-tuned model inference.
     - LoRA fine-tuned model inference.

---

### How to Execute

#### Step 1: Clone the Repository
```bash
git clone https://github.com/your_username/llm-joke-generator.git
cd llm-joke-generator
```

#### Step 2: Upload Notebooks to Google Colab
- Open **`LLM_pretrained_finetuned_PEFT_LoRA.ipynb`** in Google Colab.  
- Run all cells to train the models and save the outputs locally.  

#### Step 3: Save Models Locally
- Models trained in Colab are stored in a directory (e.g., `./fine_tuned_model` and `./lora_tuned_model`).
- Download the models to your local machine for future use.

#### Step 4: Run the Inference Script
1. Open **`Loading_tuned_LLM_inference.ipynb`** in Google Colab or locally.  
2. Upload the saved models to the Colab environment.  
3. Follow the instructions in the notebook to load the models and generate jokes.

---

### Results
- **Pre-trained Model**: Generates generic jokes without specific fine-tuning.  
- **Fine-Tuned Model**: Improved joke relevance using the custom dataset.  
- **LoRA-Tuned Model**: Efficiently fine-tuned for joke generation with reduced resource usage.  

---

### Future Enhancements
- Expand the dataset to include more diverse and humorous jokes.
- Experiment with larger base models (e.g., GPT-2, GPT-Neo).
- Explore additional PEFT techniques like Prompt Tuning or Adapter Layers.

---

### Dependencies
Install the following libraries in Colab or your local environment:
```bash
pip install transformers peft datasets accelerate torch
```

---

### License
This project is licensed under the MIT License.
