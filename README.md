README - Market Sentiment Analyzer using LangChain and Azure OpenAI

🧠 Overview
This project implements a LangChain-powered pipeline that performs real-time market sentiment analysis for a given company. It uses Azure OpenAI's GPT-4o model to analyze financial news and generate structured sentiment insights.

🚀 Features
• Accepts a company name as input

• Extracts or generates its stock code using Yahoo Finance

• Fetches recent news headlines using DuckDuckGo search

• Analyzes sentiment using Azure OpenAI GPT-4o

• Outputs structured JSON with sentiment and named entities

• Logs and traces the pipeline using mlflow

pip install langchain openai mlflow yfinance duckduckgo-search

🔐 Azure & mlflow Configuration

Set the following environment variables in your.env file:

AZURE_OPENAI_API_KEY = "your-azure-openai-api-key"

AZURE_OPENAI_ENDPOINT = "your-azure-endpoint"

For mlflow:

mlflow.set_tracking_uri("your-mlflow-tracking-uri")

mlflow.set_experiment("MarketSentimentAnalyzer")

🧪 How to Run
Open the notebook:
jupyter notebook Market_Sentiment_Analyzer.ipynb

Run all cells. The notebook will:

• Ask for a company name (e.g., 'Microsoft')

• Extract its stock code

• Fetch recent news

• Analyze sentiment using GPT-4o
• Output a structured JSON
• Log everything to mlflow

📦 Sample Output
{
  "company_name": "Microsoft",
  "stock_code": "MSFT",
  "newsdesc": "...",
  "sentiment": "Positive",
  "people_names": ["Satya Nadella", "Sam Altman"],
  "places_names": ["Redmond", "San Francisco"],
  "other_companies_referred": ["OpenAI", "Google", "Amazon"],
  "related_industries": ["Cloud Computing", "Artificial Intelligence"],
  "market_implications": "...",
  "confidence_score": 0.92
}
