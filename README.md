# Exploratory Data Analysis and Clustering on the Wine Dataset (From Scratch)

Overview

This project implements Principal Component Analysis (PCA) and k-Means Clustering from scratch using only NumPy. The dataset contains 178 samples of three different wine cultivars, each with 13 chemical properties.

PCA is used for dimensionality reduction, transforming the dataset into an orthogonal feature space. k-Means Clustering is then applied to group the wines based on chemical similarities. This project avoids external machine learning libraries like sklearn to provide full mathematical transparency.

Project Structure

```
wine-PCA-Kmeans
├── wine.csv              # Dataset
├── pca_kmeans.py         # Main Python script with PCA & k-means implementation
├── requirements.txt      # Dependencies for running the project
├── README.md             # Project documentation
├── results/              # Folder for plots & outputs (created when running the script)
└── notebooks/            # Optional Jupyter Notebooks with detailed analysis
```

The Wine Dataset

The dataset consists of 178 wine samples, each described by 13 chemical features:
	•	Alcohol
	•	Malic acid
	•	Ash
	•	Alcalinity of ash
	•	Magnesium
	•	Total phenols
	•	Flavanoids
	•	Nonflavanoid phenols
	•	Proanthocyanins
	•	Color intensity
	•	Hue
	•	OD280/OD315 (optical density ratio)
	•	Proline concentration

Each sample is labeled as one of three wine cultivars. The goal is to reduce dimensionality using PCA and explore clustering patterns in the data.

Methodology

Data Preprocessing

Each feature is mean-centered and scaled to unit variance before PCA. The covariance matrix is computed from the standardized features, and eigen decomposition is used to extract the principal components. An alternative method using Singular Value Decomposition (SVD) is also explored.

PCA Implementation
	•	Compute the covariance matrix of the standardized data.
	•	Perform eigen decomposition to extract principal components.
	•	Transform the dataset into the PCA space.
	•	Verify results using SVD.

k-Means Clustering

The k-Means algorithm is implemented from scratch and applied to the first two principal components to group the wines into three clusters. This approach helps reveal natural groupings in the dataset.

Results and Visualizations
	•	Covariance matrix heatmap showing feature correlations.
	•	Explained variance plot illustrating the variance captured by each principal component.
	•	Cluster visualization in the reduced PCA space.

Running the Project

Install Dependencies

Ensure you have Python 3.x installed, then install dependencies:

pip install -r requirements.txt

Run the Main Script

Execute the script to perform PCA and clustering:

python pca_kmeans.py

View Results

Plots and outputs will be saved in the results/ directory. The script generates visualizations for PCA-transformed data, covariance matrix, and clustering results.

Dependencies

This project uses NumPy, Matplotlib, and Pandas. The required dependencies are listed in requirements.txt.

Additional Resources

For further reading on PCA and k-Means clustering, refer to:
	•	PCA: Stanford CS229 Notes
	•	k-Means Clustering: Stanford CS229 Notes

License

This project is open-source and licensed under the MIT License.

This version keeps everything clear and professional while avoiding unnecessary formatting and lists. Let me know if you need any modifications.
