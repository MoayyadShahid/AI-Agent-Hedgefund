# AI-Agent Hedge Fund  
*A LangChain + Perplexity Sonar reference project (≤ 100 LOC)*  

> **Educational-use only — _not_ financial advice._**

---

## ✨ What it is
This repo shows how to turn a single stock-ticker input into a **data-driven trading thesis** using nothing but LangChain and the Perplexity Sonar API.  
Five lightweight AI agents cooperate in sequence:

| # | Agent role | Output |
|---|------------|--------|
| 1 | **Market-Data Analyst**      | Real-time price, volume & fundamental ratios |
| 2 | **Sentiment Analyst**        | Bullet-point news & social-media sentiment |
| 3 | **Macroeconomic Analyst**    | Interest-rate, GDP & other macro factors |
| 4 | **Quantitative Strategist**  | Entry/exit rules & position sizing |
| 5 | **Risk Manager**             | 4-bullet risk assessment & mitigations |

Everything is wired together with a single `SequentialChain`, giving clear, step-by-step reasoning.

---

## 🏗  Architecture

| Layer | Library / Service | Why |
|-------|-------------------|-----|
| **Agent orchestration** | [LangChain](https://python.langchain.com/) | Simple `LLMChain` + `SequentialChain` primitives |
| **LLM** | [Perplexity Sonar “reasoning” model](https://docs.perplexity.ai/) | Built-in web search → always-fresh market data |
| **Environment** | Python 3.9, single notebook / script | < 100 lines of actual code |


## 🚀 Quick Start

git clone https://github.com/MoayyadShahid/ai-agent-hedge-fund.git
cd ai-agent-hedge-fund

# create & activate a fresh conda env
conda create -n ai-hedge-fund python=3.9 -y
conda activate ai-hedge-fund

# install deps, set your key, run
pip install langchain==0.3.19 langchain-community==0.3.18 openai==1.65.2 ipykernel==6.29.5  

# add your own Perplexity Sonar API key
```PPLX_API_KEY = "API KEY GOES HERE"```
