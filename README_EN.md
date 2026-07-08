# 💱 AI Currency Exchange Agent (n8n)
[Traduzir para Português](https://github.com/sthefanyalaminos/agent-currency-exchange/blob/main/README.md)
 
Low-code automation built in n8n: an AI agent specialized in finance and currency exchange, with conversation memory and the ability to look up real-time currency quotes.
 
The agent chats in natural language about currency exchange and finance. Whenever the user asks for a currency quote, the agent uses an HTTP Request to fetch the current value from AwesomeAPI before answering, so it works with real data. It also keeps the conversation history through persistent memory in Redis, enabling context-aware dialogue.
 
---

## How it works
```
User sends a message in the chat
        │
        ▼
 ┌────────────────────── AI Agent ──────────────────────┐
 │                                                        │
 │   🧩 Google Gemini Chat Model  → generates responses   │
 │   💾 Redis Chat Memory         → keeps the context      │
 │   🌐 HTTP Request Tool         → fetches real quotes    │
 │      (AwesomeAPI)                 when needed           │
 │                                                        │
 └────────────────────────────────────────────────────────┘
        │
        ▼
   Response to the user
```
1. The user sends a question through the chat (e.g., "what's the dollar exchange rate today?").
2. The **AI Agent** (LangChain Agent node) receives the message and decides, based on its system prompt, whether it needs to look up a quote.
3. If it does, it triggers the **HTTP Request** tool, which queries **AwesomeAPI** and returns the current value of the currency.
4. **Google Gemini** (via the Google AI API) generates the final response in natural language, using the query result.
5. **Redis Chat Memory** stores the conversation history, so the agent remembers the context across following messages.