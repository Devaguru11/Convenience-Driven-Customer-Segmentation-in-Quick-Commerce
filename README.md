# 🛒 Convenience-Driven Customer Segmentation in Quick Commerce

## 📌 Project Objective
Analyze customer behavior in quick commerce platforms to understand **why customers order from nearby stores instead of physically visiting them**, even when the store is very close. Identify actionable customer segments based on delivery distance, time, order value, and convenience-driven behavior.

## 📊 Quick Commerce Platforms Analyzed
The project analyzes over 1,000,000 raw orders from top quick commerce platforms:
- **Swiggy Instamart** (Highest Revenue Share: ~14.05%)
- **Blinkit**
- **Zepto** (Fastest Avg Delivery Time: ~9.64 mins)
- **Big Basket**
- **Flipkart Minutes**
- **Amazon Now**
- **Dunzo**
- **Jio Mart**

## 📂 Project Structure
- `Quick_Commerce_Customer_Segmentation.ipynb`: Main Jupyter Notebook with complete data pipeline, exploratory data analysis, and clustering algorithms.
- `quick_commerce_data_raw.csv` (1,000,000 rows): Original raw dataset.
- `quick_commerce_data_modified_cleaned.csv` (947,752 rows): Cleaned and pre-processed dataset used for modeling.
- `Results/`: Directory containing generated outputs and clustering visualizations.
- `report_charts/`: Visualizations including correlation heatmaps, boxplots, distance distributions, and dendrograms.
- `dashboard.html`: Interactive HTML dashboard presenting key KPIs, charts, and actionable insights.
- `business_insights_table.csv`: Detailed metrics, behaviors, and actionable recommendations for each identified customer segment.
- `company_comparison_report.csv`: Performance and metric comparison across different quick commerce competitors.
- `kpi_summary.csv`: High-level key performance indicators of the dataset.
- `requirements.txt`: List of Python dependencies required to run the notebook.

## 📈 Key Performance Indicators (KPIs)
Based on the cleaned dataset of **947,752 orders**:
- **Total Revenue**: ₹538,545,961
- **Avg Order Value**: ₹568.24
- **Avg Delivery Time**: 16.47 Minutes
- **Avg Distance**: 7.75 Km
- **Avg Customer Rating**: 3.04
- **Discount Usage Rate**: 40.1%
- **Premium Buyer Share**: 25.0%
- **Lazy Local Buyer Share**: 30.0%

## 🧑‍🤝‍🧑 Customer Segments Identified
Using K-Means Clustering (evaluated with Silhouette Score 0.1781) and advanced feature engineering, we identified **7 distinct customer segments**:

| Segment Name | Customer Share | Revenue Share | Key Behavior | Actionable Strategy |
|--------------|----------------|---------------|--------------|---------------------|
| **Satisfied Loyal Customer** | 15.25% | 19.63% | High avg order value (₹731), high ratings, low discount usage. | **High Priority** - Enroll in Loyalty Programs. |
| **Lazy Local Buyer 1** | 15.23% | 22.68% | Very high order value (₹846), short distances (3.31 km), highly convenience-driven. | **Medium Priority** - Upsell & Premium Subscriptions. |
| **Lazy Local Buyer 2** | 18.15% | 13.03% | Moderate order value, zero discount usage, short distance. | **Medium Priority** - Loyalty Programs. |
| **Lazy Local Buyer 3** | 4.67% | 4.06% | Extremely short distances (1.02 km), moderate order value. | **Medium Priority** - Loyalty Programs. |
| **Discount Hunter 1** | 15.18% | 16.52% | 100% discount usage rate, good order value. | **Monitor** - Discount Rationalization. |
| **Discount Hunter 2** | 13.48% | 12.44% | 100% discount usage rate, longer delivery times. | **Monitor** - Discount Rationalization. |
| **Long-Distance Dependent** | 18.03% | 11.64% | Longest distance (11.92 km), zero discount usage, lower order values. | **Monitor** - Loyalty Programs. |

## 🛠️ Methodology & Tech Stack
**Techniques Used:** 
- K-Means Clustering, DBSCAN, Agglomerative (Hierarchical) Clustering
- Principal Component Analysis (PCA)
- Advanced Feature Engineering (Convenience Score, Premium Score, etc.)
- Model Evaluation Metrics (Silhouette Score, Davies-Bouldin, Calinski-Harabasz)

**Tools & Libraries:** 
- **Python**
- **Data Manipulation:** Pandas, Numpy
- **Machine Learning:** Scikit-learn, Scipy
- **Visualization:** Matplotlib, Seaborn, Plotly

## 💡 Business Recommendations
1. **Focus on "Lazy Local Buyers"**: With a 30% combined share of customers representing a substantial revenue chunk, emphasizing hyper-local convenience over heavy discounting will maximize margins.
2. **Rationalize Discounts**: Approximately 28% of the customer base are strictly "Discount Hunters". Transitioning them towards value-add services or placing conditions on discounts can prevent revenue leakage.
3. **Targeted Loyalty Programs**: The "Satisfied Loyal Customer" segment contributes nearly 20% of the revenue but only 15% of the base. Expanding loyalty offerings to them provides the highest retention ROI.

## 🚀 Installation & Usage
To run the Jupyter Notebook locally and reproduce the analysis:
1. Clone the repository:
   ```bash
   git clone https://github.com/Devaguru11/Convenience-Driven-Customer-Segmentation-in-Quick-Commerce.git
   cd Convenience-Driven-Customer-Segmentation-in-Quick-Commerce
   ```
2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Open and run the notebook:
   ```bash
   jupyter notebook Quick_Commerce_Customer_Segmentation.ipynb
   ```

To view the dashboard, simply open `dashboard.html` in any modern web browser.
