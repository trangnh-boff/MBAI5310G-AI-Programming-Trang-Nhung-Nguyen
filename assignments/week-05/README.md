# Assignment 5: K-means Clustering for ProcurePro Office Supplies

## Business Problem
ProcurePro Office Supplies is a B2B procurement and office supply distribution business. The main business problem is supplier delivery uncertainty. Some purchase orders arrive on time, while others may be delayed because of supplier backorders, low past on-time performance, long delivery distance, urgent order pressure, seasonal demand, or previous supplier quality issues.

## Dataset
The dataset used for this assignment is the ProcurePro supplier delay risk dataset. Each row represents one purchase order placed with a supplier. The dataset includes supplier profile information, order characteristics, delivery conditions, supplier performance, risk indicators, and inventory context.

## Clustering Method
This assignment uses K-means clustering, which is an unsupervised learning method. The target variable was not used for training. Only numerical features were selected and scaled before applying K-means. The Elbow Method was used to help choose the number of clusters, and K = 3 was selected.

## Main Results
The K-means model identified three purchase order segments:

1. **High Delay Risk / Lower Supplier Reliability**  
   This segment includes orders connected to weaker supplier performance, such as lower past on-time rate and lower supplier rating.

2. **Moderate Risk / Low Inventory Buffer**  
   This segment includes orders with lower inventory buffer and stronger demand pressure.

3. **More Reliable but Long Distance Orders**  
   This segment includes orders connected to suppliers with stronger reliability, but longer delivery distance.

## Business Recommendation
ProcurePro should use the clusters to prioritize supplier follow-up, customer communication, and inventory planning. For lower reliability orders, the company should contact suppliers earlier and prepare backup suppliers. For low inventory buffer orders, ProcurePro should send earlier customer updates and encourage earlier reordering. For reliable but long-distance orders, the company should maintain strong supplier relationships while still monitoring shipping timelines.

## Repository Files
- `Assignment 5.ipynb` — completed Jupyter Notebook
- `procurepro_supplier_delay_risk_dataset.xlsx` — dataset used for the assignment
- `README.md` — project summary
