# 📝 TextSummerizer

A simple AI-powered text summarization web app built with **Streamlit** and the **Google Gemini API**. Paste text into the app, choose a summary style, adjust creativity, and generate a concise summary that can be downloaded as a `.txt` file.

## ✨ Features

- 🤖 AI-powered summarization with Google Gemini
- 📝 Three summary styles:
  - Three bullet points
  - A single sentence
  - A paragraph for a non-technical reader
- 🎛️ Adjustable creativity/temperature
- ✅ Input validation with minimum and maximum text limits
- 📊 Displays input characters, summary word count, and tokens used
- 📥 Download generated summaries as a text file
- ⚡ Streamlit interface with cached Gemini client
- 🔐 API key loaded from environment variables or Streamlit secrets
- ⚠️ Includes a warning that AI-generated summaries may omit or misstate details

## 🛠️ Tech Stack

- **Python**
- **Streamlit**
- **Google Gemini API / Google Gen AI SDK**

## 📁 Project Structure

```text
TextSummerizer/
├── .streamlit/
└── app.py
```

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/vyasanbmathew2008/TextSummerizer.git
cd TextSummerizer
```

### 2. Create a virtual environment

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install dependencies

```bash
pip install streamlit google-genai
```

### 4. Configure your Gemini API key

Set the API key as an environment variable:

```bash
export GEMINI_API_KEY="your_api_key_here"
```

Or configure it using Streamlit secrets.

> **Never commit your API key to GitHub.**

### 5. Run the application

```bash
streamlit run app.py
```

The application will open in your browser.

## ⚙️ How It Works

1. Enter or paste text into the Streamlit text area.
2. Select the desired summary format.
3. Adjust the creativity value if needed.
4. Click **Summarise**.
5. The app sends the prompt to the configured Gemini model.
6. The generated summary and usage information are displayed.
7. Download the result as `summary.txt`.

## 🔒 Input Limits

The application validates the input before making an API request:

- Minimum: **200 characters**
- Maximum: **20,000 characters**

This helps prevent unnecessary API requests and keeps the input within the application's intended limits.

## ⚠️ Disclaimer

This project uses a generative AI model. AI-generated summaries can occasionally omit, misunderstand, or misstate information. Always check the original source before relying on an important summary.

## 📌 Project Status

This project is an educational AI/ML application demonstrating how to integrate a generative AI model with a Streamlit frontend.

## 📄 License

No license has currently been specified for this repository.

## 👨‍💻 Author

**Vyasan B Mathew**

GitHub: https://github.com/vyasanbmathew2008
