# 🚀 SpaceX Falcon 9 First Stage Landing Prediction

<div align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python Badge"/>
  <img src="https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white" alt="Jupyter Badge"/>
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas Badge"/>
  <img src="https://img.shields.io/badge/scikit_learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" alt="Scikit-Learn Badge"/>
  <img src="https://img.shields.io/badge/Plotly-239120?style=for-the-badge&logo=plotly&logoColor=white" alt="Plotly Badge"/>
  <img src="https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white" alt="SQLite Badge"/>
</div>

<br/>

## 📝 Project Overview

SpaceX relies on the reusability of its Falcon 9 rocket's first stage to radically reduce the cost of space launches—from approximately $165 million to around $62 million. Predicting whether the first stage will successfully land is crucial for competitive pricing and resource management. 

This repository contains an end-to-end **Data Science & Machine Learning Pipeline** dedicated to predicting the successful landing of the Falcon 9 first stage. By analyzing historical launch data, payload mass, orbit types, and launch vehicle specifications, we’ve developed machine learning classification models to accurately forecast landing outcomes.

> **Note:** This project represents a capstone for applied data science and predictive analytics techniques, showcasing real-world data collection, exploratory data analysis (EDA), interactive geospatial mapping, and machine learning modeling.

---

## 🛠️ Data Science Pipeline & Architecture

The project is structured into sequentially organized modules, capturing the full lifecycle of a predictive analytics project:

### 1. Data Collection
* **`1-SpaceX_API_Scraping`**: Interfaced with the comprehensive SpaceX REST API to extract historical launch data, booster versions, payload specifications, and landing outcomes.
* **`2-SpaceX_WebScrping`**: Scraped supplemental tabular data from Wikipedia using `BeautifulSoup` to enrich our dataset with missing historical context and launch vehicle metrics.

### 2. Data Wrangling
* **`3-SpaceX_Data wrangling`**: Handled missing values, formatted datetime strings, standardized categorical variables, and engineered novel features (like computing the success rate per orbit). We transformed raw API/scraping outputs into rigorous analytical datasets.

### 3. Exploratory Data Analysis (EDA)
* **`4-SpaceX_EDA_sqllite`**: Executed complex SQL queries to identify foundational patterns in the dataset. Extracted insights regarding payload limits and success probabilities across distinct launch sites.
* **`5-SpaceX_EDA`**: Leveraged `Pandas`, `Matplotlib`, and `Seaborn` to create rich statistical visualizations. Investigated the correlation between payload mass, flight number, launch site, and the ultimate landing success.

### 4. Interactive Visualizations & Geospatial Mapping
* **`6-SpaceX_DashBoard`**: Built a comprehensive interactive dashboard utilizing `Plotly Dash`. Features interactive pie charts and scatter plots that dynamically respond to user inputs, dynamically filtering down by launch site and payload mass.
* **`7-SpaceX_Location_Folium`**: Developed interactive geographic maps using `Folium`. Plotted active launch sites, measured distances to geographical features (coastlines, highways, railways), and analyzed their impact on safety and operational feasibility.

### 5. Predictive Modeling
* **`8-SpaceX-Machine-Learning-Prediction`**: Built, validated, and tuned multiple machine learning algorithms:
  - **Logistic Regression**
  - **Support Vector Machines (SVM)**
  - **Decision Tree Classifier**
  - **K-Nearest Neighbors (KNN)**
* Hyperparameter tuning was performed utilizing `GridSearchCV`. We analyzed confusion matrices and evaluated the models structurally based on accuracy and robust generalization to unseen data.

---

## 🔬 Core Findings and Insights

* **Flight Experience Matters:** As the `FlightNumber` increases, the likelihood of a successful first-stage landing substantially increases, indicating accumulated expertise and procedural refinements over time.
* **Payload Influences:** Extreme payload masses show a varied impact on success rates; optimal success brackets exist based on specific orbit destinations (e.g., LEO, ISS).
* **Launch Site Discrepancies:** Specific launch sites, such as KSC LC-39A, exhibit distinctly higher historical success rates compared to others.
* **Model Performance:** While multiple models performed well, the finely tuned **Decision Tree** and **SVM** algorithms exhibited peak performance on the test set, achieving robust and reliable classification metrics.

---

## 🗂️ Repository Structure

```text
📦 SpaceX-Falcon9-Prediction
 ┣ 📜 1-SpaceX_API_Scraping.pdf           # Data extraction from SpaceX API
 ┣ 📜 2-SpaceX_WebScrping.pdf             # Web scraping Falcon 9 historical data
 ┣ 📜 3-SpaceX_Data wrangling.pdf         # Data cleaning and feature engineering
 ┣ 📜 4-SpaceX_EDA_sqllite.pdf            # SQL-based Exploratory Data Analysis
 ┣ 📜 5-SpaceX_EDA.pdf                    # Python/Pandas Exploratory Data Analysis
 ┣ 📜 6-SpaceX_DashBoard.pdf              # Interactive Plotly Dash Application
 ┣ 📜 7-SpaceX_Location_Folium.pdf        # Geospatial mappings and distance visualisations
 ┣ 📜 8-SpaceX-Machine-Learning-Prediction.pdf # Machine Learning modeling and evaluation
 ┗ 📜 README.md                           # Project documentation (You are here!)
```

*(Note: The current repository provides the compiled analysis and results as readable PDF reports. The methodologies, scripts, and code execution are thoroughly documented within these documents.)*

---

## 💻 Technical Stack

- **Data Manipulation:** `Pandas`, `NumPy`, `SQL (SQLite3)`
- **Web Scraping & API:** `Requests`, `BeautifulSoup`
- **Machine Learning:** `Scikit-Learn` (`LogisticRegression`, `SVC`, `DecisionTreeClassifier`, `KNeighborsClassifier`, `GridSearchCV`)
- **Data Visualization:** `Matplotlib`, `Seaborn`, `Plotly`, `Dash`
- **Geospatial Analysis:** `Folium`

---

## 🚀 Future Enhancements

- **Deep Learning Integration:** Explore neural networks (e.g., TensorFlow/Keras) for potentially higher complex pattern recognition.
- **Real-Time Forecasting Model:** Connect directly to the live SpaceX API via an automated CI/CD pipeline allowing for real-time model retraining and live-feed forecasting.
- **Advanced Feature Engineering:** Incorporate atmospheric, meteorological, and telemetry data for deeper multidimensional feature spaces.

---

<div align="center">
  <i>Developed applying advanced Machine Learning & Data Engineering techniques. </i>
  <br>
  <b><a href="#-spacex-falcon-9-first-stage-landing-prediction">Return to Top</a></b>
</div>
