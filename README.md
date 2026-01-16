# Machine_Learning_project
🎬 Cinema Audience Attendance Forecasting
📌 Overview

This project focuses on time-series forecasting of cinema audience attendance using data from two different ticketing platforms. The goal is to predict daily audience counts for movie theaters by leveraging historical booking patterns, calendar effects, and theater-specific attributes.

The dataset combines online booking behavior with on-site ticket sales, making it a realistic and challenging forecasting problem.

📊 Dataset Description

The dataset is collected from two independent cinema booking platforms:

1. BookNow

An online booking and aggregation platform where users can:

Search for nearby theaters

View show timings

Book tickets in advance

2. CinePOS

A Point-of-Sale (POS) system installed directly at theaters that:

Records on-site ticket sales

📁 Files Included

| File Name                       | Description                                                              |
| ------------------------------- | ------------------------------------------------------------------------ |
| `cinePOS_theaters.csv`          | Theater information from CinePOS                                         |
| `booknow_theaters.csv`          | Theater information from BookNow                                         |
| `movie_theater_id_relation.csv` | Mapping between BookNow and CinePOS theater IDs                          |
| `cinePOS_booking.csv`           | On-site booking data from CinePOS                                        |
| `booknow_booking.csv`           | Online booking data from BookNow                                         |
| `booknow_visits.csv`            | Daily audience visit counts                                              |
| `date_info.csv`                 | Calendar details (holidays, weekdays, etc.)                              |
| `sample_submission.csv`         | Submission format (`ID = book_theater_id + show_date`, `audience_count`) |

Tracks real-time audience attendance

Both platforms capture complementary audience behavior and must be used together for better forecasting accuracy.


🧠 Problem Objective

Using historical data from both platforms, the objective is to:

Forecast the future daily audience count for each theater

This is a time-series regression problem where predictions are influenced by:

Past audience trends

Online vs on-site booking behavior

Calendar effects (weekends, holidays)

Theater characteristics


⚠️ Important Notes

Audience attendance is affected by holidays, weekends, theater type, and booking trends.

Latitude and longitude values are approximate due to data anonymization.

Some theaters may be closed on certain days, resulting in zero audience counts.

Closed-theater days are included in the dataset but ignored during final scoring.

🛠️ Suggested Approach

Merge data using movie_theater_id_relation.csv

Perform time-series feature engineering (lags, rolling means)

Incorporate calendar features from date_info.csv

Use both POS and online booking patterns

Apply regression or time-series models (e.g., XGBoost, LGBM, ARIMA, LSTM)
