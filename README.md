# 🤖 AI-Powered Meeting Agenda Generator

This project generates professional meeting agendas using an LLM (via the free Groq API) based on your input — including title, topics, and meeting duration. Built with **Gradio**, **Groq LLM**, **SQLite**, and **Python** (runs in Google Colab or locally).

---

## 🎥 Demo

<video width="100%" controls>
  <source src="demo.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

---

## 🚀 Features

- 🧠 Generates structured, bullet-pointed meeting agendas using Groq LLM
- ✅ Input validation: title, topics (comma-separated), and duration
- ✍️ Editable agenda output field
- 📥 Download agenda as PDF
- 🗃️ Saves agenda to a local SQLite database with timestamp
- 🌐 User-friendly UI built with **Gradio**

---

## 🛠️ Tech Stack

- Python 3.10+
- [Gradio](https://gradio.app/) – for frontend
- [Groq API](https://console.groq.com) – backend AI model
- [SQLite](https://sqlite.org/) – to log generated agendas
- [FPDF](https://pyfpdf.github.io/) – to export agenda as PDF

---

## 🧪 How to Run This Project

### ✅ Option 1: Run in Google Colab (Recommended)
1. Open the [Colab Notebook](LINK_TO_YOUR_NOTEBOOK)
2. Replace the API key section with your **Groq API Key**:
   ```python
   from openai import OpenAI
   client = OpenAI(
       api_key="your-groq-api-key",
       base_url="https://api.groq.com/openai/v1"
   )

## ✅ Option 2: Run Locally
git clone https://github.com/yourusername/your-repo-name.git
cd your-repo-name
pip install -r requirements.txt
python app.py

## 🔐 API Setup
from openai import OpenAI
client = OpenAI(
    api_key="your-groq-api-key",
    base_url="https://api.groq.com/openai/v1"
)
## 💡 Prompt Template\
Create a professional meeting agenda titled '{title}'.
Duration: {duration} minutes.
Topics to cover: {topics}.
The agenda should be clear, organized, and use bullet points.

## 🗃️ Database Schema
CREATE TABLE agendas (
  id INTEGER PRIMARY KEY AUTOINCREMENT,
  title TEXT,
  topics TEXT,
  agenda TEXT,
  timestamp TEXT
);
## 📥 Sample Input
Title: Product Launch Planning
Topics: Market analysis, Feature prioritization, Marketing strategy, Timeline
Duration: 45
## ✅ Sample Output
**Product Launch Planning Meeting Agenda**

**Duration:** 60 minutes

**Objective:** To discuss and finalize the product launch plan, ensuring a successful market entry for our new product.

**Agenda:**

1. Introduction and Objectives (5 minutes)
   - Review of meeting objectives and expected outcomes
   - Introduction of attendees and their roles

2. Market Analysis (15 minutes)
   - Review of target market trends and competitor analysis
   - Discussion of market size, growth potential, and customer needs
   - Key takeaways and recommendations for product launch

3. Feature Prioritization (15 minutes)
   - Review of product features and prioritization
   - Discussion of must-have, nice-to-have, and future development features
   - Alignment on feature set for launch

4. Marketing Strategy (15 minutes)
   - Review of marketing channels and tactics
   - Discussion of budget allocation and resource requirements
   - Key messaging and positioning for product launch

5. Timeline (10 minutes)
   - Review of product launch timeline and milestones
   - Discussion of critical path activities and dependencies
   - Alignment on launch date and key deadlines

6. Next Steps and Action Items (5 minutes)
   - Review of action items and responsibilities
   - Establishment of follow-up meeting or check-in

**Expected Outcomes:**
- Clear understanding of market trends and customer needs
- Prioritized feature set for product launch
- Defined marketing strategy and budget allocation
- Established product launch timeline and milestones

**Pre-Meeting Preparation:**
- Review of market analysis and competitor research
- Review of product features and prioritization
- Review of marketing strategy and budget allocation

*Note: The time allocated to each topic is an estimate and may vary based on the discussion and requirements.*
