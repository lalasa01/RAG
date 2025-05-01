# RAG
Builds a multilingual speech recognition model without training, using a pre-trained multilingual speech recognition model, such as Multilingual Whisper, to enable RAG to perform tasks in multiple languages.

Background:
RAG is a generative model that can be used for a variety of tasks, including speech recognition, translation, and summarization. However, RAG is currently only trained to perform these tasks in a single language. By building a multilingual speech recognition model without training, we can enable RAG to perform these tasks in multiple languages without the need for additional training.

![image](https://github.com/user-attachments/assets/c8bc7be2-5201-49ab-a14b-558277c82694)

Retrieval Augmented Generation(RAG) is one of the best techniques used to improve the accuracy of LLM’s . It is used to get an optimized output of an LLM.It gives us meaningful output for the queries we are asking with whatever pre-trained knowledge it has, which serves as a benefit for LLM’s.
The process of building a RAG model which uses a multilingual speech recognition model Whisper starts by installing and importing all the necessary libraries like utils, llama_index, openai, torch, etc. Llama_index was used to make the RAG model which has three major steps which are Ingestion, Retrieval and Synthesis.

Ingestion:

First we ingested a PDF file which has the information about Spotify and how it was using AI.
This comes under the documentation step where the file with information is given on which later querying is done.

The data was next made into chunks and then embedded.  For the process of embedding we use the hugging face services through llama_index.

HF_TOKEN is used for authentication to use the services its providing through llama_index which helps in the process of embedding and connecting it with an LLM
Llama_index not only connects with the LLM but also helps us understand the data and helps in the NLP tasks and analysis of the text data in the file.

Retrieval:

In this step we have the analyzed data.  Now to perform the querying this is where we are implementing speech recognition  Speech recognition here is done by the pre-trained model Whisper which helps us translate different language queries into English and passes it to the next level.

We must understand here that the importance of Whisper is to identify the language and translate and for testing this the audio file in Telugu stating “spotify ante enti?” was giving which was perfectly translated into “What is Spotify?”.

Next indexing was done where the query was indexed to solve it.

Synthesis:

In this step the query was solved and the answer for the question “What is Spotify?” was answered by the system.

To check the system accuracy further another audio file in Telugu was provided to the system which served as the query.

After the audio file was translated into English the solution was provided by the system showing the successful process.

Models Used:

Hugging Face model

Whisper
