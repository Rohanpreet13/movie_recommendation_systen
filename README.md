# **Movie Recommendation System**

A **Movie Recommendation System** built using Python and Machine Learning techniques. The system recommends the **top 10 movies** based on the movie selected by the user.

The project uses **text-based features** from movie metadata and calculates the similarity between movies using **TF-IDF Vectorization** and **Cosine Similarity**.

## **Project Overview**

The Movie Recommendation System takes a movie name as input from the user and finds movies that are most similar to the selected movie.

The recommendation process is based on important textual features such as:

-   **Genres**
-   **Keywords**
-   **Tagline**
-   **Cast**
-   **Director**

The system combines these features to create a textual representation of each movie and then compares the movies to determine which ones are most similar.

Finally, the system displays the **Top 10 recommended movies**.

## **Features**

-   Takes a movie name as input from the user
-   Uses difflib to find the closest matching movie name
-   Combines multiple textual movie features
-   Converts text into numerical vectors using TfidfVectorizer
-   Calculates similarity using the **Cosine Similarity** algorithm
-   Returns the **Top 10 most similar/recommended movies**
-   Built using Python and popular Machine Learning libraries

## **Dataset**

The dataset contains multiple columns containing information about movies.

Although the dataset contains many columns, the following features are used for building the recommendation system:

genres

keywords

tagline

cast

director

These features provide useful information about the content, people involved, and characteristics of each movie.

## **Technologies & Libraries Used**

|**Technology | Library**|
|:---|---:|
|Python|Programming language|
|Pandas|Data manipulation and preprocessing|
|NumPy|Numerical operations|

difflib

Finding the closest matching movie name

Scikit-learn

Machine learning utilities

TfidfVectorizer

Converting text into numerical vectors

Cosine Similarity

Measuring similarity between movies

## **How the Recommendation System Works**

The system follows these main steps:

**1. Load the Dataset**

The movie dataset is loaded using **Pandas**.

**2. Select Relevant Features**

Only the following features are considered for recommendation:

features = ['genres', 'keywords', 'tagline', 'cast', 'director']

**3. Handle Missing Values**

Missing values in the selected features are handled so that they do not cause problems during text processing.

**4. Combine Textual Features**

The selected movie features are combined into a single text representation.

For example:

Genres + Keywords + Tagline + Cast + Director

This combined information represents the characteristics of a movie.

**5. Convert Text into Numerical Data**

Since machine learning algorithms cannot directly work with raw text, **TF-IDF Vectorization** is used.

from sklearn.feature_extraction.text import TfidfVectorizer

vectorizer = TfidfVectorizer()

feature_vectors = vectorizer.fit_transform(combined_features)

TF-IDF converts the textual information into numerical vectors while giving importance to meaningful words.

**6. Calculate Similarity**

The similarity between movies is calculated using **Cosine Similarity**.

from sklearn.metrics.pairwise import cosine_similarity

similarity = cosine_similarity(feature_vectors)

The resulting similarity score represents how similar two movies are.

A higher similarity score means the movies have more similar characteristics.

**7. Take Movie Name as Input**

The user enters the name of a movie.

For example:

Enter your favourite movie name: Avatar

**8. Find the Closest Movie Match**

The difflib library is used to find the closest matching movie name from the dataset.

This is useful when the user enters a movie name with a small spelling mistake or slightly different wording.

import difflib

**9. Generate Recommendations**

After finding the corresponding movie, the system retrieves its similarity scores and sorts the movies according to their similarity.

The **Top 10 most similar movies** are then displayed as recommendations.

## **Project Workflow**

Movie Dataset

↓

Select Movie Features

↓

genres + keywords + tagline

  +cast + director

↓

Combine Textual Features

↓

TF-IDF Vectorization

↓

Feature Vector Creation

↓

Cosine Similarity Matrix

↓

User Enters Movie Name

↓

difflib Finds Best Match

↓

Compare Similarity Scores

↓

Sort Movies by Similarity

↓

Top 10 Recommendations

## **Example**

### **Input**

Enter your favourite movie name: Iron Man

### **Output**

Movies suggested for you:

1. Iron Man 2

2. The Avengers

3. Iron Man 3

4. Avengers: Age of Ultron

5. Captain America: Civil War

6. The Incredible Hulk

7. Thor

8. Captain America: The First Avenger

9. Avengers: Infinity War

10. Avengers: Endgame

_The actual recommendations depend on the dataset and calculated similarity scores._

## **Project Structure**

A possible project structure is:

Movie-Recommendation-System/

│

├── movie_recommendation_system.ipynb

├── movies.csv

├── README.md

└── requirements.txt

## **Installation**

### **1. Clone the Repository**

git clone https://github.com/your-username/movie-recommendation-system.git

### **2. Navigate to the Project Directory**

cd movie-recommendation-system

### **3. Install Required Libraries**

pip install pandas numpy scikit-learn

The project primarily requires:

pandas

numpy

scikit-learn

difflib is part of Python's standard library, so it does not need to be installed separately.

## **How to Run**

If the project is provided as a Jupyter Notebook:

jupyter notebook

Then open:

movie_recommendation_system.ipynb

Run the cells in sequence and enter the name of a movie when prompted.

## **Algorithms Used**

**TF-IDF Vectorization**

**TF-IDF (Term Frequency–Inverse Document Frequency)** converts textual movie information into numerical vectors.

It helps determine which words are important in the movie descriptions and features.

**Cosine Similarity**

Cosine Similarity measures the similarity between two numerical vectors.

The similarity score generally ranges from:

0 → Completely different

1 → Highly similar

The movies with the highest similarity scores are selected as recommendations.

## **Objective**

The main objective of this project is to build a simple and effective **content-based movie recommendation system** that recommends movies based on their textual characteristics.

The project demonstrates the practical application of:

-   Natural Language Processing
-   Feature Extraction
-   Text Vectorization
-   Similarity Measurement
-   Recommendation Systems
-   Python Programming

## **Future Improvements**

Some possible improvements include:

-   Add a graphical or web-based user interface
-   Deploy the recommendation system using Streamlit or Flask
-   Add movie posters and additional movie information
-   Include ratings and user reviews
-   Improve recommendation quality using more advanced recommendation algorithms
-   Add collaborative filtering
-   Combine content-based and collaborative filtering into a hybrid recommendation system
-   Allow users to select multiple favourite movies

## **Author**

**Rohanpreet Arora**

If you found this project useful or interesting, feel free to ⭐ the repository.

## **License**

This project is created for **educational and learning purposes**.Welcome to StackEdit!

Hi! I'm your first Markdown file in **StackEdit**. If you want to learn about StackEdit, you can read me. If you want to play with Markdown, you can edit me. Once you have finished with me, you can create new files by opening the **file explorer** on the left corner of the navigation bar.


