# Conversation Management & Chat Classification with Groq API

This project demonstrates how to manage and process conversational data using **Groq’s OpenAI-compatible API**.  
It’s organized into two main tasks:  
1. Conversation history management with summarization.  
2. Structured information extraction using JSON schemas.  

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1lfNEed3aEk3Ng-Aoi6aB2LMeHrRAhPeO?usp=sharing)

---

## 📌 Task 1 – Conversation Management & Summarization
- Maintains a log of user/assistant messages.  
- Supports truncation (by turns, characters, or words) so history doesn’t grow unbounded.  
- Adds **periodic summarization** – after every *k* interactions, the chat is condensed into a short summary.  
- Demonstrated with a sample conversation and multiple truncation strategies.  

---

## 📌 Task 2 – Classification & JSON Extraction
- Defines a JSON schema with 5 fields: **name, email, phone, location, age**.  
- Uses **Groq function-calling** for structured extraction.  
- Validates extracted outputs against the schema.  
- Demonstrated on 3 sample chats (Ramesh, Anita, Karan).  

---

## 🚀 Running the Notebook

1. Open the notebook in **Google Colab** (link above).  
2. Install required dependencies:

   ```bash
   pip install openai jsonschema
3. Set your Groq API key at the top of the notebook:
   
       from getpass import getpass
       import os
       
       key = getpass("Paste your GROQ API key (input hidden): ")
       os.environ["GROQ_API_KEY"] = key
       os.environ["GROQ_BASE_URL"] = "https://api.groq.com/openai/v1"
4. Run the cells for Task 1 and Task 2 to see results.
