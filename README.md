# E-Commerce Sales Chatbot

An intelligent chatbot for e-commerce applications, built using the **Microsoft Bot Framework**. It helps users search for products, explore categories, and simulate shopping cart actions using cognitive services like LUIS, Azure Search, and Text Analytics.

This bot demonstrates how conversational AI can enhance the shopping experience through natural language interactions.

---

## 🔧 Project Updates

- Updated to use **Moltin v2 API** for generating search indexes.
- Transitioned from **Restify to Express** for improved performance and middleware flexibility.
- LUIS model upgraded to schema version 2.1.0.
- Temporarily removed Recommendations API due to deprecation by Microsoft. Logic still exists in code and can be re-enabled once supported.

⚠️ Note: This bot still uses Microsoft’s original **State API**, which is deprecated but functional. For production use, it's recommended to switch to [custom state storage using CosmosDB](https://learn.microsoft.com/en-us/bot-framework/nodejs/bot-builder-nodejs-state-azure-cosmosdb).

---

## 💡 Features

- Product search using [Azure Search](https://azure.microsoft.com/en-us/services/search)
- Natural language understanding using [LUIS](https://www.luis.ai/)
- Sentiment detection using [Text Analytics API](https://www.microsoft.com/cognitive-services/en-us/text-analytics-api)
- Shopping cart logic stored in memory
- Extensible structure for integrating e-commerce APIs

---

## 🚀 Getting Started

To run the project locally, you’ll need:

1. A **Moltin** (now [Elastic Path Commerce Cloud](https://www.elasticpath.com/)) account and sample product data
2. An **Azure Search** service with 3 indexes: `categories`, `products`, `variants`
3. A trained **LUIS** model (you can import the included app from `/luis`)
4. Optional: a **Text Analytics API** subscription for sentiment analysis

---

### 🔑 Environment Variables

Before running the bot, configure the following environment variables:

```
MICROSOFT_APP_ID=<your-app-id>
MICROSOFT_APP_PASSWORD=<your-app-password>
SEARCH_APP_NAME=<your-azure-search-app-name>
SEARCH_API_KEY=<your-azure-search-api-key>
LUIS_ENDPOINT=<your-luis-endpoint-url>
SENTIMENT_API_KEY=<your-text-analytics-key>
SENTIMENT_ENDPOINT=<your-text-analytics-endpoint>
```

ℹ️ You can use `.env` file or directly export variables in the terminal.

---

### 🧪 Run Instructions

1. Clone or download the repository.
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the server:
   ```bash
   npm start
   ```

The bot can be tested locally using the [Bot Framework Emulator](https://github.com/microsoft/BotFramework-Emulator).

---

## 🛠️ To-Do

- Integrate persistent shopping cart via external API or DB
- Enable real-time checkout functionality
- Extend to support multiple languages and locale-based search
- Improve visual product rendering in chat

---

## 📄 License

MIT License  
Feel free to modify and build upon this project for educational or commercial use.
