# Langchain Chatbot Basics Notebook 🤖
This notebook serves as a practical guide to designing and implementing an LLM-powered chatbot using LangChain, focusing on enabling conversational memory. It covers fundamental concepts essential for building more advanced conversational AI applications.

✨ Concepts Covered
This notebook explores the following key LangChain concepts:

LLM Initialization: Setting up and interacting with a chat model (Groq's Gemma2-9b-It).
Basic Conversational Turns: Demonstrating simple single-turn interactions.
Message History (RunnableWithMessageHistory): How to integrate conversation history into a LangChain runnable to allow the chatbot to remember previous interactions.
Using an in-memory store for session-specific chat history.
Managing session_id for distinct conversations.
Prompt Templates: Crafting dynamic prompts with ChatPromptTemplate and MessagesPlaceholder for structured conversation input.
Adding system messages for defining AI behavior.
Conversation History Management (trim_messages): Techniques to limit the size of messages sent to the LLM to prevent context window overflow, including:
Specifying max_tokens and strategies like "last".
Integrating message trimming into a LangChain expression language (LCEL) chain using RunnablePassthrough.
🚀 Getting Started
To run this notebook, you'll need to set up your environment and obtain the necessary API key.

Prerequisites
Python 3.9+ installed.
A GROQ_API_KEY from Groq.
1. Clone the repository (if applicable)
If this notebook is part of a larger repository, clone it:

Bash

git clone [YOUR_REPOSITORY_URL_HERE] # Replace with the actual URL if known
cd [YOUR_PROJECT_DIRECTORY]
2. Set up Virtual Environment & Install Dependencies
It's highly recommended to use a Python virtual environment.

Bash

python -m venv .venv
source .venv/bin/activate # On macOS/Linux
# .\.venv\Scripts\activate # On Windows

# Install the required libraries for this notebook
pip install langchain-groq langchain-core langchain-community python-dotenv
3. Configure Environment Variables
Create a file named .env in the same directory as this notebook and add your Groq API key:

Code snippet

GROQ_API_KEY="your_groq_api_key_here"
Important: Add .env to your .gitignore file to prevent accidentally committing your secret keys.

4. Run the Notebook
Launch Jupyter Notebook or JupyterLab from your terminal in the directory containing 1-chatbots.ipynb:

Bash

jupyter notebook
# or
jupyter lab
Then, open 1-chatbots.ipynb from the Jupyter interface and run the cells sequentially to follow the tutorial and see the chatbot in action.

🧠 Key Learnings
By working through this notebook, you will learn how to:

Integrate Groq LLMs into LangChain applications.
Implement stateful chatbots that remember conversation history.
Effectively manage the LLM's context window for long conversations.
Build flexible and robust conversational chains using LangChain Expression Language (LCEL).
