# Opinify


---

# Text Sentiment Analysis Web Application

This GitHub repository hosts a web application that utilizes Natural Language Processing (NLP) techniques to perform sentiment analysis on text data. The application is split into two main components: a Flask API for backend sentiment prediction and a Streamlit front end for user interaction.

## Flask API (Backend):

### 1. Text Preprocessing:
   - The input text undergoes NLP-based preprocessing, including:
     - Removal of non-alphabetic characters.
     - Conversion to lowercase.
     - Tokenization into individual words.
     - Stemming using the Porter Stemmer from NLTK.
     - Removal of stopwords using NLTK's English stopword list.

### 2. Model Loading:
   - A pre-trained XGBoost model, along with a scaler and CountVectorizer for text processing, is loaded during the Flask application startup.

### 3. Sentiment Analysis:
   - The core of the API involves predicting sentiment using the loaded XGBoost model. Both single text inputs and bulk predictions from CSV files are supported.

### 4. Graphical Visualization:
   - Matplotlib is employed to create a pie chart visualization showcasing the distribution of predicted sentiments in bulk predictions.

### 5. Flask Response:
   - The Flask API provides responses in various formats, including downloadable CSV files for bulk predictions and visualizations for sentiment distribution.

## Streamlit Application (Frontend):

### 1. Streamlit Setup:
   - Streamlit is used to create an interactive web application with a user-friendly interface.

### 2. File Uploader and Text Input:
   - Users can upload CSV files for bulk predictions or enter text for single sentence predictions. This involves interacting with the Flask API for sentiment analysis.

### 3. Prediction and Download:
   - When users click the "Predict" button, the Streamlit application sends requests to the Flask API for sentiment prediction.
   - For bulk predictions, a CSV file is returned and presented for download.
   - For single predictions, the response is displayed in the Streamlit interface.

### 4. GitHub Structure:
   - The repository is organized with separate directories for Flask backend and Streamlit frontend.
   - Pre-trained models, scalers, and other resources are stored in a "Models" directory.
   - Code for Flask routes, sentiment analysis functions, and Streamlit UI elements are well-structured.

## Summary:

This project demonstrates the integration of NLP techniques for sentiment analysis in a web application. The Flask API leverages machine learning models, while Streamlit provides an intuitive user interface. The combination of Flask and Streamlit facilitates seamless communication, making sentiment analysis accessible to users through a user-friendly and visually appealing web interface.

---

