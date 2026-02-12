# 🎬 Kannada Movie Recommender System with Sentiment Analysis

A Content-Based Movie Recommendation System built using Flask that recommends movies based on similarity and performs sentiment analysis on IMDb reviews.

---

## 🚀 Project Overview

This application recommends movies similar to the one selected by the user using **Cosine Similarity** and analyzes user reviews using a pre-trained NLP model.

The system fetches movie details from TMDB API and performs web scraping to extract IMDb reviews for sentiment classification.

---

## 🛠 Tech Stack

### Backend

* Python
* Flask
* Scikit-learn
* NLTK

### Frontend

* HTML
* CSS
* JavaScript
* AJAX

### Data & APIs

* TMDB API (for movie details)
* IMDb (for review scraping)

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

* Movie features are combined into a single text column (`comb`)
* CountVectorizer converts text into numerical vectors
* Cosine similarity computes similarity score
* Top 10 most similar movies are returned

### 2️⃣ Sentiment Analysis

* IMDb reviews are scraped
* Reviews are transformed using saved vectorizer
* Pre-trained ML model predicts sentiment
* Reviews are classified as **Good** or **Bad**

---

## 🧠 Similarity Formula

Cosine Similarity measures the cosine of the angle between two vectors:

* Value ranges between 0 and 1
* Higher value → More similar movies

---

## ▶️ How to Run Locally

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

Open browser and visit:

```
http://127.0.0.1:5000/
```

---

## 🌐 Deployment

This project can be deployed on:

* Hugging Face Spaces (Docker)
* Render
* Railway
* Heroku (legacy)

---

## 📈 Features

* Content-based recommendation engine
* IMDb review scraping
* Sentiment classification
* Dynamic AJAX UI
* TMDB API integration

---

## 📌 Future Improvements

* Add multilingual support
* Replace scraping with official review API
* Improve recommendation quality using TF-IDF
* Add user authentication

---

## 👩‍💻 Author

Developed by Deepu

---

⭐ If you found this project useful, consider giving it a star!
