# Gmail-RAG-automation

Gmail-RAG-automation is an automated email responder that leverages the power of Retrieval-Augmented Generation (RAG) to provide intelligent and context-aware replies to incoming emails. The system utilizes LangChain for processing and responding to emails based on the content of attached PDF files and previous emails.

## Overview

This project integrates multiple technologies to create a seamless workflow for automatically responding to emails. The key components include:

- **Gmail API**: To connect and fetch unread emails from the user's Gmail account.
- **LangChain**: A framework that facilitates the integration of Language Models (LLMs) with retrieval capabilities.
- **Pinecone**: A vector database used to store and retrieve embeddings generated from the email content.
- **Ollama LLM**: Utilized to generate responses based on the context provided from emails and PDF content.

## Functionality

1. **Email Retrieval**: The application checks for unread emails in the user's inbox using the Gmail IMAP protocol.
  
2. **PDF Processing**: If a PDF file is included in the email, the application extracts the text from the PDF for further processing.
  
3. **Text Embedding**: The extracted text is split into chunks and embedded using a Hugging Face model, storing the embeddings in Pinecone.

4. **Response Generation**: Using the RAG system, the application generates an appropriate response to the email content and sends it back to the sender.

5. **Continuous Monitoring**: The API can be invoked to check for new emails continuously, ensuring timely responses to incoming queries.

## Technologies Used

- Python
- Django REST Framework
- LangChain
- Pinecone
- Ollama
- Gmail API
