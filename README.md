%%writefile /content/ScraperAgent/README.md
# ScraperAgent

This project is an experimental **Scraper Agent** that combines:
- **Selenium** – to scrape dynamic web pages (like forums or reviews).
- **Prompt-based pipeline** – to clean, structure, and normalize raw scraped text.

### ✨ Why?
Instead of writing fragile parsing logic for every website, I experimented with letting a language model:
1. Take messy, raw scraped text.
2. Clean and structure it into a strict schema (e.g., `Date`, `user_id`, `comments`).
3. Export results as CSV for easy analysis.

### 📊 Features
- Dynamic scraping with Selenium.
- Prompt-driven cleaning of reviews/comments.
- Example pipeline on IMDb reviews (50 reviews, cleaned vs. raw).
- Export of cleaned dataset to CSV & generation of analysis reports (e.g., likes vs. dislikes).

### 📁 Repo contents
- `ScraperAgent.ipynb` – the notebook with the scraping + prompt-cleaning pipeline.
- `README.md` – this file.

### 🚀 Next steps
- Extend to other sites (forums, e-commerce product reviews, etc.).
- Improve prompt templates for domain-specific cleaning.
- Explore automated report generation from cleaned data.

---

### 📥 Add & push the README
```bash
%cd /content/ScraperAgent
!git add README.md
!git commit -m "Add README.md"
!git push https://YourUsername:YOURTOKEN@github.com/YourUsername/ScraperAgent.git main
# ScraperAgent
