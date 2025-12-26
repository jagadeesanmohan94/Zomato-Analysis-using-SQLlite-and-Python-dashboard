# Zomato-Analysis-using-SQLlite-and-Python-dashboard

Zomato-Restaurant-Data-Analysis-and-Text-Mining

Dashboard link:

Zomato_analysis.ipynb.


Description:
A complete end-to-end data analytics project analyzing Zomato’s Bengaluru restaurant dataset using SQL, Python, and NLP. Includes EDA, customer behavior analysis, rating insights, geospatial heatmaps, and text mining of customer reviews.

![Image](https://github.com/user-attachments/assets/d8452ff8-1278-48d0-b20d-0cde717d6d41)

![Image](https://github.com/user-attachments/assets/16c56e4b-b68f-4222-b18c-c1c6e23b74fe)

⭐ Project Overview
Food delivery platforms like Zomato generate millions of customer interactions daily. Understanding patterns in ratings, online ordering behavior, restaurant location density, and customer sentiments can help businesses optimize service quality and improve customer experience.
In this project, I analyzed a large Zomato raw dataset (SQLite format) to uncover:
•	Trends in restaurant ratings
•	Online-order vs offline-order customer behavior
•	Location based restaurant density
•	Text analysis of customer reviews
•	Word & bi gram frequency insights
The project combines SQL, Python, Pandas, Matplotlib, Seaborn, and Text Mining techniques.


![Image](https://github.com/user-attachments/assets/371052f4-c796-42a7-81bb-8a1cb4605574)

![Image](https://github.com/user-attachments/assets/05e4693a-4362-4429-be74-8c9c46eb8c32)

![Image](https://github.com/user-attachments/assets/10c7946f-be01-4186-ab67-8c792ce2ac5f)

![Image](https://github.com/user-attachments/assets/1007e2f5-1b3a-4599-af6a-bc82daa28808)

![Image](https://github.com/user-attachments/assets/927c6423-77ec-4c0b-a369-2c76b183c923)


________________________________________
📁 1. Data Extraction (SQLite)
I connected to the raw database using Python’s sqlite3 module:
Python
import sqlite3
import pandas as pd

con = sqlite3.connect(r"C:\...\zomato_rawdata.sqlite")
df = pd.read_sql_query("SELECT * FROM Users", con)
df.head()
Show more lines
This extracted the full dataset for cleaning and analysis.
________________________________________
🧽 2. Data Cleaning
✔ Handling inconsistent rating formats
Ratings contained values like "4.1/5", "NEW", and "-" which required cleaning.
✔ Removing nulls & duplicates
Ensured analytical accuracy by filtering missing ratings, locations, and reviews.
✔ Text preprocessing for NLP
•	Lowercasing
•	Removing punctuation
•	Removing stopwords
•	Tokenization
•	Generating unigrams & bigrams
________________________________________
📊 3. Key Insights & Visualizations
________________________________________
📈 A. Rating Distribution by Online Order Availability
Stacked Count Plot
(Image from your notebook is represented here)
🔍 Insight:
•	Restaurants offering online ordering consistently receive higher volume of ratings.
•	There is a clear concentration between 3.5 – 4.0, indicating most customers rate average-to-good experiences.
________________________________________
📉 B. Percentage Distribution by Rating
This plot normalizes the rating distribution to percentages.
🔍 Insight:
•	Across all rating buckets, the share of customers choosing online ordering is significantly higher than dine-in.
•	Lower ratings (2.0–3.0) show a larger offline share, suggesting dine in experiences may face more operational challenges.
________________________________________
🗺 C. Bengaluru Restaurant Heatmap
(Heatmap image included in your upload)
Created using folium and HeatMap().
🔍 Insight:
•	High restaurant density in Koramangala, Indiranagar, MG Road, HSR Layout, and BTM.
•	These hotspots correlate with areas known for tech parks and nightlife.
This helps brands identify expansion potential, delivery demand, and competition hotspots.
________________________________________
📝 4. Text Analytics on Customer Reviews
🔤 A. Word Frequency Plot (Unigrams)
(Your screenshot included a word frequency descending plot)
🔍 Key word insights:
•	Frequent words like good, place, food, taste, service indicate dominant themes customers care about.
•	High frequency of neutral words like n, Rated, x were removed as noise.
________________________________________
👫 B. Bigram Frequency Plot
(Your bigram frequency screenshot)
Most frequent bigrams:
•	("Rated", "RATED") ← Cleaning artifact
•	("The", "food")
•	("really", "good")
•	("This", "place")
•	("must", "try")
🔍 Insight:
Bigram analysis helps uncover structured phrases customers use, useful for sentiment scoring.
________________________________________
🧠 5. Conclusions & Business Recommendations
📌 1. Online ordering drives higher engagement
Restaurants offering online delivery have:
✔ More number of ratings
✔ Higher visibility
✔ Better customer interaction
➡ Recommendation: Encourage restaurants to offer online ordering & promotions.
________________________________________
📌 2. Bengaluru shows clear restaurant hotspots
High-density clusters in Koramangala, Indiranagar, and HSR indicate:
✔ Prime locations for new outlets
✔ Areas with strong customer demand
➡ Recommendation: Use heatmap insight for expansion planning.
________________________________________
📌 3. Text reviews highlight food quality & service as main determinants
Most common positive bigrams include “really good”, “must try”, “good food”.
➡ Recommendation: Restaurants should focus on consistency in taste & customer service.
________________________________________
🛠 6. Tools & Technologies Used
Category	Tools
Data Extraction	SQLite, SQL
Data Processing	Python, Pandas, NumPy
Visualization	Matplotlib, Seaborn
Geospatial Analysis	Folium HeatMap
NLP/Text Mining	NLTK, Regex, Tokenization
________________________________________
🚀 7. What This Project Demonstrates About My Skills
✔ Ability to extract, clean, and transform real-world data
✔ Understanding of restaurant/food-tech business metrics
✔ Proficiency in Python for EDA, visualization & NLP
✔ Ability to present insights clearly for decision-makers
✔ Strong analytical storytelling skills
________________________________________

