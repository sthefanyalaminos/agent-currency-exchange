# 💱 AI Currency Exchange Agent (n8n)
[Traduzir para Português](https://github.com/sthefanyalaminos/agent-currency-exchange/blob/main/README.md)
 
Low-code automation built in n8n: an AI agent specialized in finance and currency exchange, with conversation memory and the ability to look up real-time currency quotes.
 
The agent chats in natural language about currency exchange and finance. Whenever the user asks for a currency quote, the agent uses an HTTP Request to fetch the current value from AwesomeAPI before answering, so it works with real data. It also keeps the conversation history through persistent memory in Redis, enabling context-aware dialogue.
 
---