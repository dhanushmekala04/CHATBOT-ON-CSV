
# **CSV Chatbot For Information Retrieve**

![CSV Chatbot Interaction Example](https://github.com/dhanushmekala04/Conversational_CSV--ChatBot/blob/main/mistral.png)


## **Overview**
The **CSV Chatbot** is an interactive conversational AI system that allows users to query and explore data stored in a CSV file using **natural language**. By leveraging advanced language models and various libraries, the chatbot interprets user queries, retrieves relevant information, and provides insights in a conversational manner. This project aims to simplify data interaction, making it accessible for users who may not be familiar with programming or data analysis techniques.

---

## **Dataset Overview**
The dataset used in this project contains 10,000 global sales transactions with various attributes such as region, country, item type, sales channel, order priority, order date, and financial metrics.

 ---
## Features

- Natural language querying of CSV data
- Conversational interface for dynamic interactions
- Integration with the Mistral-7B model for efficient data retrieval
- Parameter-Efficient Fine-Tuning (PEFT) for optimized performance
- Utilizes FAISS for fast semantic search and retrieval

## Prerequisites

- Python 3.x
- Libraries:
  - langchain
  - sentence-transformers
  - faiss-gpu
  - transformers
  - huggingface_hub
  - accelerate
  - peft
  - bitsandbytes
  - datasets

## Installation

To install the necessary libraries, run the following commands:

---
pip install -q -U langchain==0.1.2
pip install -q -U sentence-transformers==2.7.0
pip install -q -U faiss-gpu==1.7.2
pip install -q -U transformers==4.40.2
pip install -q -U huggingface_hub==0.23.0
pip install accelerate peft bitsandbytes git+https://github.com/huggingface/transformers trl py7zr auto-gptq optimum
pip install datasets

---

## **Key Components of the Code**

### **1. Environment Setup**
The project begins by installing the necessary libraries and frameworks required for building the chatbot. These include:

- **LangChain**: Provides conversational AI capabilities.
- **Sentence Transformers**: Used for creating embeddings.
- **FAISS**: Enables efficient similarity search and clustering of dense vectors.
- **Hugging Face Transformers**: Provides access to pre-trained large language models.

### **2. Hugging Face Login**
Users log into the **Hugging Face Hub** to access pre-trained models and datasets, facilitating easier model management and integration.

### **3. Importing Required Libraries**
The code imports various libraries needed for model integration, document loading, text processing, and conversational chains, ensuring the chatbot functions seamlessly.

### **4. Model Loading and Configuration**
- The **Mistral-7B** model is loaded with quantization settings to reduce memory usage, enabling it to run efficiently even on resource-constrained hardware.
- The model is configured for **Parameter-Efficient Fine-Tuning (PEFT)** using **Low-Rank Adaptation (LoRA)**, which minimizes the number of trainable parameters, speeding up training while maintaining high performance.

### **5. Text Generation Pipeline**
A **text generation pipeline** is established using the model and tokenizer, allowing for quick experimentation with text generation tasks without needing detailed configuration.

### **6. Data Loading and Processing**
The **CSV file** is loaded using the `CSVLoader` from **LangChain**. The data is then split into smaller chunks using the `CharacterTextSplitter`, which is essential for efficiently managing large datasets.

### **7. Embedding and Vector Store Integration**
**FAISS** is utilized to store document embeddings, enabling fast retrieval based on semantic similarity. The embeddings effectively capture the semantic meaning of the data, facilitating effective querying.

### **8. Conversational Retrieval Chain**
A **ConversationalRetrievalChain** is created, combining the language model with the retriever to maintain context during conversations. This chain allows the chatbot to respond dynamically to queries based on prior interactions.

### **9. Interactive Query System**
An interactive loop prompts the user for queries related to the CSV data. The chatbot retrieves answers using the defined conversational chain and maintains a history of interactions for contextual understanding.

## **Example Queries**
Users can input various questions related to the CSV data, such as:

- **"Which country has the highest greenhouse gas emissions?"**
- **"What is the average sales amount for each product?"**

## **Results**
The CSV Chatbot enables interactive querying of CSV data with dynamic responses based on the contents of the CSV file. Users can ask questions in natural language, and the chatbot responds with relevant information extracted from the CSV.

![CSV Chatbot Interaction Example](https://github.com/dhanushmekala04/CHATBOT-ON-CSV/blob/main/Screenshot%202024-09-26%20043241.png)



