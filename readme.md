AI-Powered Multi-Resume Chatbot
This project is an intelligent chatbot designed to help recruiters, hiring managers, or anyone working with multiple resumes to quickly and efficiently extract and compare information. Instead of manually reading through each document, you can simply upload a batch of PDF resumes and ask the AI questions in natural language.

The application uses a powerful combination of semantic search to find the most relevant information across all documents and Google's Gemini LLM to generate accurate, human-like answers.

Key Features
Multi-File Upload: Upload and process multiple PDF resumes at once.

Semantic Search: Understands the meaning and context of your questions, not just keywords.

Intelligent Answering: Uses the Gemini 2.5 Flash API to synthesize information and provide concise, accurate answers.

Source Citing: Clearly indicates which resume(s) the information was drawn from.

Interactive UI: A simple and clean web interface built with Gradio.

Secure: Keeps your secret API key safe and is never uploaded to GitHub.

How It Works
The application follows a modern Retrieval-Augmented Generation (RAG) pipeline:

PDF Parsing: Extracts clean text from each uploaded resume, intelligently splitting it into logical sections (Objective, Skills, Experience, etc.).

Embedding: Uses a sentence-transformer model to convert each text chunk into a numerical vector that captures its semantic meaning.

Indexing: Stores all these vectors in a high-speed FAISS index for efficient searching.

Retrieval: When you ask a question, it's also converted into a vector. FAISS then finds the most relevant text chunks from across all resumes.

Generation: The retrieved chunks and your original question are sent to the Gemini API, which generates a final, coherent answer.
