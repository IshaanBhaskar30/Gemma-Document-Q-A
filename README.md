📊 Gemma Model Document Q&A

📘 Project Overview

This Streamlit-powered application allows users to ask questions about official U.S. Census PDF documents using the LLaMA 3-8B model (via Groq) and Google's Gemini embeddings. It integrates LangChain's Retrieval-Augmented Generation (RAG) workflow, enabling semantic search over document chunks and providing precise, grounded answers.

📂 Document Sources

This app uses the following U.S. Census Bureau documents:

->Health Insurance Coverage Status and Type by Geography: 2021 and 2022

->Poverty in States and Metropolitan Areas: 2022

->Household Income in States and Metropolitan Areas: 2022

->Occupation, Earnings, and Job Characteristics

All PDFs are stored in the ./us_census/ directory and automatically loaded during embedding.

🔍 Key Features

->📥 Automatically load and split multiple government PDF reports.

->🔐 Securely input your Groq & Google API Keys in the sidebar.

->🧠 Ask natural language questions about document content.

->⚡ Fast and accurate answers using LLaMA 3 via Groq + Gemini Embeddings.

->📚 Explore the top-matching document chunks used for answering your query.

🧠 How It Works

->PDFs are loaded and split into text chunks using LangChain.

->Chunks are embedded using Google's Gemini embedding model (embedding-001).

->Chunks are stored in a FAISS vector store.

->When a user asks a question:

    o The app retrieves the most relevant chunks.

    o A prompt is constructed using a custom RAG template.

    o The LLaMA 3 model (Groq API) generates the answer.

🖼️ UI Overview

->Sidebar:

    o Google API Key (for embeddings)

    o Groq API Key (for LLM)

    o "📚 Embed Documents" button

->Main Panel:

    o Question input field

    o Streamed answer from LLaMA 3

    o Expandable section to view relevant document chunks

