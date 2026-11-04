# Winning the Space Race with Data Science

Capstone project for the IBM Data Science Professional Certificate (Coursera): predicting whether the first stage of a SpaceX Falcon 9 rocket will land successfully.

## Why it matters

SpaceX advertises Falcon 9 launches at about 62 million dollars, while other providers charge upwards of 165 million. Much of that saving comes from landing and reusing the first stage. If we can predict whether the first stage will land, we can estimate the cost of a launch, which is useful for any company bidding against SpaceX.

## Project files

| Step | File | What it does |
|---|---|---|
| 1 | [jupyter-labs-spacex-data-collection-api.ipynb](jupyter-labs-spacex-data-collection-api.ipynb) | Collects launch data from the SpaceX REST API |
| 2 | [jupyter-labs-webscraping.ipynb](jupyter-labs-webscraping.ipynb) | Scrapes Falcon 9 launch records from Wikipedia with BeautifulSoup |
| 3 | [labs-jupyter-spacex-Data_wrangling.ipynb](labs-jupyter-spacex-Data_wrangling.ipynb) | Cleans the data and creates the landing label (1 = landed, 0 = did not land) |
| 4 | [jupyter-labs-eda-sql-coursera_sqllite.ipynb](jupyter-labs-eda-sql-coursera_sqllite.ipynb) | Explores the data with SQL queries on SQLite |
| 5 | [edadataviz.ipynb](edadataviz.ipynb) | Explores the data with charts and prepares features for modeling |
| 6 | [lab_jupyter_launch_site_location.ipynb](lab_jupyter_launch_site_location.ipynb) | Maps launch sites, outcomes and nearby features with Folium |
| 7 | [spacex-dash-app.py](spacex-dash-app.py) | Interactive Plotly Dash dashboard of launch outcomes by site and payload |
| 8 | [SpaceX_Machine_Learning_Prediction_Part_5.ipynb](SpaceX_Machine_Learning_Prediction_Part_5.ipynb) | Trains and tunes four classification models |
| | [IBM_DS_Capstone_Ezinne_Okereke.pdf](IBM_DS_Capstone_Ezinne_Okereke.pdf) | Final presentation |

## Key results

- **Landing success improved with experience:** 66.7% of the 90 Falcon 9 launches landed. The yearly success rate rose from 0% (2010 to 2013) to about 90% in 2019.
- **Launch site matters:** KSC LC-39A has the highest success rate, 76.9% (10 of 13 launches).
- **Site locations follow a pattern:** KSC LC-39A is 0.68 km from a railway, 0.84 km from a highway, 3.96 km from the coast and 16.30 km from the nearest city.
- **Models:** Logistic Regression, SVM, Decision Tree and KNN all reached 83.3% accuracy on the test set (15 of 18 launches). The Decision Tree had the best cross-validation accuracy (0.891). All four models made the same mistake: 3 failed landings predicted as landings.

## Note on the data

The SpaceX API (api.spacexdata.com) returned HTTP 522 errors throughout this project. The API project was archived in June 2026. The data collection notebook shows the attempt and the error. The launch records came from IBM's static copy of the API response, and the later notebooks use IBM's prepared datasets.

## Tools

Python, pandas, NumPy, requests, BeautifulSoup, SQLite, Matplotlib, Seaborn, Folium, Plotly Dash, scikit-learn

## Author

Ezinne Okereke