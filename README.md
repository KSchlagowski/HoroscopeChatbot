# HoroscopeChatbot

## Project Overview
HoroscopeChatbot is an AI-powered chatbot designed to provide detailed horoscope insights for 2025. Utilizing Retrieval-Augmented Generation (RAG) and Pinecone vector storage, the chatbot delivers highly accurate and context-aware responses to user queries about horoscopes. This project highlights expertise in language models, vector databases, and AI-driven chat interfaces.

## Features
- **Accurate Horoscope Predictions for 2025**: Get personalized horoscope insights based on stored data.
- **Natural Language Interaction**: Ask questions in plain language and receive clear, insightful responses.
- **RAG-based**: Combines the strengths of retrieval and generation for detailed and contextually relevant answers.
- **Modular and Scalable**: Easy to expand with more data or additional horoscope insights.

## How It Works
HoroscopeChatbot leverages Pinecone for vector storage and Ollama for embeddings and language model execution. Documents containing horoscope information are pre-processed, split, and embedded into Pinecone, making them retrievable based on user queries. The chatbot retrieves the most relevant context and uses the Llama 3.2 3B language model to generate informative responses【23†source】【24†source】.

## File Structure
- **horoscope2025.txt** – Data sourced from [AstroStyle 2025 Horoscopes](https://astrostyle.com/2025-horoscopes-astrology-forecasts-zodiac-signs/) and [KarmaWeather 2025 Horoscope](https://www.karmaweather.com/news/yearly-horoscope/2025-horoscope).
- **main.py** – Chatbot application that handles user input and provides horoscope insights【23†source】【24†source】.
- **pinecone_repository.py** – Handles document loading, splitting, and inserting data into Pinecone vector storage【23†source】.
- **config.json** – Configuration for embedding models, prompt templates, and document paths.
- **requirements.txt** – Lists necessary Python packages.

## Requirements
1. Fill in Pinecone api_key and index name in .env file.

2. Install the required dependencies:
```bash
pip install -r requirements.txt
```

## Usage
1. Start the chatbot by running:
   ```bash
   python main.py
   ```
2. Ask horoscope-related questions such as:
   ```bash
   >>> What activities will benefit Sagittarius's overall well-being?
   ```
   Output:
   ```
   Travel, outdoor activities, and career advancements are recommended for Sagittarius's well-being.
   ```
3. To exit, type `/exit`.

You can also upload custom data from file to Pinecone db by running:
  ```bash
  python pinecone_repository.py
  ```

## Examples
- *What activities will benefit Aries's overall well-being?*
> Based on the context provided, it seems that Aries would benefit from activities such as:
>
> * Relaxation and stress management techniques
> * Incorporating mindfulness or meditation into their routine to sustain energy throughout the year.
> * Engaging in physical activity to maintain energy levels.
>
> Additionally, prioritizing relaxation, rest, and self-care can help maintain mental sharpness and creativity, which is also beneficial for Aries's overall well-being.

- *How will Taurus's professional life evolve throughout the year?*
> According to the provided context, Taurus's professional life is expected to bring stability and growth in the first half of the year, but this feeling of unpredictability returns midway through the year. By mid-year, stability and growth in professional endeavors are anticipated, along with financial rewards. However, I don't have more specific details about how their professional life will evolve throughout the rest of the year beyond what is mentioned for Taurus's overall forecast for 2025.

## Configuration
- Update the `config.json` to modify prompt templates or adjust the embedding model.
- Ensure `PINECONE_API_KEY` `INDEX_NAME` is set in your environment variables for Pinecone usage.

## Key Components
- **LangChain** – Orchestrates retrieval and generation workflows.
- **Pinecone** – Stores horoscope data as vector embeddings for fast retrieval.
- **Ollama** – Provides language models and embeddings for document processing and chatbot responses.

## License
This project is licensed under the MIT License.

---
Made by [Kamil Schlagowski](https://github.com/KSchlagowski)
