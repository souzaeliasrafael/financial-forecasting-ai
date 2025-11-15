**Financial Forecasting AI**

Project Codename: Clotilde

Financial Forecasting AI is an end-to-end system that combines quantitative modeling, machine learning, and LLM-powered qualitative analysis to forecast financial market behavior.
The project implements a complete, production-ready pipeline — from raw data ingestion to modeling, backtesting, and cloud deployment — mirroring the workflows used by global trading desks, fintechs, and quantitative research teams.

**Overview**

This project integrates two complementary intelligence layers:

🔹 1. *Quantitative Pipeline*

Based on market data (OHLC, volume, volatility, technical indicators), processed through classical and deep learning architectures for time-series forecasting.

🔹 2. *Qualitative LLM Intelligence Layer*

Uses a Large Language Model API to analyze financial news, macroeconomic updates, company reports, and textual signals.
The LLM converts raw text into structured numerical features such as sentiment, risk scores, trend labels, and event indicators — which are then fused with quantitative features to enhance predictions.

This combination (Quant + LLM) makes the system robust, interpretable, and closer to real-world financial intelligence engines.

**Architecture**
## 🧱 Project Structure

```text
financial-forecasting-ai/
├── src/
│   ├── download_data.py      # Market data ingestion (MetaTrader 5)
│   └── __init__.py
├── data/                     # Local raw/processed data (gitignored)
│   ├── raw/
│   └── processed/
├── notebooks/                # EDA and experiments (planned)
├── docs/                     # Technical documentation (planned)
├── requirements.txt
├── .gitignore
├── .env                      # Credentials (gitignored)
└── README.md
```

*Main Features*

✔ Quantitative Layer

* OHLC historical data ingestion via MetaTrader5
* Multiple assets (indices, FX, equities, crypto, ETFs, FIIs)
* Rolling windows, lags, volatility measures
* RSI, MACD, EMAs, stochastic oscillators
* Scaling, normalization, and gap handling
* Baseline and advanced ML/DL forecasting models

✔ Qualitative LLM Intelligence

* LLM API extracts structured financial signals from text:
* Sentiment score (–1 to 1)
* Risk score (0 to 1)
* Directional trend (bearish / neutral / bullish)
* Event indicators: earnings, regulation, lawsuits, macro crises
* Structured summaries for daily qualitative context
* These features augment the numerical dataset and are fused before training.

✔ Backtesting & Evaluation

* Time-aware train/test split
* Walk-forward validation
* Return simulation based on forecasts
* Sharpe, Sortino, drawdown
* Strategy comparison against buy-and-hold

✔ Cloud Deployment (Phase 2–3)

* AWS S3 (data lake)
* AWS Glue + Athena (catalog + queries)
* Lambda API for real-time predictions
* Streamlit / Gradio dashboard
* Automated retraining pipelines

**Tech Stack**

Languages & Libraries

* Python 3.11
* MetaTrader5
* Pandas, NumPy
* Scikit-learn
* Matplotlib
* Python-dotenv
* TensorFlow / PyTorch (Phase 3)
* LLM Integration
* Any provider with a Chat/Completions API
* JSON-structured financial analysis prompts
* Feature extraction pipeline
* Cloud & MLOps

(Applied in later phases)

* AWS S3, AWS Glue, Athena
* AWS Lambda + API Gateway
* CI/CD with GitHub Actions

**Roadmap**
Phase 1 — Local Development (Current)

✔ Project setup

_ MetaTrader 5 ingestion

_ Numerical preprocessing

_ Baseline ML model (Prophet, XGBoost, LSTM)

_ LLM qualitative signal extraction

_ Feature fusion (Quant + LLM)

_ Metrics & evaluation

Phase 2 — Cloud Integration
Automated ETL on AWS; Data lake architecture (S3 + Glue + Athena); Real-time inference API; Dashboard for visualization; Pipeline for scheduled retraining

Phase 3 — Advanced Modeling
Transformer-based forecasting models; Explainability (SHAP/LIME); Portfolio optimization strategies; Automated reporting + event-driven insights

**Getting Started**
1. Create conda environment

    conda create -n clotilde python=3.11

    conda activate clotilde

2. Install dependencies

    pip install -r requirements.txt

3. Set up .env

    MT5_LOGIN=YOUR_LOGIN
    MT5_PASSWORD=YOUR_PASSWORD
    MT5_SERVER=YOUR_SERVER



    LLM_API_KEY=YOUR_KEY
    LLM_API_URL=YOUR_ENDPOINT

4. Download market data

    python -m src.download_data

5. Run preprocessing and modeling 

    *(coming soon as modules evolve)*

**Contact**

This project is actively developed as part of an international machine learning/quantitative finance portfolio.
For inquiries, collaboration, or discussion about the architecture, feel free to reach out.