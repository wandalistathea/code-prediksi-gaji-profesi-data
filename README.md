# Salary Prediction in Data-Related Jobs Using Machine Learning Regression

## Project Overview
The ideal condition in determining employees' salaries is adjusted depending on their competencies and qualifications. But not infrequently, companies generalize the job salary even though the qualifications are different. On the other hand, prospective employees are also sometimes confused about how much they should earn based on their background and capabilities.
- Predict the salary of data-related jobs (Data Analyst, Data Scientist, and Data Engineer) based on: name of the profession, company location, level of employment, years of experience, company size, and type of industry.
- The dataset was taken by scraping the LinkedIn (November 4, 2021) and Jobstreet (December 6, 2021) sites so the point of view of data is from the company side.
- Deploy a Machine Learning model using Flask and Heroku so the end-users can input some data and get the result of salary prediction directly. Actually, the website can be accessed [prediksi-gaji-profesi-data.herokuapp.com](https://prediksi-gaji-profesi-data.herokuapp.com/) but no longer now. So [here](drive) is the picture of that website on my local page.

## Objectives
* The objective is to make salary predictions based on several variables. As a result, the model can help companies and employees or job seekers to negotiate the amount of competitive salary that they should pay or earn so that will give them a win-win solution.

## Methodology
- Scraping Data - `Scraped data from LinkedIn and Jobstreet using code [here](https://github.com/wandalistathea/code-prediksi-gaji-profesi-data/blob/main/1.%20Linkedin%20Job%20Scraping%20OKE.ipynb) and [here](https://github.com/wandalistathea/code-prediksi-gaji-profesi-data/blob/main/1.%20Jobstreet%20Job%20Scraping%20OKE.ipynb)
- Data Wrangling - `Dropped misssing or null salaries values in the dataset, replacing the Years of Experience to the mean and analyzed/removed outliers.`
- Exploratory Data Analysis - `Analyzed the data and summarized the main characteristics.`
- Data Visualization - `Used boxplot, bar plot, scatter plot and violin plot to visualize the data and it's characteristics.`
- Machine Learning Algorithms - ` The models trained were: Lasso, ElasticNet, Decision Tree Regressor, KNeighbors Regressor, Random Forest Regressor and Gradient Boosting Regressor.`
- Evaluation Metrics Used - `Mean Absolute Error (MAE) and R-squared`

## Web App (streamlit)
#### End-users are able to predict the output based on the features:
- **Country of residence:** United States of America, Germany, Canada, Brazil, and so on.
- **Profession (job type):** Developer, full-stack, Developer, front-end, Data scientist or machine learning specialist, and so on.
- **Education Level:** Less than a Bachelor’s, Bachelor’s degree', Master’s degree or Postgraduate.
- **Years of Experience:** How many years of experience.

## Conclusions
Gradient Boosting Regressor Model resulted in a better performace applying prepocessing steps (Standard Scale, One Hot Encoding and Ordinal Coding) for specific features. The Model Evaluation resulted: **Mean Absolute Error of 13,612.26 and R-squared of 75.8%.**
