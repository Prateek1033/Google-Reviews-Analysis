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


**Tasks** These FIVE Tasks has been given by the client(NULL CLASS) to complete 

1. Visualize the sentiment distribution (positive, neutral, negative) of user reviews using a stacked bar chart, segmented by rating groups (e.g., 1-2 stars, 3-4 stars, 4-5 stars). Include only apps with more than 1,000 reviews and group by the top 5 categories.

2. Create a dual-axis chart comparing the average installs and revenue for free vs. paid apps within the top 3 app categories. Apply filters to exclude apps with fewer than 10,000 installs and revenue below $10,000 and android version should be more than 4.0 as well as size should be more than 15M and content rating should be Everyone and app name should not have more than 30 characters including space and special character .this graph should work only between 1 PM IST to 2 PM IST apart from that time we should not show this graph in dashboard itself.

3. Create an interactive Choropleth map using Plotly to visualize global installs by Category. Apply filters to show data for only the top 5 app categories and highlight category where the number of installs exceeds 1 million. The app category should not start with the characters “A,” “C,” “G,” or “S.” This graph should work only between 6 PM IST and 8 PM IST; apart from that time, we should not show it in the dashboard itself.

4. Create a violin plot to visualize the distribution of ratings for each app category, but only include categories with more than 50 apps and app name should contain letter “C” and exclude apps with fewer than 10 reviews and rating should be less 4.0. this graph should work only between 4 PM IST to 6 PM IST apart from that time we should not show this graph in dashboard itself.

5. Plot a time series line chart to show the trend of total installs over time, segmented by app category. Highlight periods of significant growth by shading the areas under the curve where the increase in installs exceeds 20% month-over-month and app name should not starts with x, y ,z and app category should start with letter " E " or " C " or " B " and reviews should be more than 500 as well as this graph should work only between 6 PM IST to 9 PM IST apart from that time we should not show this graph in dashboard itself.

**Task 1**
Graph Type: Stacked Bar Chart (Sentiment × Rating Group × Category)

**Description:**
This visualization analyzes user sentiment (Positive, Neutral, Negative) derived from app reviews and displays it using a stacked bar chart.
Each bar represents a rating group (e.g., 1-2 stars, 3-4 stars, 4-5 stars), and is segmented by sentiment types.

**Filters & Logic Applied:**
	
 •	Only apps with more than 1,000 reviews were included to ensure significant sentiment volume.
	
 •	Data is grouped by the Top 5 app categories based on app count.
	
 •	Reviews are preprocessed to classify into Positive, Negative, or Neutral, using NLTK’s VADER Sentiment Analyzer.

**Ratings were binned into three intuitive ranges:**
	
 •	1.0–2.9 stars: Low Rated
	
 •	3.0–3.9 stars: Average Rated
	
 •	4.0–5.0 stars: Top Rated

**Insight Gained:**
This chart helps correlate app ratings with user sentiment, showing how highly rated apps generally receive more positive feedback, while lower-rated apps tend to accumulate more negative or neutral sentiment.

**OUTPUT OF TASK 1**
<img width="1440" alt="Screenshot 2025-04-20 at 5 38 55 PM" src="https://github.com/user-attachments/assets/1f4f2def-1f02-4be4-860f-623d523454e1" />


**Task 2**
Time Window for this graph: Visible only between 1:00 PM – 2:00 PM IST on Dashboard

Graph Type: Dual-axis bar chart

**Description:**
This visualization provides a comparative overview of Free vs Paid apps in terms of their average installs (on primary Y-axis) and average revenue (on secondary Y-axis) across the top 3 app categories.

**It leverages a dual-axis chart, where:**

•	Bars represent average installs for Free and Paid apps

•	Lines represent average revenue for the same groups

**Filters & Criteria Applied:**
	
 •	Apps must belong to the top 3 most frequent categories
	
 •	Minimum installs: ≥ 10,000
	
 •	Minimum revenue: ≥ $10,000
	
 •	Size: > 15 MB
	
 •	Android version: > 4.0
	
 •	Content Rating: Everyone
	
 •	App name character limit: ≤ 30 characters (including spaces/symbols)


This graph is only rendered if the current system time is between 1 PM and 2 PM IST, ensuring contextual delivery of insights.

**Insight Gained:**
	
 •	Free apps generally have higher install counts but lower revenue per app.
	
 •	Paid apps, while having fewer installs, generate significantly higher revenue due to direct purchase models.
	
 •	Categories like Productivity, Tools, and Education often highlight these contrasts more clearly.

**OUTPUT OF TASK 2**
<img width="1440" alt="Screenshot 2025-04-21 at 1 43 26 PM" src="https://github.com/user-attachments/assets/4768f5bd-3df4-4674-a14d-3ddacd05b2c9" />


**Task 3**
Time Window for this graph: Visible only between 6 PM – 8 PM IST on Dashboard

Graph Type: Choropleth Map (Geo Visualization)

Tool Used: Plotly Express

**Description:**
This task features an interactive Choropleth map to represent the global distribution of app installs by category, offering a geospatial perspective of market penetration. Since direct geolocation was unavailable in the dataset, this visualization relies on category-based aggregation with random mock country mapping, ideal for conceptual display in dashboards or POCs.

**Filters & Custom Conditions Applied:**
	
 •	Only includes top 5 app categories based on total installs.
	
 •	Highlights categories where total installs > 1 million.
	
 •	Excludes all categories that begin with the letters: A, C, G, or S (e.g., ART_AND_DESIGN, COMMUNICATION, etc.)
	
 •	This chart is time-sensitive and only appears in the dashboard between 6 PM to 8 PM IST to encourage contextual engagement.

**Insight Gained:**
	
 •	Categories such as Education, Business, and Entertainment showed widespread install footprints and crossed the 1 million installs threshold in multiple regions.
	
 •	This type of visualization helps stakeholders identify popular app categories by geographical spread and prepare region-specific marketing strategies.
 
**OUTPUT OF TASK 3**
<img width="1440" alt="Screenshot 2025-04-20 at 6 05 37 PM" src="https://github.com/user-attachments/assets/0fcf295b-bc9d-4f73-8797-443bdf82f57f" />


**Task 4**
Time Window for this graph: Visible only between 4 PM – 6 PM IST on Dashboard

Graph Type: Violin Plot

Tool Used: Plotly Express

**Description:**

This task uses a violin plot to explore the distribution of user ratings across app categories. The violin plot is ideal for visualizing density, spread, and central tendencies of ratings for each qualifying category. It shows both distribution shape and outliers, making it easier to understand variability in app feedback.

**Filters & Custom Conditions Applied:**
	
 •	Only includes categories that have more than 50 apps.
	
 •	App names must contain the letter “C” (case-insensitive).
	
 •	Apps with fewer than 10 reviews are excluded.
	
 •	Only includes apps with a rating less than 4.0.
	
 •	This graph is conditionally rendered and appears in the dashboard only between 4 PM and 6 PM IST.

**Insight Gained:**
	
 •	The violin plot highlights how lower-rated apps (rating < 4.0) are distributed across different categories.
	
 •	Categories such as Communication and Tools had wider distributions, indicating mixed user feedback and potentially unstable experiences.
	
 •	Compact violins (like those in the Education or Books categories) suggest more consistency in user ratings, even among lower-rated apps.

 **OUTPUT OF TASK 4**
<img width="1440" alt="Screenshot 2025-04-20 at 5 40 01 PM" src="https://github.com/user-attachments/assets/67b68a7a-664d-4347-a435-64fad5bd71e8" />

**Task 5**
Time Window for this graph: Visible only between 6 PM – 9 PM IST on Dashboard

Graph Type: Time Series Line Chart with Shaded Growth Regions

Tool Used: Plotly Graph Objects

**Description:**
This task generates an interactive time series chart to track how total app installs have evolved over time, segmented by app categories. The key enhancement is the highlighting of time periods where month-over-month (MoM) growth in installs exceeds 20%, providing a visual indicator of explosive user adoption or successful promotional periods.

**Filters & Custom Conditions Applied:**
	
 •	Only includes apps where:
	
 •	App name does NOT start with X, Y, or Z.
	
 •	App category starts with E, C, or B (e.g., Education, Communication, Business).
	
 •	The app has received more than 500 reviews.
	
 •	The dataset is aggregated by month using the Last Updated field.
	
 •	Growth is calculated as a % increase from the previous month, and if the growth is greater than 20%, that segment is shaded under the line using a transparent fill.
	
 •	This chart is conditionally visible only between 6 PM and 9 PM IST, ensuring controlled access based on time logic.

**Insight Gained:**
	
 •	Categories like Education and Communication saw notable growth spikes, especially during months that align with exam seasons, school terms, or global events (like remote learning).
	
 •	Shaded regions under the lines effectively communicate “growth bursts”, making it easy for stakeholders to identify performance jumps.
	
 •	Flat or declining lines for some months signal either saturation or lack of product updates.

 **OUTPUT OF TASK 5**
<img width="1440" alt="Screenshot 2025-04-20 at 6 11 05 PM" src="https://github.com/user-attachments/assets/e7628f96-de12-443f-8b30-b20b8b87749d" />


