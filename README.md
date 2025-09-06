# ScraperAgent

This project is an experimental **Scraper Agent** that blends:
- **Selenium** → to scrape dynamic websites that can’t be fetched with simple requests.
- **Prompt-based pipelines** → to clean, normalize, and structure raw text into a consistent schema.

Instead of writing brittle parsing logic for each site, the agent lets a language model shape scraped content into a well-defined CSV. This keeps the workflow flexible and maintainable.

---

## ✨ Why?
Scraping websites often gives you messy, inconsistent text (extra whitespace, strange symbols, half sentences). Traditional cleaning requires lots of regex and site-specific parsing.  
Here, I tested a new approach:  
1. Collect raw data with Selenium.  
2. Send raw text to a model with a **prompt describing the schema** (Date, user_id, comments).  
3. Get back structured, cleaned CSV data.  

---

## 📊 Experiments

### 1. **Edmunds Car Forum Comments**
- Selenium scrapes discussion threads dynamically.  
- The agent cleans text into a CSV with:  
  - `Date`  
  - `user_id`  
  - `comments`  
- Shows how prompt-based shaping can replace hand-coded parsing rules.

### 2. **IMDb Movie Reviews**
- Collected **50 reviews** using Selenium.  
- Prompt pipeline cleaned reviews to remove noise, normalize casing, and keep only the main comment.  
- A **before vs after cleaning** comparison shows the importance of text preprocessing.  
- Added a reporting step to analyze:  
  - What users liked (positives).  
  - What could be improved (negatives).  
- Exported results to CSV and generated PDF summaries.

---

## 📁 Repo contents
- `ScraperAgent.ipynb` – the main notebook with Selenium + prompt-cleaning pipeline.  
- `imdb_reviews_cleaned.csv` – cleaned IMDb review dataset (50 rows).  
- `imdb_review_report.pdf` – PDF summary report of likes vs. dislikes.  
- `README.md` – this file.  

---

## 🚀 Next steps
- Extend agent to other websites (forums, product reviews, news).  
- Try domain-specific prompts for better structured outputs.  
- Automate more advanced reports (sentiment charts, word clouds, etc.).  

---

## ⚡ Tech stack
- **Python**  
- **Selenium** for dynamic scraping  
- **BeautifulSoup** for HTML parsing  
- **OpenAI API** for prompt-based cleaning  
- **Pandas** for structuring data  
- **ReportLab** for PDF generation  

---

## 📌 Takeaway
ScraperAgent is a first attempt at **merging classical scraping with LLM-powered cleaning**.  
It demonstrates that instead of brittle regex pipelines, we can:  
- Describe what we want,  
- Let the model reshape messy text,  
- Still get strict CSV/structured outputs for downstream analysis.
