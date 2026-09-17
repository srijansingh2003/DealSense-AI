# DealSense AI 🚀

### Agentic Price Intelligence Platform

DealSense AI is an **agentic AI system for discovering and evaluating
online deals**. It automatically collects deals from RSS feeds, extracts
structured product information, estimates the fair value of products
using multiple AI/ML approaches, combines the predictions through an
ensemble, and sends a notification when a potentially attractive
opportunity is found.

## 🏗️ Architecture

``` text
                    ┌─────────────────────┐
                    │   DealNews RSS      │
                    │      Feeds          │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Deal Scraper /      │
                    │ HTML Parser         │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   Scanner Agent     │
                    │ Deal Selection      │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │    Preprocessor     │
                    │ Product Normalizer  │
                    └──────────┬──────────┘
                               │
                               ▼
              ┌─────────────────────────────────┐
              │       Ensemble Pricing Agent    │
              └────────────────┬────────────────┘
                               │
          ┌────────────────────┼────────────────────┐
          ▼                    ▼                    ▼
┌─────────────────┐  ┌──────────────────┐  ┌──────────────────┐
│ Frontier Agent  │  │ Specialist Agent │  │ Neural Network   │
│ RAG + LLM       │  │ Fine-tuned LLM   │  │ PyTorch Model    │
└────────┬────────┘  └────────┬─────────┘  └────────┬─────────┘
         │                    │                     │
         └────────────────────┼─────────────────────┘
                              ▼
                    ┌─────────────────────┐
                    │ Weighted Ensemble   │
                    │ Price Estimation    │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Opportunity Check   │
                    │ Discount > 50 ?     │
                    └──────────┬──────────┘
                               │
                         Yes   │
                               ▼
                    ┌─────────────────────┐
                    │ Messaging Agent     │
                    │ Pushover Alert      │
                    └─────────────────────┘
```

