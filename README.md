# 💳 Credit Card Customer Segmentation and Service Matrix Optimization

## 📌 Business Problem Context
AllLife Bank aims to significantly increase market penetration for its credit card segment in the upcoming fiscal financial year. To optimize execution, the marketing team requires automated, data driven customer personas to transition from generic advertisements to high conversion, personalized campaigns. 

Concurrently, market feedback reveals poor customer perception regarding the bank's customer support center. The operations team seeks to identify distinct interaction patterns across communication channels to upgrade their service delivery metrics.

**Objective:** Built an end to end **Unsupervised Machine Learning Pipeline** using **K-Means** and **Agglomerative Hierarchical Clustering** to isolate unique customer segments based on spending capacities, credit card volumes and operational contact channels (In person, Online, Phone Support).

---

## 📊 Feature Space and Behavioral Indicators
The model analyzes historical behavior across 660 active profiles (`Credit Card Customer Data.xlsx`):
* **`Avg_Credit_Limit`:** The baseline indicator of a customer's purchasing capacity.
* **`Total_Credit_Cards`:** Quantitative indicator of the customer's wallet share with the bank.
* **`Total_visits_bank`:** Traditional physical brick-and-mortar branch interactions.
* **`Total_visits_online`:** Digital platform engagement rates (App logins, web transactions).
* **`Total_calls_made`:** Customer center support dependencies.

---

## ⚙️ Clustering Architecture and Diagnostics
1. **Feature Engineering and Scaling:** Applied z-score normalization (`StandardScaler`) to smooth scale gaps between credit limit volumes and single digit visit metrics.
2. **K-Optimal Evaluation:** * **Elbow Method:** Monitored Within Cluster Sum of Squares (WCSS) drop offs across a range of cluster candidates.
   * **Silhouette Optimization:** Maximized cluster separation metrics, confirming an optimal global silhouette score of **0.57** at $K=3$.
3. **Algorithm Cross Validation:** Benchmarked $K$-Means centroids against **Agglomerative Hierarchical Clustering** using an average linkage distance matrix to verify structural segment stability.

---

## 🎯 Engineered Customer Archetypes ($K=3$ Solution)

The machine learning framework grouped AllLife Bank's consumer footprint into three highly distinct behavioral archetypes:

### 1. 🏢 Segment 0: The Traditional Mid Tier Consumer (*Count: 386 Customers*)
* **Profile:** Moderate Credit Capacity (~$33.7K Limit) holding 5–6 credit cards.
* **Channel Preference:** **In person banking dominant** (Avg. 3.5 physical bank visits per year). They rarely use online infrastructure (~0.98 online logins).
* **Actionable Recommendation:** Deploy physical point of sale branch materials. Transition this segment to basic digital services through guided branch support.

### 2. 📞 Segment 1: The Low Cap Support Dependent Consumer (*Count: 224 Customers*)
* **Profile:** Lower financial baseline (~$12.1K Limit) with minimal credit cards (2–3 cards max).
* **Channel Preference:** **Heavy Phone Support Dependencies** (Avg. 6.87 calls made yearly). 
* **Actionable Recommendation:** This segment drives the bank's poor support scores. Operations must fix root cause friction by deploying clear billing explanations and self service IVR/Chatbot options to deflect high call volumes.

### 3. 🚀 Segment 2: High Value Digital Power Users (*Count: 50 Customers*)
* **Profile:** Elite financial status (~$141K Avg. Credit Limit) holding 8–9 active credit cards.
* **Channel Preference:** **Purely Digital** (Avg. 10.9 online visits per year, virtually zero phone calls or branch visits).
* **Actionable Recommendation:** High margin asset pool. Target with premium tier upsells, exclusive cash back structures, app integrated spend analytics and premium lifestyle partnerships.

---

## 🛠️ Tech Stack & Core Libraries
* **Language Environment:** Python
* **Clustering Frameworks:** `scikit-learn` (`KMeans`, `AgglomerativeClustering`)
* **Evaluation & Scoring:** `scikit-learn` (`silhouette_score`)
* **Data Pipelines:** `pandas`, `numpy`
* **Statistical Graphics:** `matplotlib`, `seaborn`

---

## 🤝 Connect with Me
* **LinkedIn:** www.linkedin.com/in/yash-rane-275867156
* **GitHub Portfolio:** https://github.com/yash-rane-17
