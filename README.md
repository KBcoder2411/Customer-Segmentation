RFM Customer Segmentation Using K-Means Clustering
This project implements RFM (Recency, Frequency, Monetary) analysis to segment customers based on their purchasing behavior and applies K-Means clustering for customer segmentation. This approach is widely used in marketing to identify different customer groups for targeted campaigns.


Requirements
To run the project, ensure you have the following dependencies installed:

numpy
pandas
matplotlib
seaborn
scikit-learn
pickle


Dataset
The dataset used for this project is an online retail transaction dataset. It contains the following columns:

InvoiceNo: Invoice number
StockCode: Product code
Description: Product description
Quantity: The quantity of products purchased
InvoiceDate: Date of the invoice
UnitPrice: Unit price of the product
CustomerID: Unique customer identifier
Country: The country of the customer
Data Preprocessing
Data Cleaning:

Missing values are removed.
A new column Amount is calculated as Quantity * UnitPrice.
RFM Calculation:

Recency: The number of days since the customer's last purchase.
Frequency: The total number of transactions made by the customer.
Monetary: The total amount spent by the customer.
Outlier Treatment:

Outliers in Amount, Recency, and Frequency are treated using the interquartile range (IQR) method to ensure robust clustering.
K-Means Clustering
The project applies K-Means Clustering to group customers into similar segments based on their RFM scores. The dataset is scaled using StandardScaler before applying K-Means.

Model Training
The K-Means model is trained using 3 clusters (you can change the number of clusters based on your analysis):



Customer Segmentation
Customers are categorized into the following segments based on RFM values:

Best Customers: High-value, frequent, and recent customers.
Loyal Customers: Frequent customers who don’t spend as much.
At-Risk Customers: Customers who haven’t purchased recently and are at risk of churning.
New/Low-Value Customers: New customers or those with low engagement.



Visualization
The project visualizes customer behavior using Seaborn to plot box plots of Recency, Frequency, and Monetary metrics.



Future Work
Model Optimization: Experiment with different numbers of clusters using methods like the Elbow Method.
Personalized Marketing: Use the segmented customer data for creating personalized marketing strategies.
Dynamic RFM Analysis: Automate the segmentation process for real-time RFM analysis and customer tracking.


Conclusion
This project demonstrates the use of RFM analysis combined with K-Means clustering to identify different customer segments. It provides a framework for understanding customer behavior and making data-driven marketing decisions.
