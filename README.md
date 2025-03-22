# 🤖 BotCrux - AI Chatbot SaaS Platform

A powerful chatbot SaaS application that allows users to create and deploy AI-powered chatbots using **ModelsLab API** and **OpenAI API**. Users can generate API keys, manage chatbot settings, and integrate with external applications via our secure API.

## 🚀 Features

- **Pre-trained AI Models** (ModelsLab API + OpenAI API)
- **Custom API Key Generation for Each Chatbot**
- **Rate Limiting & Usage Tracking**
- **Stripe Subscription & Webhook Integration**
- **NextAuth Authentication (Google, GitHub, Credentials)**
- **Prisma + MongoDB for Database Management**
- **Server Actions & API Routes for Seamless Requests**
- **Admin Dashboard for Managing Chatbots & Users**

## 🛠️ Tech Stack

- **Frontend**: Next.js, Tailwind CSS, ShadCN UI
- **Backend**: Next.js API Routes, Server Actions, Prisma, MongoDB
- **Authentication**: NextAuth.js
- **Payments**: Stripe API & Webhooks
- **AI Integration**: ModelsLab API + OpenAI API

## 📦 Installation

### 1️⃣ Clone the Repository

```sh
git clone https://github.com/yourusername/botcrux.git
cd botcrux
```

### 2️⃣ Install Dependencies

```sh
pnpm install
```

### 3️⃣ Setup Environment Variables

Create a `.env` file in the root directory and add:

```env
NEXTAUTH_URL=http://localhost:3000
NEXTAUTH_SECRET=your-secret-key
DATABASE_URL=mongodb+srv://your-db-url
STRIPE_SECRET_KEY=your-stripe-key
STRIPE_WEBHOOK_SECRET=your-webhook-secret
MODEL_LAB_API_KEY=your-modelslab-key
OPENAI_API_KEY=your-openai-key (optional)
```

### 4️⃣ Run the Project

```sh
pnpm dev
```

## 📡 API Usage

Each chatbot gets a unique API key. You can send a request to:

```sh
POST /api/chatbot/respond
Authorization: Bearer {YOUR_CHATBOT_API_KEY}
Content-Type: application/json

{
  "message": "Hello, chatbot!"
}
```

## 💳 Stripe Webhook

The webhook listens for subscription changes.

```sh
POST /api/stripe/webhook
```

Set the webhook URL in Stripe Dashboard.

## 📜 License

This project is licensed under the MIT License.

---

💡 **Contributions Welcome!** Fork and create a PR. 🚀

