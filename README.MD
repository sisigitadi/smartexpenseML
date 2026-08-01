🧠 Smart Expense by M/L - Client-Side ML Expense Categorizer

A smart, automated financial tracking web application powered by Client-Side Machine Learning (Zero API Key & Zero Cost). It automatically classifies income and expense transactions based on natural language keywords directly in the user's browser, without sending any data to external servers.

🌟 Key Features

🤖 100% Client-Side Machine Learning: Built on a native Vanilla JS Naive Bayes Text Classifier that processes text locally without needing backend servers or paid APIs (OpenAI/Gemini).

🔄 Active Online Retraining (Interactive Feedback Loop): The ML model learns dynamically whenever a user modifies or corrects a category in the history table. Learned weights are saved locally in localStorage.

🗣️ Natural Language & Voice Input: Parses free-form natural language text (e.g., "Bought iced latte $4.5" or "Monthly salary $2500") and supports speech recognition (Web Speech API).

🔤 Dual Language Support (🇮🇩 ID & 🇬🇧 EN): Complete localization for the UI, ML keyword lexicon, sample dataset, and CSV exports in both Indonesian and English.

💱 Dynamic Real-Time Exchange Rate Engine: Seamless currency switcher between IDR (Rp) and USD ($) integrated with a live exchange rate API (open.er-api.com). Dynamically converts amounts across all dashboard components.

🌗 Multi-Theme Selector: Toggle between Light, Dark, and System (Auto) modes with adaptive Chart.js visual themes.

📊 Interactive Visual Dashboard: Features net balance summary cards, interactive doughnut charts, bar charts, search filtering, and CSV export.

🔒 100% Privacy Preserved: All financial data is stored exclusively in your browser's localStorage and never leaves your device.

🛠️ Architecture & ML Workflow

[Text / Voice Input] ➔ [Regex NLP Parser] ➔ [Word Tokenization]
                                                   │
                                                   ▼
[Dashboard UI] ◄─ [Doughnut/Bar Charts] ◄─ [Naive Bayes Classifier]
      │                                            │
      ▼                                            ▼
[Category Correction] ➔ [Online Retraining] ➔ [Update Local Storage]


Regex NLP Parser: Extracts currency values (such as 15rb, 50k, 2.5jt, $30, $4.50) from transaction descriptions.

Tokenization: Breaks the transaction description into normalized individual tokens.

Naive Bayes Scoring: Computes probability scores for each token against 8 category classes (Food & Drinks, Transportation, Bills & Utilities, Shopping, Entertainment, Health, Income, and Others).

Interactive Retraining: When a user changes a category in the table, the token weights in local memory are automatically reinforced (+5 weight increment) and saved to localStorage.

🚀 Getting Started

1. Running Locally (No Installation Required)

Clone or download this repository:

git clone https://github.com/username/smart-expense-ml.git


Double-click or drag the index.html file into any web browser (Chrome, Firefox, Edge, Safari).

2. Deploy to GitHub Pages (2 Minutes)

Create a new repository on GitHub (e.g., smart-expense-ml).

Upload the index.html file to the repository.

Navigate to Settings ➔ Pages.

Under Branch, select main and / (root) folder, then click Save.

Your web app will be live and accessible globally in seconds!

💻 Tech Stack

Frontend Core: HTML5, Vanilla JavaScript (ES6+).

Styling: Tailwind CSS (via Play CDN) + Custom Glassmorphism CSS.

Typography & Icons: Plus Jakarta Sans (Google Fonts) & FontAwesome 6.

Data Visualization: Chart.js v4.

Speech Recognition: Web Speech API.

Exchange Rate API: Open ER API (Free Keyless API).

📜 License

Distributed under the MIT License. Feel free to modify, distribute, and use for personal portfolio or commercial purposes.