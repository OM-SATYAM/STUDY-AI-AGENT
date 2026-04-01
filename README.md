# 📚 Study AI Agent

An AI-powered study assistant built with **Google Gemini 2.0** that runs on **Google Colab**. Just add your free API key and start learning!

---

## ✨ Features

| Feature | Description |
|---|---|
| 💬 **Q&A Mode** | Ask any study question with conversation memory |
| 📝 **Summarizer** | Summarize notes or PDFs at different detail levels |
| 🧪 **Quiz Generator** | Auto-generate MCQ, True/False, or Short Answer quizzes |
| 🔍 **Concept Explainer** | Step-by-step explanations with analogies |
| 📅 **Study Planner** | Personalized multi-day study plans |

---

## 🚀 Quick Start

### Step 1 — Get a Free Gemini API Key
1. Go to [https://aistudio.google.com/app/apikey](https://aistudio.google.com/app/apikey)
2. Sign in with your Google account
3. Click **Create API Key** and copy it

### Step 2 — Open the Notebook in Google Colab
1. Go to [colab.research.google.com](https://colab.research.google.com)
2. Click **File → Open Notebook → GitHub**
3. Paste your GitHub repo link and open `main.ipynb`

### Step 3 — Add Your API Key
1. In Colab, click the 🔑 **Secrets** icon in the left sidebar
2. Click **Add new secret**
3. Name: `GEMINI_API_KEY` → Value: paste your key
4. Toggle **Notebook access** ON

### Step 4 — Run the Notebook
Click **Runtime → Run all** and you're ready! 🎉

---

## 💡 How to Use

### Ask a Question
```python
answer = agent.ask("What is Artificial Intelligence?")
print(answer)
```
---

**# Summarize Your Notes**
```python
summary = agent.summarize(my_notes, detail_level="detailed")
# detail_level options: 'brief' | 'medium' | 'detailed'
```
---

**# Summarize a PDF**
``` python
# Upload your PDF to Colab first, then:
summary = agent.summarize_pdf("/content/my_notes.pdf")
```
---

**# Take an Interactive Quiz**
```python
agent.take_quiz(
    topic="Python programming basics",
    num_questions=5,
    difficulty="medium"   # 'easy' | 'medium' | 'hard'
)
```
---

**# Explain a Concept**
```python
explanation = agent.explain(
    concept="Neural Networks",
    level="high school",   # 'elementary' | 'high school' | 'university' | 'expert'
    style="analogy"        # 'normal' | 'analogy' | 'eli5'
)
```
---

**# Create a Study Plan** 
```python
plan = agent.create_study_plan(
    subject="Data Science with Python",
    days_available=14,
    hours_per_day=2,
    goal="build and evaluate ML models"
)
```
---

⚙️ **Configuration Options**
| Parameter | Options | Default |
|---|---|---|
| detail_level | brief, medium, detailed | medium |
| difficulty | easy, medium, hard | medium |
| quiz_type | mcq, true_false, short_answer | mcq |
| style | normal, analogy, eli5 | normal |

---

**🔧 Troubleshooting**

GEMINI_API_KEY **not found**
→ Make sure you added it to Colab **Secrets** (🔑 icon), not as a regular variable, and toggled notebook access ON.

**Rate limit error (429)**
→ You hit the free tier limit. Wait 1 minute and try again.

**Quiz JSON error**
→ Just re-run the cell. The model occasionally adds extra formatting which the code auto-cleans, but retrying fixes it.

**PDF shows 0 characters**
→ Your PDF is image/scanned based. Copy-paste the text manually instead.

---

**📦 Dependencies**

• google-genai

• PyPDF2

These are installed automatically in Cell 1 of the notebook.

---

**🛠️ Built With**

•Google Gemini 2.0 — AI model

•Google Colab — Runtime environment

•PyPDF2 — PDF text extraction

---

**🤝 Contributing**

Pull requests are welcome! Some ideas for future features:

• Flashcard generator

• Math problem solver

• Code debugger assistant

• Voice input support

---

**Made with ❤️ for students everywhere!!**
