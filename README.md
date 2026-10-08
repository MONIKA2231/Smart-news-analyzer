# 📰 SmartNews Analyzer - Multi-Feature NLP Dashboard

An impressive beginner-friendly NLP project that classifies news articles by category, analyzes sentiment, extracts key entities, and generates summaries - all in a beautiful web interface.

## 🌟 Why This Project Stands Out

- **Multiple NLP Techniques**: Classification, Sentiment Analysis, Named Entity Recognition, Summarization
- **Real-world Application**: Works with live news data
- **Professional Dashboard**: Interactive web interface with visualizations
- **Modern Stack**: Uses transformers, not just basic models
- **Portfolio Ready**: Impressive for interviews and GitHub

## 🎯 Features

1. **Article Classification** - Categorizes news into: Politics, Technology, Sports, Entertainment, Business, Health
2. **Sentiment Analysis** - Detects positive, negative, or neutral tone
3. **Named Entity Recognition** - Extracts people, organizations, locations
4. **Auto Summarization** - Generates concise article summaries
5. **Trend Analysis** - Visualizes topics over time
6. **Web Dashboard** - Beautiful interface to interact with results

## 📁 Project Structure

```
smartnews-analyzer/
├── app.py                 # Main Flask web application
├── nlp_pipeline.py        # Core NLP processing logic
├── data_collector.py      # News data fetching
├── requirements.txt       # Python dependencies
├── models/               # Saved models (auto-created)
├── templates/            # HTML templates
│   └── index.html
├── static/               # CSS, JS, images
│   ├── css/
│   └── js/
└── data/                 # Sample datasets
    └── sample_news.csv
```

## 🚀 Quick Start

### Prerequisites
- Python 3.8+
- 2GB free disk space (for models)

### Installation

```bash
# Clone or download the project
cd smartnews-analyzer

# Create virtual environment (recommended)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Download required models (first time only)
python -c "from nlp_pipeline import download_models; download_models()"
```

### Run the Application

```bash
python app.py
```

Visit: `http://localhost:5000`

## 📊 How It Works

### 1. Data Collection
- Fetches news from NewsAPI (free tier: 100 requests/day)
- Falls back to sample dataset for learning
- Supports custom text input

### 2. NLP Pipeline
- **Preprocessing**: Tokenization, cleaning, lemmatization
- **Classification**: Fine-tuned DistilBERT model
- **Sentiment**: VADER + Transformer ensemble
- **NER**: spaCy's en_core_web_sm model
- **Summarization**: Extractive (TF-IDF) + Abstractive (T5)

### 3. Visualization
- Category distribution charts
- Sentiment timeline
- Entity word clouds
- Topic clustering (t-SNE)

## 🎓 Learning Path

This project teaches you:

1. **Text Preprocessing** - Cleaning, tokenization, normalization
2. **Feature Engineering** - TF-IDF, word embeddings
3. **Model Training** - Fine-tuning pre-trained models
4. **Model Evaluation** - Accuracy, F1-score, confusion matrix
5. **API Integration** - NewsAPI, RESTful design
6. **Web Development** - Flask, HTML/CSS/JS basics
7. **Data Visualization** - Plotly, charts, dashboards

## 📈 Extensions & Improvements

Once comfortable, try:

- [ ] Add more news sources (BBC, Guardian APIs)
- [ ] Implement article recommendation system
- [ ] Add fake news detection
- [ ] Multi-language support
- [ ] Real-time streaming analysis
- [ ] Deploy to Heroku/AWS
- [ ] Add user authentication
- [ ] Implement search functionality

## 🛠️ Technologies Used

- **NLP**: transformers, spaCy, NLTK, scikit-learn
- **Web**: Flask, HTML5, Bootstrap, Plotly.js
- **Data**: pandas, numpy
- **APIs**: NewsAPI, HuggingFace

## 📝 Documentation

Each file contains detailed comments explaining:
- What the code does
- Why we use specific techniques
- How to modify/extend it

## 🤝 Contributing Ideas

- Use different datasets (Reddit, Twitter)
- Add emotion detection (joy, anger, fear)
- Implement bias detection
- Create Chrome extension version

## 📄 License

MIT License - Free to use for learning and portfolio

## 🆘 Troubleshooting

**Models taking too long?**
- Use smaller models (see config options)

**API limit reached?**
- Use sample dataset mode

**Memory errors?**
- Reduce batch size in config

---

Built with ❤️ for learning NLP
# 1. Activate the virtual environment where we installed the dependencies
.\.venv\Scripts\Activate.ps1

# 2. Set the encoding to UTF-8 (this prevents errors from the emojis in the print statements)
$env:PYTHONIOENCODING="utf-8"

# 3. Start the application
python app.py