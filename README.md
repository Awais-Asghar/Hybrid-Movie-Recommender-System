<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/9520bf4d-f2e2-4eb3-9213-023c66f8bf24" /># Hybrid Movie Recommender System
![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Recommender%20Systems-brightgreen)
![TMDB](https://img.shields.io/badge/Data-TMDB%20API-orange)
![MovieLens](https://img.shields.io/badge/Data-MovieLens-red)
![Status](https://img.shields.io/badge/Status-Completed-success)
![License](https://img.shields.io/badge/License-Academic-lightgrey)

---

## Project Overview

This project implements a **Movie Recommender System** using **Content-Based Filtering**, **Collaborative Filtering**, and a **Hybrid Recommendation approach**. The system focuses on **high-rated movies released between 2015 and 2025** and leverages both movie metadata and user–movie interaction data to generate accurate and personalized recommendations.

---

## Objectives

- Build a **content-based recommender** using movie metadata  
- Build a **collaborative filtering model** using user ratings  
- Combine both approaches into a **hybrid recommender system**  
- Evaluate recommendation quality using ranking-based metrics  

---

## Dataset Description

### Data Sources
- **TMDB API** – Movie metadata (titles, overview, genres, cast, keywords)
- **MovieLens Dataset** – User–movie rating interactions
- **IMDb (Scraping)** – Scraping pipeline implemented (reviews optional)

### Filtering Criteria
- Release years: **2015–2025**
- Minimum rating: **6.0**
- Minimum vote count: **50**

### Generated Files
| File Name | Description |
|----------|------------|
| `movies_2015_2025.csv` | Raw movie metadata from TMDB |
| `movies_tmdb_enriched.csv` | Enriched metadata (genres, cast, keywords) |
| `ratings_for_cf.csv` | User–movie ratings for collaborative filtering |
| `movies_master.csv` | Final dataset with combined textual features |

---

## Methodology

### 1. Content-Based Filtering
- Feature engineering using movie **overview, genres, keywords, cast**
- Unified text feature: `combined_text`
- **TF-IDF vectorization**
- **Cosine similarity** for movie-to-movie recommendations

### 2. Collaborative Filtering
- User–item interaction matrix from MovieLens
- **Matrix factorization (SVD)** using Surprise library
- Personalized rating prediction

### 3. Hybrid Recommendation
- Weighted fusion of content-based and collaborative scores  
- Fusion parameter **α** controls contribution of each model  

```

Final Score = α × Content Score + (1 − α) × Collaborative Score

```

---

## Evaluation Metrics

The system was evaluated using ranking-based and prediction metrics:

- **HitRate@5**
- **HitRate@10**
- **MRR@5**
- **RMSE** (for collaborative filtering)

### Performance Highlights

- **HitRate@10 ≈ 0.95**
- **HitRate@5 ≈ 0.92**
- **MRR@5 ≈ 0.90**
- Best performance achieved at **α ≈ 0.7–0.9**
- Hybrid model significantly outperformed collaborative-only (Surprise) baseline

---

## Tools and Technologies

- **Programming Language:** Python  
- **Libraries:** Pandas, NumPy, Scikit-learn, Surprise  
- **Data Sources:** TMDB API, MovieLens  
- **Web Scraping:** BeautifulSoup  
- **Visualization:** Matplotlib  
- **Environment:** Kaggle, Jupyter Notebook  
- **Version Control:** Git, GitHub  

---

## Ethical Considerations

- Only **public and academic datasets** were used  
- Ethical and rate-limited web scraping  
- No personal or sensitive user data collected  
- Project developed strictly for **educational purposes**

---

## Future Work

- Deep learning–based recommenders (Neural CF, embeddings)
- Real-time user feedback integration
- Web or mobile application deployment
- Larger and multilingual datasets

---

## Authors

- **Awais Asghar**
- **Ahmad Hussain**
- **M. Hammad Sarwar**

---

## ⭐ Acknowledgments

- TMDB for providing the movie metadata API  
- GroupLens Research for the MovieLens dataset  

---

⭐ If you find this project useful, feel free to the repository ⭐
