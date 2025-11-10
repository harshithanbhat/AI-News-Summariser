### End to End Project Agentic AI Chatbots

# AI News Summariser

AI News Summariser is an end-to-end agentic AI chatbot project that fetches news articles from multiple sources, summarizes them using modern language models, and serves concise, informative summaries via a simple chat interface. The project demonstrates an integrated pipeline for data collection, preprocessing, summarization, and conversational delivery.

## Features
- Fetch articles from RSS feeds and public news APIs
- Extract and clean article content (HTML parsing, deduplication)
- Summarize articles using transformer-based models or external LLM APIs
- Chat interface to request summaries by topic, source, or time range
- Configurable summary length and detail level
- Extensible pipeline to add new sources, models, or UIs

## Quickstart

1. Clone the repo:
   git clone https://github.com/harshithanbhat77/AI-News-Summariser.git

2. Create and activate a virtual environment:
   python3 -m venv venv
   source venv/bin/activate

3. Install dependencies:
   pip install -r requirements.txt

4. Create a .env file in the project root with required credentials (example below).

5. Run the fetch pipeline and start the app (examples):
   python scripts/fetch_articles.py
   python app.py

## Configuration

Create a .env file with keys similar to:
- NEWSAPI_KEY=your_newsapi_key
- OPENAI_API_KEY=your_openai_api_key
- RSS_FEEDS=https://example.com/feed,https://another.com/feed
- SUMMARY_MODEL=openai/gpt-4 (or local model identifier)
- SUMMARY_LENGTH=short|medium|long

Adjust additional settings in config.yaml or config.py if present.

## Development

- Run tests:
  pytest

- Format code:
  black .

- Lint:
  flake8

## Project Structure (high level)
- scripts/           Data collection and preprocessing scripts
- models/            Summarization model wrappers and adapters
- app.py             Simple chat/summarization server or CLI entrypoint
- frontend/          Optional UI for conversational interaction
- tests/             Unit and integration tests

## Contributing
Contributions welcome — please open issues or pull requests. Follow existing code style, add tests for new functionality, and document any breaking changes.

## License
This project is licensed under the MIT License — see LICENSE for details.

## Contact
Created by harshithanbhat. For questions or help, open an issue on GitHub.
