# StartupGenAI Backend

Welcome to the **StartupGenAI Backend**, a scalable API designed to generate business plans for startup ideas using AI services such as OpenAI's GPT.

---

## 🚀 Features

- **Input startup ideas**: Provide an idea, business model, and industry.
- **AI-generated business plans**: Outputs detailed pitches, market analysis, investor strategies, and projections.
- **Future Enhancements**:
  - User authentication & generation history storage.
  - PDF downloads & shareable links.
  - Tiered plans with rate-limiting.

---

## 🛠️ Getting Started

### 1. **Clone the Repo**

```bash
git clone https://github.com/<your-username>/startupgenai-backend.git
cd startupgenai-backend
```

### 2. **Install Dependencies**

```bash
pip install -r requirements.txt
```

### 3. **Set Environment Variables**

Create a `.env` file in the root directory and add:

```env
OPENAI_API_KEY=sk-xxxxxxx
```

### 4. **Run the Server**

```bash
uvicorn app.main:app --reload
```

API is accessible at: `http://127.0.0.1:8000/api/generate/`

---

## 📑 API Documentation

### **Endpoint**: `POST /api/generate/`

#### **Request Body**:
```json
{
  "idea": "AI-powered plant health app",
  "business_model": "Freemium",
  "industry": "Technology"
}
```

#### **Response**:
```json
{
  "pitch": "Your elevator pitch here...",
  "market_analysis": "Market insights...",
  "investor_section": "Attract investors...",
  "projections": "Growth projections..."
}
```

---

## 🗂️ Project Structure

```
startupgenai-backend/
│
├── app/
│   ├── main.py               # FastAPI entry point
│   ├── schemas.py            # Pydantic models
│   ├── routes/
│   │   └── generator.py      # Business plan generation route
│   ├── services/
│   │   └── ai_generator.py   # AI integration logic (OpenAI, etc.)
│   └── utils/
│       └── pdf.py            # For future PDF download feature
│
├── .env                      # API keys, config
├── requirements.txt
└── run.sh                    # Startup script
```

---

## 📌 Next Steps

### Phase 2

- **Authentication**: OAuth2 + JWT for secure API access.
- **Data Storage**: Save generation history (e.g., MongoDB/Postgres).
- **Downloads**: Generate PDF versions of business plans.

### Phase 3+

- Shareable links for generated plans.
- User dashboard with analytics.
- Pro-tier plans with quotas/rate limits.

---

## 🤝 Contributing

Feel free to open issues or PRs to improve this project.

---

## 🛡️ License

This project is licensed under the MIT License.
