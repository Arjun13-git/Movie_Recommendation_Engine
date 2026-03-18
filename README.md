# 🎬 Enhanced Movie Recommendation Engine

An intelligent, agentic AI system designed to provide personalized movie recommendations, deep analytical insights, and real-time review synthesis. Built using **LangGraph**, **LangChain**, and **Google Gemini**, this project demonstrates the power of tool-using agents and Retrieval-Augmented Generation (RAG).

## 🚀 Features

- **🧠 Smart Recommendations**: Understands natural language queries to suggest movies based on mood (e.g., "I'm feeling adventurous"), genre, or specific similarities (e.g., "Movies like Inception").
- **📊 Comprehensive Movie Details**: Retrieves detailed metadata including plot summaries, cast, director, ratings (IMDb, Rotten Tomatoes, Metascore), awards, and box office performance via the OMDb API.
- **📰 Advanced RAG for Reviews**: Performs real-time web searches to fetch the latest critic reviews and news, synthesizing a comprehensive consensus using the Gemini LLM.
- **📚 Deep Analysis**: leverages Wikipedia to provide thematic comparisons, historical context, and director style analysis (e.g., "Compare Nolan and Villeneuve").
- **📺 Streaming Availability**: Identifies where to watch specific titles on streaming platforms in India (Netflix, Prime Video, Disney+ Hotstar, etc.).

## 🛠️ Tech Stack

- **Core Framework**: [LangChain](https://www.langchain.com/) & [LangGraph](https://langchain-ai.github.io/langgraph/)
- **LLM**: Google Gemini (via `langchain-google-genai`)
- **Search & Tooling**:
  - [Tavily API](https://tavily.com/) (Web search for RAG)
  - [OMDb API](https://www.omdbapi.com/) (Structured movie data)
  - Wikipedia (Deep context)
- **Vector Database**: ChromaDB (for potential future expansions/memory)
- **Environment**: Jupyter Notebook / Google Colab

## 📋 Prerequisites

To run this project, you will need API keys for the following services:

1.  **Google Gemini API Key**: For the LLM reasoning agent.
2.  **OMDb API Key**: For fetching structured movie metadata.
3.  **Tavily API Key**: For real-time web search and RAG capabilities.
4.  **LangSmith API Key** (Optional): For tracing and debugging agent steps.

## ⚙️ Installation

1.  **Clone the repository**:
    ```bash
    git clone https://github.com/yourusername/Movie-Recommendation-Engine.git
    cd Movie-Recommendation-Engine
    ```

2.  **Install dependencies**:
    Depending on your environment, you can install the required packages using pip:
    ```bash
    pip install -U langgraph langchain langchain-google-genai langchain-community tavily-python requests chromadb
    ```

## 🚀 Usage

1.  **Open the Notebook**:
    Launch `Movie_Recommendation_Engine.ipynb` in Jupyter Notebook, VS Code, or Google Colab.

2.  **Set up API Keys**:
    The notebook expects API keys to be set in the environment. You can set them directly in the notebook cell provided or use a `.env` file/Colab secrets.

    ```python
    import os
    os.environ["GEMINI_API_KEY"] = "your_gemini_key"
    os.environ["OMDB_API_KEY"] = "your_omdb_key"
    os.environ["TAVILY_API_KEY"] = "your_tavily_key"
    ```

3.  **Run the Cells**:
    Execute the notebook cells sequentially to:
    - Install libraries.
    - Initialize the agent tools (`findmovies`, `getmoviedetails`, `wikipediasearch`, etc.).
    - Build the LangGraph workflow.
    - Run the agent with your queries.

4.  **Example Queries**:
    Try asking the agent questions like:
    - "Recommend a psychological thriller released in 2023."
    - "I'm feeling sad, suggest some heartwarming movies."
    - "Tell me about Dune Part Two, including the plot, cast, and recent critic reviews."
    - "Compare the directing styles of Christopher Nolan and Ridley Scott."
    - "Where can I watch The Godfather in India?"

## 📂 Project Structure

```
.
├── Movie_Recommendation_Engine.ipynb   # Main project notebook containing agent logic
├── README.md                           # Project documentation
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

