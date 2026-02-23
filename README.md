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
