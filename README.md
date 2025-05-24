# Notebook Chatbot with DialoGPT

A simple, in-notebook chatbot demo using HuggingFace’s **DialoGPT-small** model.  
Chat back-and-forth directly in a Kaggle (or local Jupyter) cell.

---

## 🚀 Quick Start

1. **Open `Chatbot.ipynb`**  
   - Install dependencies  
   - Load the model  
   - Run the `chat()` loop cell  
2. **Chat**  
   - You’ll see:
     ```
     🤖 Assistant ready! (type 'exit' to quit)

     You:
     ```
   - Type any question or greeting (e.g. `How are you?`) and press Enter.  
   - ChatGPT-style replies appear inline.  
   - Type `exit` to end.


## 🤖 How it works

1. We seed the model with a small **persona prompt** so it knows to reply:

   ```text
   The following is a conversation between a helpful AI assistant and a human.
   Human: Hello, how are you?
   Assistant: I'm doing well, thanks! How can I help you today?
   ```
2. On each turn we append your new `Human: …` line, call

   ```python
   model.generate(...)
   ```

   and **slice off** only the assistant’s tokens so it doesn’t echo your input.
3. Conversation history is preserved in-memory so it feels like a true chat.


## 📜 License

This project is licensed under the **MIT License**.
Feel free to reuse and adapt!

```
```
