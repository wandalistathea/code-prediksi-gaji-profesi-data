# Salary Prediction in Data-Related Jobs Using Machine Learning Regression

## Project Overview
The ideal condition in determining employees' salaries is adjusted depending on their competencies and qualifications. But not infrequently, companies generalize the job salary even though the qualifications are different. On the other hand, prospective employees are also sometimes confused about how much they should earn based on their background and capabilities.
- Predict the salary of data-related jobs (Data Analyst, Data Scientist, and Data Engineer) based on: name of the profession, company location, level of employment, years of experience, company size, and industry type.
- The dataset was taken by scraping the LinkedIn (November 4, 2021) and Jobstreet (December 6, 2021) sites so the point of view of data is from the company side.
- Deploy a Machine Learning model using Flask and Heroku so the end-users can input some data and get the result of salary prediction directly. Actually, the web app can be accessed [prediksi-gaji-profesi-data.herokuapp.com](https://prediksi-gaji-profesi-data.herokuapp.com/) but no longer now. So [...](drive) is the picture of that web app on my local page.

## Objectives
* The objective is to make salary predictions based on several variables. As a result, the model can help companies and employees or job seekers to negotiate the amount of competitive salary that they should pay or earn so that will give them a win-win solution.

## Methodology
- **Scraping Data**

  Scraped data from LinkedIn and Jobstreet using [this code](https://github.com/wandalistathea/code-prediksi-gaji-profesi-data/blob/main/1.%20Linkedin%20Job%20Scraping%20OKE.ipynb) and [this](https://github.com/wandalistathea/code-prediksi-gaji-profesi-data/blob/main/1.%20Jobstreet%20Job%20Scraping%20OKE.ipynb).
  
- **Preprocessing Step 1**

  Equated the data writing format, combined data from 2 sources (LinkedIn and Jobstreet), and removed duplicate data so that the data was ready to be processed. The process used [this code](https://github.com/wandalistathea/code-prediksi-gaji-profesi-data/blob/main/2.%20Preprocessing%20Hasil%20Scraping%20JobStreet.ipynb), [this](https://github.com/wandalistathea/code-prediksi-gaji-profesi-data/blob/main/2.%20Preprocessing%20Hasil%20Scraping%20Linkedin.ipynb), and [this](https://github.com/wandalistathea/code-prediksi-gaji-profesi-data/blob/main/3.%20Gabungan%20Data%20Linkedin%20dan%20Jobstreet%20(Hasil%20Preprocessing).ipynb).

- **Exploratory Data Analysis and Data Visualization**

  Analyzed the data and got an overview of the data. The process used code [here](https://github.com/wandalistathea/code-prediksi-gaji-profesi-data/blob/main/4.%20EDA%20dari%20Data%20Gabungan.ipynb). The visualization also used Tableau with the result is in the folder ...
  
- **Preprocessing Step 2**

  Dropped missing or null salaries values in the dataset, performed feature selection, handled other missing values and categorical data, performed target engineering. The process used code [here](https://github.com/wandalistathea/code-prediksi-gaji-profesi-data/blob/main/5.%20REVISI%20-%20Preprocessing%20Tahap%202%20(Feature%20Selection%20s.d.%20Target%20Engineering).ipynb).
  
- **Modeling**

  The methods used were: Decision Tree, Random Forest, and Support Vector Regression (SVR). In the modeling process, hyperparameter tuning was also carried out. In this process also used resampling using SMOTE to balance the amount of data in each category (name of profession). The process used [this code](https://github.com/wandalistathea/code-prediksi-gaji-profesi-data/blob/main/6.%20REVISI%20-%20Modelling%20(Perbandingan%20Metode%20%26%20Learning%20Curve).ipynb) and [this](https://github.com/wandalistathea/code-prediksi-gaji-profesi-data/blob/main/7.%20REVISI%20-%20Modelling%20Ulang%20Menggunakan%20Decision%20Tree%20dan%20SMOTE.ipynb).
  
- **Model Evaluation**

  Used R-squared, Root Mean Square Error (RMSE), and Mean Absolute Percentage Error (MAPE) values from 5-fold cross-validation.

## Web App (Flask)
End-users can predict the monthly salary based on these variables:
- **Name of the profession:** Data Analyst, Data Scientist, Data Engineer.
- **Company location:** Bali, Banten, Yogyakarta, Jakarta, West Java, East Java, West Kalimantan.
- **Level of employment:** Intern, Entry Level, Associate, Mid Level Senior.
- **Years of Experience:** How many years of experience.
- **Company size:** 1-50 employees, 51-200 employees, 201-500 employees, 501-1,000 employees, 1,001-5,000 employees, >5,000 employees.
- **Industry type:** Events, Economics, Human Resources, Finance, Construction, Consulting, Media, Marketing & Advertising, Information and Communication Technology, Transportation.

Code for deployment can be accessed in [this repository](https://github.com/wandalistathea/prediksi-gaji-profesi-data/tree/main).

## Conclusions
Decision Tree Regressor using SMOTE with the amount of data per category "name of the profession" n=87 resulted in a better performance with the evaluation results were **R-squared of 0.683 (68.3%), RMSE of 144.4, and MAPE of 12.6%**.
