# LA_County_Coder_DataHacks25_project
Made by Elii Lopez and Jesus Aguilera for the 2025 DS3 DataHacks competition. 
Website: https://devpost.com/software/la-county-coders?ref_content=my-projects-tab&ref_feature=my_projects

🎥 Movie Rating Predictor - DS3 DataHacks 2025

This project was built for the 2025 DS3 DataHacks competition with the goal of predicting a movie's average rating (1–10) based on user-inputted characteristics such as director, genre, and runtime. We also explored trends in movie ratings and profitability to uncover what makes a film successful or highly rated.


📊 Project Goals

Predict a movie's average rating based on input features.

Identify trends and insights about:

Directors and their impact on movie ratings and profitability.

The influence of genre on both ratings and profits.

Whether runtime affects how well a movie is rated.

📚 Key Features

1. Data Preprocessing

Merged multiple datasets on the original_title column.

Cleaned and filtered data:

Removed movies with 0 vote count, missing or zero revenue/budget.

Filtered out extreme losses (>$263.7 million).

Lowercased and stripped whitespace from titles.

2. Feature Engineering

Calculated each movie's profit (revenue - budget).

Created one-hot encoded vectors for:

Directors

Genres (exploded into separate rows for multi-genre films)

Grouped runtimes into:

Short (< 60 min)

Medium (60–119 min)

Long (≥ 120 min)

3. Visual Explorations

Top and bottom 10 directors by average rating and profit.

Top and bottom genres by average rating and profit.

Runtime vs. rating grouped bar charts.

4. Predictive Model

Used Linear Regression to predict movie ratings.

Inputs:

Director (one-hot encoded)

Genres (multi-hot encoded)

Runtime (numerical)

Output:

Predicted rating clipped between 1 and 10.

🔮 Example Use

user_input_director = "James Cameron"
user_input_genres = ["Action", "Adventure"]
user_input_runtime = 120

The model predicts the rating for a movie with the given inputs.

💡 Insights Discovered

Sergio Leone and Damien Chazelle were among the highest-rated directors.

Documentary and History genres had the highest average ratings.

Comedy and Horror tended to have lower ratings.

Long movies (≥ 2 hrs) were generally rated higher than shorter ones.

🤖 Team & Tech

Built in Python with:

pandas, matplotlib, numpy, sklearn

Created by: [Your Team Name or Individual Name]

Hackathon: DS3 DataHacks 2025

🚀 Future Improvements

Incorporate more features: cast, release year, production company.

Use advanced models like Random Forest or XGBoost.

Build a web-based UI to let users try predictions live.

Datasets Used

We combined and analyzed two Kaggle datasets:

TMDb Movies Dataset 2023 (930K+ Movies)

Movies Dataset

Thanks for checking out our project!
