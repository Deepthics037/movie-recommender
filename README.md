# 🎬 Content-Based Movie Recommender System with Sentiment Analysis using AJAX

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Framework](https://img.shields.io/badge/Framework-Flask-red)
![Frontend](https://img.shields.io/badge/Frontend-HTML/CSS/JS-green)
![ML](https://img.shields.io/badge/ML-Scikit--Learn-orange)

---

## 📌 Project Overview

This is a **Content-Based Movie Recommendation System** built using Flask that recommends movies similar to the one selected by the user and performs **sentiment analysis** on IMDb reviews.

The application fetches movie details (title, genre, runtime, rating, poster, etc.) using the TMDB API. It then uses the IMDb ID to scrape user reviews and classify them as **Positive (Good)** or **Negative (Bad)** using a trained NLP model.

---

## 🚀 Features

* 🎯 Content-based movie recommendation engine
* 🤖 Sentiment analysis on IMDb reviews
* 🔍 Auto-suggestion search functionality
* ⚡ AJAX-based dynamic frontend
* 🌐 TMDB API integration
* 🧠 Cosine similarity-based recommendation logic

---

## 🛠️ Tech Stack

### Backend

* Python
* Flask
* Scikit-learn
* NLTK
* BeautifulSoup

### Frontend

* HTML
* CSS
* JavaScript
* AJAX

### APIs & Data Sources

* TMDB API (Movie details)
* IMDb (Review scraping)

---

## 📂 Project Structure

```
.
├── main.py
├── requirements.txt
├── main_data.csv
├── nlp_model.pkl
├── tranform.pkl
├── templates/
├── static/
└── reviews.txt
```

---

## ⚙️ How It Works

### 1️⃣ Content-Based Recommendation

* Important movie features are combined into a single text column (`comb`).
* `CountVectorizer` converts text data into numerical vectors.
* `Cosine Similarity` calculates similarity between movies.
* Top 10 most similar movies are returned to the user.

### 2️⃣ Sentiment Analysis

* IMDb reviews are scraped using BeautifulSoup.
* Reviews are transformed using a saved vectorizer.
* A trained ML model predicts sentiment.
* Reviews are classified as **Good** or **Bad**.

---

## 📊 Similarity Score

The system uses **Cosine Similarity**, which measures the cosine of the angle between two vectors in multi-dimensional space.

* Score ranges from 0 to 1
* Closer to 1 → More similar
* Smaller angle → Higher similarity

This method ensures that similarity is based on content features rather than movie popularity.

---

## 🔑 How to Get TMDB API Key

1. Create an account on TMDB.
2. Go to Account Settings → API.
3. Apply for an API key.
4. Copy your API key once approved.

Replace `YOUR_API_KEY` inside `static/recommend.js` with your actual key.

---

## ▶️ How to Run the Project Locally

### 1️⃣ Clone the Repository

```
git clone https://github.com/YOUR_USERNAME/movie-recommender.git
cd movie-recommender
```

### 2️⃣ Create Virtual Environment

```
python -m venv venv
venv\Scripts\activate
```

### 3️⃣ Install Dependencies

```
pip install -r requirements.txt
```

### 4️⃣ Run Application

```
python main.py
```

Open your browser and visit:

```
http://127.0.0.1:5000/
```

---

## 🏗️ Architecture

User Input → TMDB API → Recommendation Engine (CountVectorizer + Cosine Similarity) → IMDb Review Scraping → Sentiment Analysis Model → Display Results

---

## 📈 Future Improvements

* Add multilingual movie support
* Replace scraping with official review APIs
* Use TF-IDF for improved similarity
* Add user authentication system
* Deploy with Docker for production use


