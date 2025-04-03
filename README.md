# Google-Playstore-Reviews-Analysis
 Google Playstore Analysis & Sentiment Dashboard

This repository contains a detailed end-to-end data analysis project on the Google Play Store app data along with an interactive web-based dashboard.
The project covers everything from Data Cleaning, EDA, Sentiment Analysis, and Data Visualization using Python libraries like Plotly, Pandas, NLTK, and Sklearn.

**Project Objective**

The main objective of this project is to:
	•	Clean and preprocess the Google Playstore Dataset
	•	Handle missing values, duplicates & irrelevant data
	•	Transform and normalize the data
	•	Analyze sentiment of user reviews using NLP (Sentiment Analysis)
	•	Generate interactive visualizations using Plotly
	•	Build a Web-Based Interactive Dashboard for presenting key insights
**Project Structure**
 📦 Google-Playstore-Analysis
 ┣ 📄 Google playstore analysis.ipynb
 ┣ 📄 README.md
 ┣ 📂 data
 ┃ ┣ 📄 Play Store Data.csv
 ┃ ┗ 📄 User Reviews.csv
 ┣ 📂 graph
 ┃ ┗ 📄 (All interactive HTML graphs)
 ┗ 📄 web page.html (Interactive Dashboard)

**Technologies Used**
	•	Python
	•	Jupyter Notebook
	•	Pandas & NumPy
	•	NLTK (VADER Sentiment Analysis)
	•	Scikit-learn
	•	Plotly Express
	•	HTML & CSS (for dashboard)
	•	Webbrowser (Python library)
 
**Key Components**

1. Data Cleaning & Preprocessing
	•	Missing Value Handling: Used .dropna() and .fillna() methods.
	•	Duplicate Handling: Used .duplicated() and .drop_duplicates().
	•	Outlier Removal: Filtered ratings > 5.
	•	Type Conversion: Converted data types for columns like Reviews, Installs, Price, Size.
	•	Data Normalization: Converted app sizes into MB and applied log transformation on Installs and Reviews.

2. Sentiment Analysis
	•	Performed Sentiment Analysis on user reviews using VADER Sentiment Analyzer.
	•	Derived a Sentiment Score for every review.
	•	Categorized sentiments as Positive, Negative, Neutral.

3. Feature Engineering
	•	Added new metrics like:
	•	Revenue = Price × Installs
	•	Rating Group (Top Rated, Above Average, Average, Below Average)
	•	Extracted Year from the Last Updated column.

4. Data Visualization & Dashboard
	•	Created Interactive Graphs using Plotly Express:
	•	Top Categories
	•	Free vs Paid App Distribution
	•	Rating Distribution
	•	Sentiment Score Distribution
	•	Installs by Category
	•	Updates Over Years
	•	Revenue by Category
	•	Most Common Genres
	•	Last Update Impact on Ratings
	•	Ratings Comparison (Paid vs Free)
	•	All graphs were saved as HTML Files.
	•	A Web-based Dashboard was designed using HTML & CSS with interactive plots and one-line insights.

**Key Insights**
	•	Free apps dominate the Play Store.
	•	Categories like Tools, Entertainment, and Productivity are the most common.
	•	Positive Sentiments are dominant but mixed reviews exist.
	•	Paid apps generally have higher ratings than free apps.
	•	App updates have been increasing over the years.
	•	Genres like Action & Casual games are highly preferred.

**Dashboard Preview**
![image](https://github.com/user-attachments/assets/71d66adb-1922-4964-9772-7c43e3534a27)
![image](https://github.com/user-attachments/assets/ebb5cf18-a493-4298-b11f-12e2cd368169)

**How to Run**
1.	Clone the repository
 git clone [https://github.com/Prateek1033/Google-Playstore-Analysis.git](https://github.com/Prateek1033/Google-Reviews-Analysis/tree/main)
2.	Install dependencies
 pip install pandas numpy matplotlib seaborn plotly nltk scikit-learn
3.	Download NLTK VADER Lexicon
import nltk
nltk.download('vader_lexicon')
4.	Run Jupyter Notebook
jupyter notebook "Google playstore analysis.ipynb"





 
