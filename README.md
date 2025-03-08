# K-Means Clustering - Cricket Player Analysis  

## Overview  
This project applies **K-Means Clustering** to classify cricket players based on their performance metrics. The dataset contains player statistics such as **matches played, innings, runs, strike rate, and batting average**.  

## Dataset  
📂 **File:** `Cricket (1).csv`  
📊 **Rows:** Varies (Player-wise data)  
🔢 **Columns:**  

### **Key Features:**  
- **Player** – Cricketer's name  
- **Mat** – Matches played  
- **Inns** – Innings played  
- **NO** – Not outs  
- **Runs** – Total runs scored  
- **HS** – Highest individual score  
- **Ave** – Batting average  
- **BF** – Balls faced  
- **SR** – Strike rate  
- **100, 50, 0** – Number of centuries, half-centuries, ducks  
- **Span** – Playing duration (Start-End year)  
- **exp** – Experience (calculated as `end - start`)  

---

## **Project Workflow**  

### **1️⃣ Data Preprocessing**  
- Cleans missing values and converts categorical columns to numeric  
- Extracts **Start and End years** from the `Span` column to compute **player experience (`exp`)**  
- Converts `HS` (Highest Score) into a numeric format  

### **2️⃣ Feature Scaling**  
- Uses **StandardScaler** to normalize numerical columns (`Mat`, `Inns`, `Runs`, `Ave`, `SR`, etc.)  

### **3️⃣ Clustering with K-Means**  
- Trains a **K-Means model (4 clusters)** on the scaled data  
- Assigns each player a **Cluster ID (`Cluster_id`)**  
- Evaluates cluster performance using **Elbow Method**  

### **4️⃣ Visualization**  
- **Scatter plot of Runs vs. Balls Faced (BF)** to analyze clusters  
- Highlights **centroids** in **red (X marker, size=200)**  

---

## **Technologies Used**  
🚀 **Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn**  

## **Results & Insights**  
- **Clustered players into 4 performance groups** based on their batting stats  
- **Higher experience correlates with better averages**  
- **Strike Rate & Runs are key differentiators** in clustering  

## **Future Improvements**  
🔹 Experiment with **DBSCAN or Hierarchical Clustering**  
🔹 Include **bowling performance** to analyze all-rounders  
🔹 Tune `n_clusters` using **Silhouette Score**  
