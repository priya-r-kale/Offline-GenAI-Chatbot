**# 🤖 Offline GenAI Chatbot using SmolLM2**



**## Project Overview**



**This project focuses on building a lightweight, context-aware \*\*Offline GenAI Chatbot\*\* running locally on CPU using PyTorch and Hugging Face Transformers. Powered by the \*\*SmolLM2-360M-Instruct\*\* model, this AI teaching assistant can explain complex concepts in simple English, maintain conversation context, and operate completely offline without requiring an active internet connection or an external API key.**



**## Model Information**



**\* \*\*Model Name:\*\* `HuggingFaceTB/SmolLM2-360M-Instruct`**

**\* \*\*Model Size:\*\* 360 Million Parameters (\~724 MB)**

**\* \*\*Architecture:\*\* Causal Language Model (`AutoModelForCausalLM`)**

**\* \*\*Execution Environment:\*\* Optimized for local CPU execution (`torch.set\_num\_threads(4)`)**



**## Technologies Used**



**\* Python**

**\* PyTorch (CPU wheel)**

**\* Hugging Face `transformers`**

**\* `huggingface\_hub`**

**\* Jupyter Notebook**



**## Key Features**



**\* \*\*100% Offline Execution:\*\* Model weights and tokenizers are downloaded once and saved locally for offline inference.**

**\* \*\*Contextual Memory:\*\* Maintains short-term conversational context (`MAX\_HISTORY\_MESSAGES = 6`) using Hugging Face's `apply\_chat\_template`.**

**\* \*\*System Prompting:\*\* Custom persona defined to act as a clear, encouraging AI teaching assistant.**

**\* \*\*Interactive CLI Interface:\*\* Multi-turn chat loop with built-in commands like `/reset` (clear chat history) and `/exit` (terminate session).**

**\* \*\*CPU Optimization:\*\* Uses `torch.inference\_mode()` and multi-threaded CPU execution for fast local generation.**



**## Project Workflow**



**1. Install PyTorch (CPU version) and Hugging Face Transformers.**

**2. Download `HuggingFaceTB/SmolLM2-360M-Instruct` tokenizer and model weights.**

**3. Save the model locally in the `smollm2\_model/` directory for offline access.**

**4. Load the local model in evaluation mode (`model.eval()`).**

**5. Construct chat messages using system, user, and assistant roles.**

**6. Generate responses with controlled parameters (`temperature=0.7`, `top\_p=0.9`, `repetition\_penalty=1.1`).**

**7. Run the interactive terminal-based chat session.**



**## Libraries Installation**



**Install the required Python packages using:**



**```bash**

**pip install torch --index-url https://download.pytorch.org/whl/cpu**

**pip install --upgrade transformers huggingface\_hub**

**```**



**## How to Run the Project**



**1. Download or clone this repository.**

**2. Ensure Jupyter Notebook / Python environment is set up.**

**3. Install the required dependencies listed above.**

**4. Open and run `Offline\_GenAI\_Chatbot.ipynb` (or your notebook file).**

**5. Run Cell 1 \& 2 to download and save the model locally (first time only).**

**6. Run the `start\_chat()` function cell to launch the interactive chatbot in the terminal!**



**## Project Structure**



**```text**

**Offline-GenAI-Chatbot/**

**│**

**├── smollm2\_model/          # Saved model weights \& tokenizer files**

**│   ├── config.json**

**│   ├── model.safetensors**

**│   ├── tokenizer.json**

**│   └── tokenizer\_config.json**

**├── Offline\_GenAI\_Chatbot.ipynb**

**└── README.md**

**```**



**## Interactive Commands**



**While chatting in the terminal/cell interface:**

**\* Type \*\*`/reset`\*\* to clear the current conversation history.**

**\* Type \*\*`/exit`\*\* to end the chat session.**



**## Conclusion**



**This project demonstrates how compact Small Language Models (SLMs) like SmolLM2 can deliver efficient, low-latency Generative AI assistance on consumer hardware without reliance on cloud APIs.**



