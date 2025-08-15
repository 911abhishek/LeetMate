# LeetMate – Your Leet Buddy

LeetMate is a **Streamlit app** that helps you practice LeetCode more efficiently by fetching problem details, generating beginner-friendly tips, and producing easy/optimal solutions on demand using **Google Gemini**.  
It also supports light/dark themes and keeps a local CSV of problems up to date.

---
# 📷Screenshots
<img width="827" height="391" alt="LeetMate_ss" src="https://github.com/user-attachments/assets/759a0588-a593-4b9b-9ab2-b80b77775e42" />
<img width="826" height="390" alt="leetMate_ss2" src="https://github.com/user-attachments/assets/192e529b-9026-403a-b8e8-65bf91ad9533" />


## ✨ Features

- **Real-time problem lookup** – Fetches LeetCode problem metadata (title, difficulty, etc.).
- **Motivation + strategy via Gemini** – Generates motivational guidance and actionable suggestions tailored to the selected problem.
- **Easy & Optimal solutions** – Beginner-friendly approach or performance-oriented solution in your chosen language.
- **Update problem list** – Refreshes a local `dataBase.csv` with the latest LeetCode questions.
- **Light/Dark mode** – Switch themes for comfort during long sessions.

---

## 🧰 Tech Stack

- **Python + Streamlit** for the web UI
- **Requests** + **CSV** for API calls and local caching
- **Google Gemini API** (`google.generativeai`) for suggestions and solutions

---

## 🗂 How It Works

- **Fetch & cache problems** – Calls `https://leetcode.com/api/problems/all/` and updates `dataBase.csv`.
- **AI assistance** – Generates suggestions, beginner solutions, and optimal solutions using `gemini-1.5-flash`.
- **UI & theming** – Streamlit layout with custom CSS and icons (`Leet Mate.png`, `Leet Mate_dark.png`).

---

## 🚀 Getting Started

### Prerequisites
- Python 3.10+
- A **Google Gemini API key** (set as environment variable)

### Install

pip install streamlit google-generativeai requests
Configure your Gemini key
bash
Copy
Edit
# macOS/Linux
export GEMINI_API_KEY="your_key_here"

# Windows (PowerShell)
setx GEMINI_API_KEY "your_key_here"
Run
bash
Copy
Edit
streamlit run app.py

# 🧭 Usage
Enter a LeetCode Question Number and pick a language.

Click Show Suggestion, Show Easy Solution, or Show Optimal Solution.

Use Update Questions List to refresh the local CSV.

View Problem Title and Difficulty in the output pane.

# 📁 Project Structure
pgsql
Copy
Edit
leetmate/
├─ app.py
├─ dataBase.csv         # generated/updated by the app
├─ Leet Mate.png
├─ Leet Mate_dark.png
└─ README.md
# ⚠️ Known Limitations
Depends on LeetCode and Gemini APIs.

Internet connection required.

No authentication or personalized profiles yet.

# 🛣 Future Scope
LeetCode & GitHub API integration

Advanced filtering and leaderboards

Personalized learning paths

Mobile app version

ML-based coding insights
