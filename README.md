# 💼 JobFinder: Specialized Search Engine for Job Listings

## 📌 Project Overview
JobFinder is a custom-built, specialized search engine engineered from scratch to retrieve, process, and rank employment listings. Developed to meet strict academic constraints, this project entirely avoids pre-built indexing engines like Elasticsearch or Whoosh. Instead, it relies on fundamental Information Retrieval (IR) principles, utilizing a custom-built Inverted Index and raw Boolean/TF-IDF logic. 

The domain of focus is **Job Postings**, utilizing a comprehensive dataset of real-world LinkedIn job descriptions to demonstrate how unstructured text can be transformed into a highly queryable, ranked database.

## ✨ Core Features
* **Custom Inverted Index:** A purely Python-based dictionary structure mapping individual terms to specific Document IDs and their term frequencies.
* **Advanced Preprocessing Pipeline:** Integrates NLTK to handle tokenization, stop-word removal, lowercasing, and punctuation stripping via regex.
* **Boolean Query Logic:** Seamlessly processes single-word and complex multi-word queries using Set Theory (`AND` intersections / `OR` unions).
* **Dynamic TF-IDF Ranking:** Calculates relevance scores at runtime to ensure documents with the highest contextual keyword density are ranked first.
* **Modern Web Interface:** A fully responsive, Google-inspired GUI built with Streamlit, featuring highlighted search keywords and clean snippet generation.

## 📸 Application Screenshots
* <img width="993" height="383" alt="image" src="https://github.com/user-attachments/assets/c9c57bfa-822e-4b06-8148-ba604861fed6" />

* <img width="1013" height="431" alt="image" src="https://github.com/user-attachments/assets/4c87e58f-d404-444f-8c3f-8a833423dfb3" />

* <img width="1012" height="412" alt="image" src="https://github.com/user-attachments/assets/ef78ffca-df67-4893-9bc9-478ffc648e0d" />


## 🛠️ Technology Stack & Libraries
* **Language:** Python
* **Data Manipulation:** `pandas`, `numpy`
* **Natural Language Processing (NLP):** `nltk` (punkt, stopwords), `re` (Regular Expressions)
* **Frontend UI Framework:** `streamlit`
* **Model Serialization:** `joblib`
* **Deployment Tunnel:** `pinggy` (for Google Colab port forwarding)

## 📂 Repository Structure
* `JobFinder_Notebook.ipynb`: The main Google Colab environment containing the data extraction, preprocessing, and indexing logic.
* `app.py`: The Streamlit frontend application.
* `search_engine_data.pkl`: The serialized inverted index (generated upon running the notebook).
* `README.md`: Project documentation and setup instructions.

## 🚀 How to Run the Project
1. Open `JobFinder_Notebook.ipynb` in Google Colab.
2. **Build the Engine:** Run Cells 1 through 8. This downloads the dataset, cleans the text, builds the inverted index, and tests the backend logic.
3. **Save Data:** Run Cell 9A to serialize the index using `joblib`.
4. **Generate Frontend:** Run Cell 9B to write the `app.py` script.
5. **Launch App:** Run Cell 9C. Wait roughly 15 seconds for the Pinggy tunnel to initialize, then click the generated `https://*.pinggy.link` URL to open the GUI in a new tab. No authentication is required.
