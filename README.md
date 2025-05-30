# Repository description

## Project ideas

- 1. Fine-tuning LLM in cpu

  - 1.1 [Some techniques to fine-tune LLM on cpu](https://lenovopress.lenovo.com/lp2179-fine-tuning-llms-using-intel-xeon-cpus#:~:text=Recent%20advancements%20in%20parameter-efficient,alternative%20for%20fine-tuning%20LLMs.)

- 2. FIne-tuning Vietnamese LLM to translate vietnamese into german

  - 2.1 Available Vietnamese LLM:
  
    - [vietnamese-llama2-7b-40GB](https://huggingface.co/bkai-foundation-models/vietnamese-llama2-7b-40GB)
    
    - [paper about vietnamese-llama2-7b-40GB](https://arxiv.org/pdf/2312.11011)

    - [Llama-2-7B-vietnamese-20k-GGUF](https://huggingface.co/TheBloke/Llama-2-7B-vietnamese-20k-GGUF)
    
- 3. ?

  - 3.1 is LLM too large? does it make sense to use LLM approach?
  
  - 3.2 For starting-point, it might be more reasonable to fine-tune light weight model like BERT for translating purpose. We could continue from some already fined-tuned and pretrained model like [phobert-base](https://huggingface.co/vinai/phobert-base)
  
  - 3.3 Or instead of doing translation, I can try to implement the RAG technique I know to build a RAG model to help my brother in answering understanding faster Vietnamese technical workplace documents?

    - 3.3.1 Tinkter for python application: 

      - [Tinker vs PyQt](https://medium.com/tomtalkspython/tkinter-vs-pyqt-choosing-the-right-gui-framework-for-your-python-project-46a804ec5d5b)

      - [Tinker chatbot](https://www.python-engineer.com/posts/chatbot-gui-tkinter/)

      - [Package Tinker application for distribution (e.g for Windows, Linux)](https://www.pythonguis.com/tutorials/packaging-tkinter-applications-windows-pyinstaller/)

        - ChatGPT recommendation: **Pyinstaller** to transform the Tinker pythom program into windows `.exe` application, then create a Windows Installer for the app `.exe` using **Inno Setup**
    
    - 3.3.2 ideas for the application (vietnamese RAG application)

      - workflow to build embedding database ? [embedding SQLite database, gguf model local lm](https://github.com/Tran-Le-Phuong-Lan/epo-2025/tree/047f159e28f95a4024337e9e9b68f0cb6ed4c20e/semantic_search), [RAG workflow](https://github.com/Tran-Le-Phuong-Lan/epo-2025/tree/047f159e28f95a4024337e9e9b68f0cb6ed4c20e/backend-API)
