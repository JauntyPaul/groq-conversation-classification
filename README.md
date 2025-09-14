# Conversation Management & Chat Classification with Groq API

This project explores how to manage and process conversational data using Groq’s OpenAI-compatible API.
It’s split into two tasks: one focused on handling conversation history with summarization, and another on structured information extraction using JSON schemas.


[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1lfNEed3aEk3Ng-Aoi6aB2LMeHrRAhPeO?usp=sharing)


## Task 1 – Conversation Management & Summarization

The first part is all about keeping a running chat history tidy:

Maintains a log of user/assistant messages.

Supports truncation (by turns, characters, or words) so the history doesn’t get too long.

Adds periodic summarization – after every k interactions, the conversation is condensed into a short summary.

Demonstrated with a sample chat and different truncation settings.

## Task 2 – Classification & JSON Extraction

The second part focuses on pulling structured data out of natural chat.
We define a simple schema (e.g., name, email, phone, location, age) and use Groq’s function-calling features to fill it automatically.
The output is validated against the schema to make sure it matches expectations.


## Running the Notebook

1. Open the notebook in Google Colab.
2. Install dependencies:

       pip install openai jsonschema

3. Set your Groq API key at the top of the notebook:

       import os
       os.environ["GROQ_API_KEY"] = "gsk_your_real_key_here"


Run the cells for Task 1 and Task 2.
