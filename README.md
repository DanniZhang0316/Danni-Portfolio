# Projects
## Machine Learning:
### 1. [Automatic Bee Detection Using YOLOv10 (client: Gratheon)](https://github.com/DanniZhang0316/ML-Bee-Type-Detection)         
Developed a ML pipeline for automatic detection of worker and drone bees from live video frames, achieving 97% precision and 93% recall.
- **Data Preprocessing**: Implemented high-resolution image tiling by slicing 3840×1080 images into three overlapping tiles.
- **Data Augmentation**: Applied copy-paste augmentation by extracting and augmenting drone instances and reinserting them into training images, improving mAP@50–95 from 0.63 to 0.66.

responsibility: YOLOv10 trainning, data preprocessing and augmentation

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

**Technologies:**  
Python | Scikit-learn | XGBoost | GridSearchCV | Machine Learning | Data Preprocessing | Model Evaluation  

## Data Analysis
### 1. [Uber Pickups Analysis in New York City](https://github.com/DanniZhang0316/Data-Analysis-Uber-pickups)
Analyzed 4.5 million Uber trip records (April–September) to identify temporal and spatial demand patterns across New York City, supporting data-driven insights for service optimization and fleet management.

- **Data Processing & Exploration**: Merged six monthly datasets and performed large-scale data cleaning and preprocessing. Conducted exploratory data analysis to uncover monthly, weekly, and hourly demand patterns.

- **Time-Series Analysis**: Identified peak usage periods, including evening rush hours (16:00–19:00), weekday vs. weekend differences (+19.6% higher demand on weekdays), and special Monday demand behavior.

- **Spatial Analysis**: Generated geographic heatmaps to detect high-demand pickup hotspots and low-demand regions, highlighting core service areas and potential outliers.

**Technologies:**  
Python | Pandas | NumPy | Matplotlib | Seaborn | Geospatial Analysis | Data Visualization | Time-Series Analysis  

## Data Engineering
### 1.
