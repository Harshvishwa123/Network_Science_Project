# 📚 Exploration of Amazon’s Co-Purchase Network

**Authors**: Dhairya, Harsh Vishwakarma, Divyansh  
**Institute**: IIIT Delhi  
**Course Project**: Network Science  
**Email**: dhairya22157@iiitd.ac.in, harsh22205@iiitd.ac.in, divyansh22178@iiitd.ac.in  

---

## 🧠 Project Overview

This project explores a real-world **co-purchase network** from Amazon using **network science techniques**. Each node represents a product (primarily books/music), and each edge represents a co-purchase relationship.

### 🔍 Key Goals

- Analyze the **topological structure** of the co-purchase graph
- Detect **communities** of related products
- Investigate **scale-free** and **small-world** network properties
- Build **predictive models** to forecast future co-purchases

---

## 🗂️ Files in This Repository

| File | Description |
|------|-------------|
| `NS_Project.ipynb` | Jupyter notebook with full analysis and modeling |
| `products.csv` | Product metadata including title, category, sales rank, rating |
| `Network_science_Project.pdf` | Detailed report of methodology, results, and model evaluation |
| `Exploration of Amazon’s Co-Purchase Network.pptx` | Presentation slides summarizing the project |

---

## 🧾 Dataset Description

### 1. `products.csv`  
Metadata for products including:
- `id`, `title`, `group` (category)
- `salesrank`, `rating`, `downloads`, `review count`

### 2. `copurchase.csv`  
A directed edge list where:
- `source` = purchased product
- `target` = frequently co-purchased product

> 🧮 **Nodes**: 310,771 | **Edges**: 915,666 | **Avg Degree**: 5.89

---

## 📊 Analysis & Findings

### ✅ Topological Analysis

- **Degree Distribution** follows a long-tail (heavy-tailed) structure  
- **Clustering Coefficient** = 0.4198 → Strong product grouping  
- **Assortativity** = -0.0025 → Disassortative mixing observed  
- **Connected Components**:  
  - 6,595 Strongly Connected Components  
  - 1 Weakly Connected Component with 262,110 nodes  

### 📌 Community Detection

- Louvain algorithm used  
- **164 communities** detected  
- **Modularity** = 0.9016 → Strong community structure  
- Thematic product groupings (e.g. same book genres)

### 🌐 Network Properties

- **Scale-Free Behavior**: Degree distribution heavy-tailed  
- **Small-World**:  
  - Avg. shortest path = 9.89  
  - Clustering ratio vs. random graph = 11,397.82  

---

## 🤖 Co-Purchase Prediction

### 📥 Feature Engineering

- Salesrank Difference  
- Preferential Attachment  
- Rating Product  
- Common Neighbors  
- Jaccard Coefficient  
- Adamic-Adar Index  
- Resource Allocation Index

### 🧪 Models Trained

- Gradient Boosting (Best: **AUC = 0.7935**)
- Random Forest
- Logistic Regression
- Neural Network
- K-Nearest Neighbors

> ✅ Best Model: **Gradient Boosting Classifier**  
> F1 Score: 0.7122 | Cross-validated AUC: 0.8062

---

## 🧠 Recommendation System

Users can:
- Predict the **likelihood of co-purchase** for any two products
- Get **top-N recommendations** for a product using link prediction

Includes a **Graphical User Interface (GUI)** for live demos.

---

## 🛠️ Technologies Used

- **Python**, **Jupyter Notebook**
- **NetworkX**, **Pandas**, **NumPy**
- **Matplotlib**, **Plotly**
- **Scikit-learn**

---

## 🚀 Getting Started

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/amazon-co-purchase-network.git
   cd amazon-co-purchase-network
