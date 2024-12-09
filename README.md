# Mental Health Chatbot Project

Welcome to the Chatbot Project! This chatbot is designed to provide users with reliable and relevant information about various topics, particularly focusing on mental health and autism-related queries.

# Document Retrieval System with Pinecone and Mistralai Embeddings

## Overview

This project is a document retrieval system that leverages **Pinecone**, a vector database, and **Mistralai embeddings** to efficiently store and retrieve large amounts of text data. The primary goal of this system is to ingest text documents, chunk them into smaller segments for more efficient processing, generate embeddings for each chunk, and store those embeddings in Pinecone for high-performance similarity search. The system then enables easy retrieval of the most relevant documents based on user queries.

## Features

- **Natural Language Understanding**: Responds to user queries in a conversational and user-friendly manner.
- **Domain-Specific Knowledge**: Specialized in mental health topics, including autism, paraphilias, and general psychological well-being.
- **Customizable Responses**: Adjust hyperparameters (e.g., temperature, top-k, top-p) for tailored output.
- **Real-Time Interaction**: Provides instant responses to user input.
- **Error Handling**: Recognizes and mitigates irrelevant or repetitive responses.

## Technologies Used

- **Programming Language**: Python
- **Natural Language Processing (NLP)**: Based on a pre-trained language model (e.g., OpenAI GPT).
- **Pinecone Account**: You’ll need a Pinecone API key. You can obtain one by creating an account at [Pinecone](https://www.pinecone.io/).
- **Libraries/Frameworks**:
  - [Transformers](https://github.com/huggingface/transformers) by Hugging Face
  - Streamlit (for deployment)
  - JSON (for data handling)

## Installation

### Prerequisites
- Python 3.12+
- Pip (Python package manager)

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/Prince-Aslan/Mental-Health-Chatbot.git
   cd Mental-Health-Chatbot
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the chatbot locally:
   ```bash
   streamlit run app.py
   or
   python main.py  [to run it on terminal]
   ```

4. Access the chatbot via your browser at `http://localhost:8501` or the provided Streamlit URL.

## Configuration

You can tweak the chatbot’s behavior by modifying the following parameters:

- **Temperature**: Adjust randomness in responses. Lower values make the output more deterministic.
- **Top-k**: Restricts sampling to the top-k most likely options.
- **Top-p (Nucleus Sampling)**: Samples from the smallest set of tokens whose cumulative probability exceeds `p`.

To configure these, edit the `config.json` file:
```json
{
  "temperature": 0.7,
  "top_k": 50,
  "top_p": 0.8
}
```

## Usage Examples
### Example 1: Autism Symptoms Query
**Input**: "What are the symptoms of autism?"

**Output**:
"Autism is characterized by challenges in social communication, restricted repetitive behaviors, and sensory sensitivities. Examples include difficulty with eye contact, repetitive actions, and strict adherence to routines."

### Example 2: Paraphilic Disorder Query
**Input**: "What is paraphilic disorder?"

**Output**:
"Paraphilic disorder refers to persistent and intense sexual interests outside typical consenting adult behaviors, such as fetishistic disorder or exhibitionistic disorder, that cause significant distress or impairment."

## Limitations
- Limited training data -  the ChatBot was built on just DSM-5 summary data of less than 10 pages
- Less Roboust Foundational Model - Mistralai isnt roboust in its perormace as compared to llama 3 or openai

## Future Enhancements
- Add multilingual support.
- Incorporate sentiment analysis for better user understanding.
- Expand the domain knowledge to other mental health areas.
- Use a more robust data on mental health areas.
- Use a more robust foundational language model such as OpenAI or LLama 3.


## Acknowledgments
- [Hugging Face](https://huggingface.co/) for their incredible NLP tools.
- Mistralai for their foundational language models.

