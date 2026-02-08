Design Goals & Principles

Accessibility first by using a voice-primary interface for low-literacy and first-time users.

Trustworthy AI ensured through Retrieval-Augmented Generation (RAG) using verified data.

Inclusive design with support for multiple regional dialects and low-bandwidth networks.

User agency maintained by guiding users without making decisions on their behalf.

High-Level Architecture

Cloud-native modular architecture designed for scalability and reliability.

Clear separation between frontend, backend, AI logic, and data layers.

Major System Components

Frontend engagement layer built as a React-based Progressive Web App optimized for low data usage.

Backend orchestration layer using FastAPI for API routing, session handling, and logic execution.

AI intelligence layer integrating LLMs with Speech-to-Text and Text-to-Speech services.

Knowledge vault implemented using a vector database for semantic retrieval of verified content.

Frontend Design

Low-literacy user interface with large buttons, high contrast visuals, and minimal navigation.

Streaming audio responses to reduce perceived wait time for users.

Backend & AI Logic

Intent classification to distinguish between educational and civic queries.

Recursive simplification to automatically break down explanations when users request clarity.

RAG Data Flow

User submits a voice or text query.

Speech-to-Text converts voice input into text.

Relevant documents are retrieved from the vector database.

LLM generates responses strictly based on retrieved verified data.

Text-to-Speech converts the response back into audio.

Technology Stack

Language models include Gemini 1.5 Flash or GPT-based models with model-agnostic design.

Bhashini APIs used for Indian language speech recognition and synthesis.

FastAPI used for high-performance asynchronous backend services.

PostgreSQL, Redis, and Pinecone/ChromaDB used for structured, session, and vector data storage.

Docker-based deployment on AWS or Google Cloud.

Database & Integrations

PostgreSQL stores user preferences and configuration data.

Redis maintains short-term conversation context.

Integration with verified government portals and open educational content sources.

Non-Functional Requirements

Voice-to-voice interaction target under 2 seconds.

Auto-scaling backend to handle peak usage.

Privacy ensured through PII masking and restricted data sharing with LLMs.

MVP Scope

Supports English and Hindi voice/text interaction.

Covers basic K–10 educational topics and selected government schemes.

Excludes offline support, advanced personalization, and deep third-party integrations.

Future Enhancements

Offline-first capability using edge-based AI for low-connectivity regions.

WhatsApp integration and automated learning assessments for broader reach.

Assumptions & Limitations

Assumes users have access to basic smartphones with working microphones.

Does not provide legal or medical advice; dialect accuracy may vary.
