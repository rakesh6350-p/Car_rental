# 🎥 YouTube Sentiment Analysis

A scalable **YouTube Sentiment Analysis** web application built using **Python**, **Streamlit**, **YouTube Data API v3**, and **Natural Language Processing (NLP)**. The application scrapes comments from any YouTube video, analyzes their sentiment using the **NLTK VADER** sentiment analyzer, and displays the results through an interactive dashboard.

---

## 📖 Overview

This project enables users to analyze the sentiment of comments on any YouTube video simply by providing its URL.

The application:

- Scrapes YouTube comments using the **YouTube Data API v3**
- Retrieves video and channel information
- Performs sentiment analysis using **NLTK VADER**
- Displays interactive visualizations using **Plotly**
- Allows downloading the scraped comments as a CSV file

---

## ✨ Features

### 📥 Data Scraping

- Fetches top-level comments from any YouTube video
- Saves comments into a downloadable CSV file
- Supports pagination to collect multiple comments

### 📺 Channel & Video Insights

Displays useful information including:

#### Channel Information

- Channel Logo
- Channel Name
- Subscriber Count
- Total Videos
- Channel Creation Date
- Channel Description

#### Video Statistics

- Video Title
- Views
- Likes
- Comment Count

---

### 😊 Sentiment Analysis

The application uses **NLTK VADER (Valence Aware Dictionary and sEntiment Reasoner)** to classify each comment into one of three categories:

- 🟢 Positive
- 🔴 Negative
- ⚪ Neutral

It also displays:

- Total Positive Comments
- Total Negative Comments
- Total Neutral Comments

---

### 📊 Interactive Visualizations

The dashboard provides:

- 📈 Bar Chart
- 🥧 Pie Chart

Built using:

- Plotly Express
- Plotly Graph Objects

---

### 🌐 Streamlit Web Interface

A clean, responsive, and interactive web interface developed entirely using **Streamlit**.

---

# 📂 Project Structure

```text
YouTube-Sentiment-Analysis/
│
├── app.py
├── Senti.py
├── YoutubeCommentScrapper.py
├── README.md
└── .streamlit/
    └── secrets.toml
```

### `app.py`

Main Streamlit application responsible for:

- User Interface
- Sidebar Inputs
- Displaying Metrics
- Rendering Charts
- Displaying Channel Information
- CSV Download

---

### `Senti.py`

Contains the NLP pipeline.

Responsibilities:

- Extract Video ID
- Sentiment Analysis
- VADER Polarity Scores
- Plotly Visualizations
- Data Processing

---

### `YoutubeCommentScrapper.py`

Handles integration with the **YouTube Data API v3**.

Responsibilities:

- Fetch Video Comments
- Fetch Video Metadata
- Fetch Channel Metadata
- Handle Pagination
- Export CSV

---

# 🛠 Technologies Used

- Python
- Streamlit
- YouTube Data API v3
- NLTK
- Pandas
- Plotly
- Google API Python Client
- Colorama

---

# 📦 Prerequisites

Install the required Python libraries:

```bash
pip install streamlit google-api-python-client nltk pandas plotly colorama
```

> **Note:** The application automatically downloads the **VADER Lexicon** during its first execution.

---

# 🚀 Installation

## 1. Clone the Repository

```bash
git clone https://github.com/your-username/YouTube-Sentiment-Analysis.git
cd YouTube-Sentiment-Analysis
```

---

## 2. Install Dependencies

```bash
pip install streamlit google-api-python-client nltk pandas plotly colorama
```

---

## 3. Configure API Key

Create a folder named:

```text
.streamlit
```

Inside the folder, create a file named:

```text
secrets.toml
```

Add your YouTube Data API key:

```toml
API_KEY = "YOUR_YOUTUBE_API_KEY"
```

> You must have a Google Cloud Platform project with the **YouTube Data API v3** enabled.

---

## 4. Run the Application

```bash
streamlit run app.py
```

---

# 📖 Usage

1. Launch the Streamlit application.
2. Open it in your browser.
3. Paste a YouTube video URL into the sidebar.
4. The application will automatically:
   - Fetch video comments
   - Retrieve channel information
   - Retrieve video statistics
   - Perform sentiment analysis
   - Display interactive charts
   - Generate a downloadable CSV file

---

# 📊 Dashboard Output

The application displays:

- 🎥 Video Preview
- 👤 Channel Details
- 📈 Video Statistics
- 😊 Sentiment Distribution
- 📊 Interactive Pie Chart
- 📉 Interactive Bar Chart
- 📥 Downloadable CSV File

---

# 🔄 Workflow

```text
User Input (YouTube URL)
            │
            ▼
Extract Video ID
            │
            ▼
YouTube Data API v3
            │
            ▼
Fetch Comments
            │
            ▼
Save Comments to CSV
            │
            ▼
NLTK VADER Sentiment Analysis
            │
            ▼
Positive │ Neutral │ Negative
            │
            ▼
Plotly Visualizations
            │
            ▼
Streamlit Dashboard
```

---

# 🚀 Future Enhancements

- 🌍 Multilingual sentiment analysis
- 😊 Emotion detection
- ☁️ Word cloud generation
- 📅 Comment filtering by date
- 🚫 Spam detection
- 🤖 Machine Learning based sentiment classification
- 👤 User authentication
- 📈 Historical sentiment tracking

---

# 🤝 Contributing

Contributions are welcome!

1. Fork the repository
2. Create a new feature branch

```bash
git checkout -b feature-name
```

3. Commit your changes

```bash
git commit -m "Add new feature"
```

4. Push your branch

```bash
git push origin feature-name
```

5. Open a Pull Request

---

# 📄 License

This project is licensed under the **MIT License**.

---

# 👨‍💻 Author

Developed using **Python**, **Streamlit**, **YouTube Data API v3**, **NLTK**, and **Plotly** for scalable YouTube comment sentiment analysis.
