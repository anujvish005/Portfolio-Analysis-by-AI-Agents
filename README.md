# Portfolio-Analysis-by-AI-Agents
AI agents that analyze portfolio data to reveal performance, risk, and diversification, giving investors fast, clear financial insights.

Introduction

Managing an investment portfolio requires continuous tracking, evaluation, and decision-making. However, for working professionals, especially those with long and demanding schedules, maintaining a disciplined monitoring routine becomes almost impossible. With markets moving quickly and investment decisions depending on real-time data, missing signals—even for a day—can impact returns significantly.
The project “Portfolio Analysis by AI Agents” solves this problem by building a fully automated, multi-agent system that acts as a personal investment researcher. By combining automated data extraction, intelligent analytics, contextual reasoning, and AI-generated recommendations, the system provides a complete, hands-free portfolio management experience.
This capstone demonstrates how AI agents can independently gather information, analyze market conditions, and produce actionable insights similar to what a financial analyst would deliver—within seconds, using only a single notebook cell. The project showcases multi-agent orchestration, tool-based automation, contextual memory, and real-world workflow design, aligning strongly with the goals of the Google × Kaggle AI Agents program.

Problem Statement

Many retail investors struggle to consistently monitor their portfolios. A typical example is a full-time working professional whose day runs from 10 AM to 10 PM—during the very hours when the stock market is active. This leads to multiple challenges:
Inability to monitor price fluctuations or intraday volatility
No time to track technical indicators such as RSI, MACD, or moving averages
Difficulty reviewing fundamentals (PE, PB, ROE, ROCE) for long-term evaluation
Missing important news that may impact stock performance
Reliance on rushed or incomplete research leading to poor decision-making
Lack of consistent, data-backed strategy and insights
Manually checking apps like Zerodha or Groww, reading charts, refreshing indicators, and scanning financial news daily is unrealistic. As a result, crucial opportunities are missed, risks go unnoticed, and portfolio performance suffers.

The core question becomes:
“How can an investor with no time efficiently manage their portfolio, track trends, and make informed decisions?”
This project answers that question by building an autonomous, agent-driven investment assistant.

Project Solution Overview

The solution is an end-to-end automated Portfolio Analysis Agent System powered by multiple AI agents, structured to perform independently yet collaboratively. The system does the work of a financial analyst, data researcher, and market scanner—without requiring user intervention.

With a single click, the agents perform the following steps:

Secure login to MCP-enabled broker systems (like Zerodha MCP)
Fetch current portfolio holdings and live market prices
Collect historical OHLC data for all stocks
Compute technical indicators including:
RSI (Relative Strength Index)
MACD
SMA 20/50/200
Trend direction and strength
Scrape fundamental metrics such as:
PE Ratio
PB Ratio
ROE, ROCE
Market cap & earnings trends
Pull latest news & sentiment signals using Google Search
Run all insights through a Portfolio Report Agent

Generate:

BUY/HOLD/SELL decisions
Entry points, stop-loss levels, and target ranges
Risk warnings
Consolidated summary sheet
Ranked scoring of portfolio health

All of this is achieved with minimal user interaction. The system is designed to behave like a personal research assistant, working automatically in the background.

Value Proposition
The project delivers strong value to investors—especially busy professionals—by providing:

a. Hands-Free Portfolio Management
The entire research process is automated. No need to manually log in, track charts, or search news.

b. Faster and More Consistent Decisions
AI agents process structured workflows consistently every time, avoiding human errors or emotional bias.

c. Daily/Weekly Investment Briefing Reports
The system generates insights and summaries instantly, replacing hours of manual research.

d. Actionable Trading Recommendations
Outputs are not vague insights—they include precise decisions:
BUY/HOLD/SELL
Entry ranges
Stop-loss levels
Target projections

e. Agent-Assisted Reasoning
The advisor agent cross-references:
technical indicators
fundamentals
news sentiment
price patterns
to deliver expert-level actionable strategies.
Overall, the project transforms how an everyday investor can analyze and respond to market conditions using AI agents.

System Architecture
The multi-agent architecture is structured into four specialized agents, each performing a well-defined task:

a. Portfolio Intake Agent
Reads asset list from the user or broker system
Validates ticker symbols and structure
Converts data into a structured dataframe / JSON
Initiates the analysis workflow
This agent ensures the pipeline receives clean and well-formatted data.

b. Market Data Agent
Fetches live prices via MCP or external APIs
Pulls OHLC (Open-High-Low-Close) historical data
Computes daily returns, volatility, and trends
Calculates:
Current value
Portfolio weight
Unrealized P&L
It acts as the "data aggregator" agent.

c. Analytics Agent
Runs the core calculations:
RSI, MACD, SMA20/50/200
Trend classification (uptrend, downtrend, sideways)
Support/resistance detection
Fundamental metrics scraping
Diversification score
Portfolio risk level
Identifies:
top gainers
top losers
overweight/underweight sectors
This agent extracts the signals needed for trading decisions.

d. Advisor Agent (LLM-powered)
This is the decision-making brain.
It uses LLM reasoning to produce:
Stock-wise actionable decisions
Portfolio risk assessment
Suggested rebalancing strategies
Trade plans (entry, stop-loss, target)
Warnings about news or volatility
Consolidated summary for the entire portfolio
The Advisor Agent transforms raw analysis into human-centric investment guidance.

Agent Orchestration Flow
The workflow of the system operates sequentially and intelligently:
User → Portfolio Intake Agent
→ Market Data Agent
→ Analytics Agent
→ Advisor Agent
→ Final Portfolio Report
Each agent passes tools, memory, and structured context forward. This makes the entire system modular, scalable, and easy to debug.

Tools & Techniques Demonstrated
This project demonstrates multiple key concepts from the Google × Kaggle AI Agents course:

✔ Multi-Agent Collaboration
Sequential and functional division of work using specialized agents.

✔ MCP Tools
Integration with:
Zerodha MCP for secure holdings
Custom data-fetching tools
Google Search for news analysis

✔ Sessions & Memory
InMemorySessionService
Agent-level state tracking
Context-aware report generation

✔ Observability & Logging
ADK LoggingPlugin
Custom observability plugin
Python logging for tracking
Step-by-step agent traces

✔ Context Engineering
Well-structured JSON passed between agents ensures predictable outputs.
Overall, the project is an excellent showcase of practical AI agent development.

Notebook Structure
Notebook is organized into logical sections aligned with the agent architecture:

a. Setup & Dependencies
Load libraries
Configure logging
Initialize tools

b. Observability Layer
Logging Plugin
Custom event tracker

c. MCP Agent Integration
Login to Zerodha MCP
Fetch holdings
LTP (Live Trading Price) functions

d. Analytics Pipeline
OHLC data extraction
Technical indicator calculations
Fundamentals scraping

e. Portfolio Report Agent
Google Search news pipeline
LLM analysis
Recommendation formatting

f. Final Execution Cell
Single click run pipeline
Final report displayed

This structure emphasizes clarity, reproducibility, and modularity.

Process Flow Summary
The entire workflow follows this logic:
User triggers analysis
System retrieves holdings via MCP
Market data is fetched and enriched
Technical + fundamental analytics run
News & sentiment collected
Advisor Agent synthesizes insights
Final portfolio report is generated
The output is a clear, easy-to-read trading dashboard.

Conclusion
The "Portfolio Analysis by AI Agents" project demonstrates how AI can transform traditional investment research into an automated, intelligent, and time-efficient process. For investors with busy schedules, this system behaves like a full-time research assistant—tracking data, analyzing trends, monitoring risk, and generating actionable advice.
By leveraging multi-agent orchestration, MCP tools, observability frameworks, and LLM-driven decision-making, this project provides a real-world, production-ready application of AI agents in finance. Its modular design, clean workflow, and practical relevance make it not only a strong capstone submission but also a foundation for future enhancements such as automated alerts, WhatsApp reports, strategy back testing, or deployment on cloud platforms.
This capstone showcases the power of AI agents in solving complex, time-sensitive tasks—and represents a meaningful contribution to modern portfolio management powered by intelligent automation.




Portfolio Analysis by AI Agents
AI agents that analyze portfolio data to reveal performance, risk, and diversification, giving investors fast, clear financial insights.
