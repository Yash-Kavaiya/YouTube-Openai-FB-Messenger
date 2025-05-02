# 🤖 OpenAI-Facebook Messenger Integration 🚀

![OpenAI + Facebook Messenger](https://img.shields.io/badge/OpenAI-Facebook%20Messenger-blue?style=for-the-badge)
![Node.js](https://img.shields.io/badge/Node.js-Express-green?style=for-the-badge)
![License](https://img.shields.io/badge/License-ISC-yellow?style=for-the-badge)

## 📖 Overview

This project connects Facebook Messenger to OpenAI's powerful GPT models, allowing users to interact with an AI assistant directly through Messenger. The application acts as a middleware, processing incoming messages from Facebook users, sending them to OpenAI for intelligent responses, and delivering those responses back to users in real-time.

## ✨ Features

- 🔄 Seamless integration between Facebook Messenger and OpenAI
- 🧠 Powered by OpenAI's GPT-4 model for high-quality responses
- ⚡ Real-time messaging with typing indicators for better user experience
- 🛡️ Webhook verification for secure Facebook integration
- 🔌 Easy setup with environment variables
- 🌐 Built on Express.js for reliable API performance

## 🛠️ Prerequisites

- Node.js (v12 or higher)
- Facebook Developer Account
- Facebook Page (to connect the Messenger bot)
- OpenAI API Key
- Hosting service (Heroku, Replit, etc.) with HTTPS support

## 📋 Environment Variables

Create a `.env` file in the root directory with the following variables:

```
PORT=5000
VERIFY_TOKEN=your_custom_verify_token
TOKEN=your_facebook_page_access_token
PAGE_ID=your_facebook_page_id
OPENAI_API_KEY=your_openai_api_key
```

## 🚀 Installation

1. Clone the repository
```bash
git clone https://github.com/RajKKapadia/YouTube-Openai-FB-Messenger.git
cd YouTube-Openai-FB-Messenger
```

2. Install dependencies
```bash
npm install
```

3. Start the server
```bash
npm start
```

For development with auto-restart:
```bash
npm run dev
```

## 📐 Architecture

```
├── helper/
│   ├── messengerApi.js  # Facebook Messenger API functions
│   └── openaiApi.js     # OpenAI API integration
├── routes/
│   ├── fbWebhookRoute.js # Facebook webhook endpoints
│   └── homeRoute.js      # Basic server endpoints
├── .gitignore
├── index.js             # Main application entry point
├── package.json
└── README.md
```

## 🔄 How It Works

1. Facebook sends incoming messages to the webhook endpoint
2. The application processes the message and extracts the user's query
3. The query is sent to OpenAI's GPT-4 model for processing
4. The AI-generated response is sent back to the user through Facebook Messenger
5. Typing indicators provide a more natural conversation experience

## 🔗 Facebook Messenger Setup

1. Create a Facebook Page and Facebook App in the [Facebook Developer Portal](https://developers.facebook.com/)
2. Set up Messenger in your Facebook App
3. Configure the Webhooks with your server URL and the VERIFY_TOKEN from your .env file
4. Subscribe to messaging events
5. Generate a Page Access Token and add it to your .env file as TOKEN

## 📝 API Endpoints

- `GET /`: Simple health check endpoint
- `GET /facebook`: Webhook verification endpoint for Facebook
- `POST /facebook`: Webhook endpoint for receiving messages from Facebook

## 🔧 Customization

You can customize the OpenAI model settings in `helper/openaiApi.js`:

```javascript
// Change model type
model: "gpt-4", // Options: gpt-3.5-turbo, gpt-4, etc.

// Adjust temperature for more/less creative responses
temperature: 0.8, // Higher = more creative, Lower = more deterministic

// Set maximum response length
max_tokens: 1080,
```

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](https://github.com/RajKKapadia/YouTube-Openai-FB-Messenger/issues).

## 📜 License

This project is [ISC](https://opensource.org/licenses/ISC) licensed.

## 🙏 Acknowledgements

- [OpenAI](https://openai.com/) for their powerful GPT models
- [Facebook Developer Platform](https://developers.facebook.com/) for the Messenger API
- [Express.js](https://expressjs.com/) for the web framework

---

Made with ❤️ by [Raj Kapadia](https://github.com/RajKKapadia)
