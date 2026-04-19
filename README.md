# DevEcho: Commit Sentiment Analyzer

## Overview
DevEcho is an analytical pipeline designed to extract, classify, and respond to developer frustration identified within version control systems. It utilizes a custom-built Bidirectional Long Short-Term Memory (BiLSTM) network to evaluate sentiment in GitHub commit messages and generate automated corporate responses.

## Architecture
* **Data Extraction:** Aggregates commit messages via the GitHub Search API.
* **Classification:** Employs a PyTorch BiLSTM (built from scratch) to classify commit stress levels.
* **Semantic Search:** Integrates `sentence-transformers` and FAISS indexing to retrieve historical commits with similar semantic profiles.
* **Automated Response:** Interfaces with the Gemini API to dynamically generate structured corporate email responses based on frustration levels.

## Usage
1. Clone the repository.
2. Install dependencies: `pip install -r requirements.txt`
3. Configure your local environment variables in a `.env` file with `GITHUB_PAT` and `GEMINI_API_KEY`.
4. Execute the Jupyter Notebook to launch the Gradio interface.