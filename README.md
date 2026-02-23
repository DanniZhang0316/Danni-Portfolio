# Projects
## Machine Learning:
### 1. [Automatic Bee Detection Using YOLOv10 (client: Gratheon)](https://github.com/DanniZhang0316/ML-Bee-Type-Detection)         
Developed a ML pipeline for automatic detection of worker and drone bees from live video frames, achieving 97% precision and 93% recall.
- **Data Preprocessing**: Implemented high-resolution image tiling by slicing 3840×1080 images into three overlapping tiles.
- **Data Augmentation**: Applied copy-paste augmentation by extracting and augmenting drone instances and reinserting them into training images, improving mAP@50–95 from 0.63 to 0.66.

**Technologies**: Roboflow | Python

### 2. [Topic Modeling of COVID-19 Open Research (CORD-19 Dataset)](https://github.com/DanniZhang0316/NLP-COVID-19-Topic-Modeling)
Developed an end-to-end NLP pipeline to identify and track latent research themes across 1M+ COVID-19 scientific publications using semantic embeddings and unsupervised learning.

- **Semantic Representation**: Generated 384-dimensional SBERT embeddings for research abstracts to capture contextual meaning beyond keyword frequency.

- **Dimensionality Reduction**: Applied PCA (70% variance retained) to reduce feature space from 384 → 78 dimensions, improving clustering efficiency and scalability.

- **Clustering**: Implemented MiniBatchKMeans (k = 20, selected via silhouette score) to identify major research topics across decades (1970–2020).

- **Topic Labeling & Interpretation**: Extracted TF-IDF keywords per cluster, removed generic COVID terms, and assigned interpretable labels. Identified 20 distinct research themes and their temporal evolution.

**Technologies**: Python | SBERT | PCA | MiniBatchKMeans | TF-IDF | NLP | Unsupervised Learning | Data Visualization

### 3. [ML-Driven Predictive Analysis for Loans](https://github.com/DanniZhang0316/ML-Loan-Classification)  
Developed a machine learning pipeline to predict loan approval outcomes using a dataset of 45,000 samples, enabling automated decision-making and reducing human bias in the loan approval process.

- **Data Processing**: Cleaned and prepared the dataset by removing outliers and correcting skewed feature distributions using logarithmic transformations. Applied a standard deviation–based secondary filtering method for robust anomaly detection, and conducted exploratory data analysis with visualizations to better understand data patterns.

- **Model Development**: Evaluated six classification algorithms, including Random Forest and Logistic Regression, and optimized model performance through cross-validation and hyperparameter tuning using GridSearchCV.

- **Results**: Compared performance across all six models and identified XGBoost, and Random Forest as the top performers, achieving ROC-AUC scores ranging from 0.96 to 0.97.

**Technologies**:  
Python | Scikit-learn | XGBoost | GridSearchCV | Machine Learning | Data Preprocessing | Model Evaluation  

## Data Analysis
### 1. [Uber Pickups Analysis in New York City](https://github.com/DanniZhang0316/Data-Analysis-Uber-pickups)
Analyzed 4.5 million Uber trip records (April–September) to identify temporal and spatial demand patterns across New York City, supporting data-driven insights for service optimization and fleet management.

- **Data Processing & Exploration**: Merged six monthly datasets and performed large-scale data cleaning and preprocessing. Conducted exploratory data analysis to uncover monthly, weekly, and hourly demand patterns.

- **Time-Series Analysis**: Identified peak usage periods, including evening rush hours (16:00–19:00), weekday vs. weekend differences (+19.6% higher demand on weekdays), and special Monday demand behavior.

- **Spatial Analysis**: Generated geographic heatmaps to detect high-demand pickup hotspots and low-demand regions, highlighting core service areas and potential outliers.

**Technologies:**  
Python | Pandas | NumPy | Matplotlib | Seaborn | Geospatial Analysis | Data Visualization | Time-Series Analysis  

### 2. [Sleep Health & Lifestyle Analysis (with R)](https://github.com/DanniZhang0316/R-Sleep-Health-And-Lifestyle/blob/main/R_projekt_DanniZhang.pdf)  

Conducted an exploratory statistical analysis on a dataset of 374 individuals and 13 lifestyle and health variables to identify key factors influencing sleep quality.

- **Exploratory Data Analysis**: Computed descriptive statistics for numerical and categorical variables, including age, sleep duration, stress level, BMI category, and cardiovascular indicators.

- **Correlation Analysis**: Applied Spearman correlation to evaluate relationships between sleep quality and lifestyle factors. Identified strong positive correlation between sleep duration and sleep quality (r = 0.89) and strong negative correlation between stress level and sleep quality (r = -0.91).

- **Group Comparisons**: Analyzed sleep quality differences across stress levels, BMI categories, gender, and occupation groups using categorized visual comparisons.

- **Key Insights**:
  - Higher stress levels significantly reduce sleep quality.
  - Longer sleep duration strongly improves perceived sleep quality.
  - Elevated heart rate and higher BMI are associated with poorer sleep.
  - High-stress professions (e.g., doctors, sales representatives, scientists) show lower average sleep quality.

**Technologies**:  
R | Statistical Analysis | Spearman Correlation | Data Visualization | Exploratory Data Analysis

## Data Engineering & Database
### 1. [End-to-End Financial Data Warehouse (Airflow + dbt + ClickHouse)](https://github.com/DanniZhang0316/Data-Engineering-Stock/tree/master)    

Designed and implemented a production-style data platform to ingest, transform, and analyze S&P 600 stock market data using modern data engineering tools and a star schema warehouse model.

- **Data Architecture**: Built a star schema data warehouse consisting of a central FactStockPrice table and SCD Type 2 dimension tables (Company, Exchange, Currency) with full historical tracking.

- **Data Ingestion**: Orchestrated daily and monthly ETL pipelines in Apache Airflow to extract data from AlphaVantage APIs, Wikipedia scraping. Implemented automated refresh frequencies (daily, weekly, monthly).

- **Storage & Processing**: Stored raw data in clickhouse and transformed data into a structured warehouse model with surrogate keys, referential integrity checks, and range validations.

- **Data Transformation (dbt)**: Developed staging and mart models to generate fact and dimension tables, including incremental loading strategies and data quality tests.

- **Iceberg Integration**: Implemented Apache Iceberg as a bronze layer for daily stock data and exposed Iceberg tables as read-only analytical tables in ClickHouse.

-  **Data Governance & Security**: Implemented role-based access control (RBAC) with column-level security and data pseudonymization in ClickHouse, enforcing fine-grained access control over sensitive company attributes.

- **Analytics & Business Queries**: Built SQL analytics answering key business questions such as:
  - Top 3 most-traded companies per sector (Q1 2025)
  - Sector composition trends (2000–2025)
  - Highest volatility stocks
  - Price growth leaders

**Technologies**:  
Apache Airflow | dbt | ClickHouse | Apache Iceberg | Docker | Python | SQL | OpenMetadata | Star Schema Modeling

### 2. [LEC 2024 Winter Season Database Design (League of Legends EMEA Championship)](https://github.com/DanniZhang0316/Postgres-LEC-Match-Database/tree/main)  

Designed and implemented a fully normalized relational database for the League of Legends EMEA Championship (LEC) 2024 Winter Season, centralizing fragmented esports data into a structured system for analytics and strategic decision-making.

- **Conceptual Modeling**: Developed an Entity-Relationship (ER) model covering teams, players, matches, match details, formats, and roles based on formal business rules.

- **Normalization**: Transformed the conceptual model into 3NF relational schema; analyzed functional dependencies and justified normalization decisions.

- **Schema Implementation**: Created PostgreSQL tables with:
  - Primary & foreign keys
  - CHECK constraints (e.g., match format limits, date validation)
  - Unique constraints
  - Cascading updates/deletes

- **Advanced SQL Development**:
  - Created analytical views (e.g., team total wins ranking)
  - Implemented stored functions:
    - Top 3 most-used champions per player with win rate
    - Top 3 players per role (role-specific evaluation logic)
    - Player contribution score to team victories
  - Implemented stored procedures:
    - Add new team & player with historical tracking
    - Compare two players' performance contribution

**Technologies**:  
PostgreSQL | Database Normalization (3NF) | ER Modeling | Views | Constraint Design
