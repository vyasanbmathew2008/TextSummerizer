# 📝 Text Summerizer

> **AI-powered text summarization built with Python, Streamlit, and Google Gemini.**

TextSummerizer is a lightweight web application that turns long text into concise, readable summaries using the Google Gemini API. Choose the summary style, control the creativity level, generate the result, view usage statistics, and download the summary as a text file.

[![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Streamlit](https://img.shields.io/badge/Streamlit-App-FF4B4B?logo=streamlit&logoColor=white)](https://streamlit.io/)
[![Google Gemini](https://img.shields.io/badge/Google-Gemini-4285F4?logo=google&logoColor=white)](https://ai.google.dev/)

---

## ✨ Features

- 🤖 **AI summarization** powered by Google Gemini
- 📝 **Three summary styles**:
  - Three bullet points
  - A single sentence
  - A paragraph for a non-technical reader
- 🎛️ **Creativity control** with an adjustable temperature slider
- 🛡️ **Input validation** before sending an API request
- 📏 Supports text from **200 to 20,000 characters**
- 📊 Shows input character count, summary word count, and token usage
- 📥 **Download summaries** as `summary.txt`
- ⚡ Uses Streamlit resource caching for the Gemini client
- 🔐 Supports API keys through environment variables or Streamlit secrets
- ⚠️ Includes an AI accuracy disclaimer

## 🖥️ How It Works

```text
User enters text
       ↓
Input validation
       ↓
Choose summary style + creativity
       ↓
Google Gemini API
       ↓
Generated summary
       ↓
View statistics / Download summary
```

## 📂 Project Structure

```text
TextSummerizer/
├── .streamlit/
├── app.py
└── README.md
```

## 🚀 Getting Started

### Prerequisites

- Python 3 installed
- A Google Gemini API key
- Internet access for Gemini API requests

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

On Windows:

```powershell
.venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install streamlit google-genai
```

### 4. Configure the Gemini API key

For Linux/macOS:

```bash
export GEMINI_API_KEY="your_api_key_here"
```

For Windows PowerShell:

```powershell
$env:GEMINI_API_KEY="your_api_key_here"
```

You can also configure the key using Streamlit secrets.

> **Never commit your API key, `.env` files, or other secrets to GitHub.**

### 5. Run the application

```bash
streamlit run app.py
```

Streamlit will provide a local URL, normally:

```text
http://localhost:8501
```

## 🎯 Using the App

1. Paste the text you want to summarize.
2. Select a summary style.
3. Adjust the creativity slider.
4. Click **Summarise**.
5. Wait for Gemini to generate the summary.
6. Review the summary and usage statistics.
7. Click **Download summary** to save `summary.txt`.

## ⚙️ Input Limits

| Setting | Value |
|---|---:|
| Minimum input | 200 characters |
| Maximum input | 20,000 characters |
| Default creativity | 0.3 |
| Creativity range | 0.0 – 1.0 |

Input is validated before an API request is made.

## 🔐 Security

The Gemini API key should be supplied through an environment variable or Streamlit secrets instead of being hard-coded in the source code.

Example:

```bash
export GEMINI_API_KEY="your_api_key_here"
```

Never place a real API key in this README or commit it to the repository.

## 🧰 Tech Stack

| Technology | Purpose |
|---|---|
| **Python** | Application logic |
| **Streamlit** | Web interface |
| **Google Gen AI SDK** | Gemini API integration |
| **Google Gemini** | AI text summarization |

## 📌 Model

The Gemini model is configured in `app.py`. Update this README if the model configuration changes.

## ⚠️ Disclaimer

TextSummerizer uses generative AI. Generated summaries may omit, misunderstand, or incorrectly state details from the original text. **Always check the original source before relying on a summary for important information or decisions.**

## 🛠️ Troubleshooting

### `GEMINI_API_KEY is not set`

Check that the variable is available in the terminal where Streamlit is running:

```bash
echo $GEMINI_API_KEY
```

If you use Streamlit secrets, verify that the secret is configured correctly.

### The app does not start

Try:

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install streamlit google-genai
streamlit run app.py
```

### The Summarise button is disabled

Make sure your input contains at least **200 characters** and does not exceed **20,000 characters**.

## 🤝 Contributing

Contributions and improvements are welcome.

1. Fork the repository.
2. Create a feature branch.
3. Make your changes.
4. Test the application locally.
5. Commit your changes with a clear message.
6. Open a pull request.

## 📄 License

No license has currently been specified for this repository. Add an appropriate `LICENSE` file if you plan to distribute the project under an open-source license.

## 👨‍💻 Author

**Vyasan B Mathew**

- GitHub: https://github.com/vyasanbmathew2008
- Project: https://github.com/vyasanbmathew2008/TextSummerizer

---

⭐ If you find this project useful, consider starring the repository!
