# KNN Project Repository

This repository contains implementations of K-Nearest Neighbors (KNN) models for various problem statements.

## Projects

### 1. Job Recommendation System

**Directory:** `job_recommendation/`

**Problem Statement:**
Building a recommendation system that suggests suitable jobs based on a user's skills and experience.

**Approach:**
- **Data Preprocessing:**
    - Skills are cleaned and converted into a list format.
    - Experience years are normalized using `MinMaxScaler` to a range of [0, 1] to ensure they don't overpower the skill features during distance calculation.
- **Feature Engineering:**
    - **Skills:** Converted into numerical vectors using `CountVectorizer`.
    - **Experience:** Normalized numerical value.
    - **Combined Vector:** The skill vectors and normalized experience are stacked horizontally to form the final feature set for the KNN model.
- **Model:**
    - **Algorithm:** K-Nearest Neighbors (KNN).
    - **Metric:** Cosine Similarity (to measure the angle between vectors, suitable for high-dimensional text data).
    - **Output:** The model finds the 'k' nearest job profiles (neighbors) based on the user's input vector.
- **Hashing:** Company names are hashed for efficient storage and retrieval.

**Key Files:**
- `job_rec.py`: The main Python script implementing the logic.
- `job_dataset.csv`: The dataset containing job postings (Company Name, Skills, Experience, LPA).

**Dependencies:**
- pandas
- numpy
- scikit-learn
- nltk (if needed for further text processing)

**How to Run:**
1. Navigate to the `job_recommendation` directory.
2. Ensure you have the required dependencies installed (check `requirements.txt`).
3. Run the script:
   ```bash
   python job_rec.py
   ```