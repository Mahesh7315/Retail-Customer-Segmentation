# 🛍️ Customer Segmentation (Retail Analytics)

This project analyzes **1M+ retail transactions** from the *Online Retail II* dataset to segment customers based on purchasing behavior using **RFM (Recency, Frequency, Monetary)** analysis and **K-Means clustering**.  
The goal is to identify actionable customer groups and recommend data-driven marketing strategies to improve targeting efficiency and retention.

---

## 🚀 Objective
To group customers into distinct segments based on their purchase patterns and spending behavior, enabling businesses to:
- Personalize marketing campaigns 🎯  
- Improve customer retention 💡  
- Optimize marketing budget allocation 💰  

---

## 🧰 Tools & Technologies
- **Python** (pandas, NumPy, scikit-learn, matplotlib, seaborn)
- **Jupyter Notebook** for data exploration and visualization
- **PyCharm** for modular pipeline development
- **GitHub** for version control & documentation

---

## 📊 Dataset
**Source:** Online Retail II Dataset (UCI Machine Learning Repository)  
**Shape:** ~1,048,575 transactions  
**Key Columns:**
| Column | Description |
|:--|:--|
| Invoice | Transaction ID |
| StockCode | Product code |
| Description | Product name |
| Quantity | Number of items purchased |
| InvoiceDate | Date & time of purchase |
| Price | Unit price |
| Customer ID | Unique buyer ID |
| Country | Country of origin |

---

## ⚙️ Workflow

### 1️⃣ Data Preprocessing (`scripts/data_processing.py`)
- Removed missing or invalid `Customer ID`s  
- Filtered out returns (`Quantity < 0`)  
- Converted `InvoiceDate` to datetime  
- Created `TotalPrice = Quantity × Price`  
- Saved clean data for analysis  

### 2️⃣ Feature Engineering (RFM)
Computed for each customer:
- **Recency:** Days since last purchase  
- **Frequency:** Count of unique invoices  
- **Monetary:** Total spending amount  

### 3️⃣ Clustering (K-Means)
- Determined optimal **k = 4** using *Elbow* and *Silhouette* methods  
- Standardized RFM features  
- Assigned customers to clusters  

### 4️⃣ Cluster Profiling
| Cluster | Segment Name | Avg Recency | Avg Frequency | Avg Monetary | Customer Count | Strategy |
|:--:|:--|:--:|:--:|:--:|:--:|:--|
| 3 | 🟩 **Champions / VIPs** | 25 | 76.5 | 180,470 | 4 | Retain with loyalty perks & exclusive access |
| 1 | 🟦 **High-Value Loyalists** | 47 | 39.6 | 29,743 | 46 | Upsell & nurture into VIPs |
| 0 | 🟨 **Regular Shoppers** | 123 | 3.9 | 1,631 | 2,532 | Reactivation offers, bundle deals |
| 2 | 🟥 **At-Risk / Lost** | 528 | 1.6 | 573 | 1,634 | Deprioritize, low-cost reactivation |

---

## 🧠 Key Insights
- Only **0.1%** of customers are **Champions** but contribute significantly to revenue.  
- **Regular Shoppers** form the largest segment (~60%) — great potential for upselling.  
- Marketing efficiency can improve by **~20%** with targeted campaigns.  
- Customer retention could increase by **~15%** through loyalty and win-back programs.  

---

## 📂 Project Structure
Customer-Segmentation-Retail-Analytics/
│
├── data/
│ ├── raw/ # Original dataset
│ └── processed/ # Cleaned data
│
├── notebooks/
│ └── 01_Segmentation_Analysis.ipynb
│
├── scripts/
│ └── data_processing.py
│
├── results/
│ ├── plots/ # Cluster and elbow visualizations
│ └── reports/ # Cluster profiles and summaries
│
├── .gitignore
├── README.md
└── requirements.txt


---

## 📈 Results & Outputs
- ✅ Cleaned and validated 1M+ records  
- ✅ Created customer clusters (k=4)  
- ✅ Generated visualizations:
  - `results/plots/k_selection.png`
  - `results/plots/cluster_profiles.png`
- ✅ Saved customer profiles to:
  - `results/reports/cluster_profile.csv`

---

## 🧾 Example Business Recommendations
- **Champions:** Exclusive loyalty programs, private sale invitations.  
- **Loyalists:** Reward programs, personalized suggestions.  
- **Regular Shoppers:** Bundle offers, cart reminders.  
- **At-Risk:** Low-cost reactivation via email / discount nudges.  

---

## 👩‍💻 Author
**Mahesh** — M.Tech (Materials Science), IIT Bombay  
Driven by data analytics, machine learning, and business problem-solving.  
🔗 [LinkedIn](https://linkedin.com) | 🧠 [GitHub Projects](https://github.com)  

---

## 📜 License
This project is open-source and available under the MIT License.

---

### 🌟 Acknowledgment
Dataset: *Online Retail II* — UCI Machine Learning Repository  
Inspired by practical retail analytics case studies.
