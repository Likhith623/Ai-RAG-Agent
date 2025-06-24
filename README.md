# 🌟 AI Assistant – Universal Web & Document Conversational Agent

A world-class, production-ready AI assistant that combines **universal web search**, **document analysis (RAG)**, and **context-aware conversations**. Built with a Next.js frontend and a Flask backend, featuring seamless integration, real-time chat, file uploads, and robust cloud deployment.

---

## 🚀 Features

- **3-Step AI Process:**  
  1. Universal Web Search  
  2. Document Analysis (RAG)  
  3. Context-Aware AI Response

- **Document Upload & Q&A:**  
  Upload PDF, DOCX, TXT, or MD files and ask questions about their content.

- **Web Search Integration:**  
  Real-time web results using Serper API and NewsAPI.

- **Smart Conversations:**  
  Conversation history, context memory, and multi-turn chat.

- **Beautiful Next.js Frontend:**  
  Responsive UI, dark/light mode, glassmorphism, and animated transitions.

- **Production-Ready Backend:**  
  Flask API with RAG, web scraping, and Google Gemini AI integration.

- **Cloud Native Deployment:**  
  Google Cloud Run (no Docker needed), automatic CI/CD via GitHub Actions.

---

## 🏗️ Project Structure

```
agent623/
│
├── main.py                # Flask backend (API, RAG, web search, file upload)
├── requirements.txt       # Python dependencies
├── comprehensive_news_knowledge.txt # (Optional) Knowledge base
│
├── front_end/
│   ├── app/
│   │   ├── page.js        # Main Next.js chat interface
│   │   └── layout.js      # App layout
│   ├── public/            # Static assets
│   ├── next.config.mjs    # Next.js config (API URL, build settings)
│   ├── package.json       # Frontend dependencies & scripts
│   └── README.md          # Frontend-specific docs
│
├── .github/workflows/agent.yml # CI/CD pipeline (build, test, deploy)
├── .gitignore
└── README.md              # ← You are here!
```

---

## ⚡ Getting Started (Local Development)

### 1. **Backend (Flask API)**

```bash
# Install Python dependencies
pip install -r requirements.txt

# Set environment variables (create a .env file)
cp .env.example .env
# Edit .env with your API keys and Supabase credentials

# Start the backend server
python main.py
# By default runs on http://localhost:8080
```

### 2. **Frontend (Next.js App)**

```bash
cd front_end

# Install Node.js dependencies
npm install

# Set API URL for local dev (optional)
echo "NEXT_PUBLIC_API_URL=http://localhost:8080" > .env.local

# Start the frontend server
npm run dev

# Open http://localhost:3000 in your browser
```

---

## 📝 Usage

- **Sign in** with your email to start chatting.
- **Upload documents** (PDF, DOCX, TXT, MD) and ask questions about their content.
- **Ask anything:**  
  - "Summarize this document"  
  - "What are the key points in this PDF?"  
  - "What is the latest news about AI?"  
  - "Summarize this website: [URL]"
- **Switch between dark/light mode** for the best experience.

---

## ☁️ Cloud Deployment

### **Google Cloud Run (Recommended)**

- **CI/CD:**  
  Automated via [`.github/workflows/agent.yml`](.github/workflows/agent.yml)  
  - Builds, tests, and deploys both backend and frontend.
  - No Docker required (uses Google Buildpacks).
  - Secrets managed via GitHub Actions.

- **Frontend & Backend URLs:**  
  Automatically linked via environment variables.

### **Vercel (Frontend Only)**

- Deploy the `front_end` folder to [Vercel](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme).
- Set `NEXT_PUBLIC_API_URL` to your backend endpoint.

---

## 🔑 Environment Variables

Create a `.env` file in the root and set:

```env
SUPABASE_URL=your_supabase_url
SUPABASE_KEY=your_supabase_key
SERPER_API_KEY=your_serper_api_key
NEWSAPI_KEY=your_newsapi_key
NOVITA_API_KEY=your_novita_api_key
GEMINI_API_KEY=your_google_gemini_api_key
```

For frontend, set `NEXT_PUBLIC_API_URL` in `.env.local` or `.env.production`.

---

## 🧪 Testing

- **Backend:**  
  - Lint: `flake8 .`
  - Syntax: `python -m py_compile main.py`
- **Frontend:**  
  - Lint: `npm run lint`
  - Build: `npm run build`

---

## 📚 Learn More

- [Next.js Documentation](https://nextjs.org/docs)
- [Flask Documentation](https://flask.palletsprojects.com/)
- [Google Cloud Run](https://cloud.google.com/run)
- [Supabase](https://supabase.com/)
- [Serper API](https://serper.dev/)
- [Google Gemini AI](https://ai.google.dev/)

---

## 🤝 Contributing

Pull requests and issues are welcome!  
Please open an issue for bugs, feature requests, or questions.

---

## 🛡️ License

MIT License.  
See [LICENSE](LICENSE) for details.

---

## 🎉 Credits

- Built with [Next.js](https://nextjs.org), [Flask](https://flask.palletsprojects.com/), [Supabase](https://supabase.com/), [Google Gemini AI](https://ai.google.dev/), and [Serper API](https://serper.dev/).
- UI inspired by modern glassmorphism and conversational design.

---

**Enjoy your world-class AI