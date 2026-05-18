# MIS-311
**1. Overview**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This project analyzes the Supermarket Sale dataset, which captures transaction records from three primary branches in New York, Los Angeles, and Chicago. The dataset provides critical information regarding product categories, customer demographics, and sales metrics, enabling an in-depth evaluation of branch performance and consumer trends.
- Initial Dataset Size: 253 rows × 8 columns
- Final Dataset Size (after cleaning): 239 rows × 8 columns
- Missing Values:12 missing values were deleted because the data was incomplete, including one row that contained 2 missing values
  
**Columns:**
- sale_id: Unique sale transaction ID
- branch: Supermarket branch (A, B)
- city: City location (New York, Los Angeles, Chicago)
- customer_type: Member or Normal customer
- product_name: Name of product
- product _category: Product category (e.g., Fruits, Stationery, Beverages)
- quantity: Number of units sold
- total_price: Total sales value (USD)

**Data Sources**
  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The original source of the dataset is not clearly identified, but it appears to be sample supermarket transaction data created for learning and practice. The dataset is similar to sales data commonly used in retail systems and educational materials. Similar datasets can be found on these platforms:
- Kaggle: Supermarket and retail datasets for data analysis practice.
- UCI Machine Learning Repository: Business datasets used for academic learning and research.
- Open educational resources: Sample datasets for teaching statistics and business analytics.

**2. Data cleaning**

**2.1. Data Formatting**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;All columns were assigned suitable data types to maintain data accuracy and reduce calculation mistakes. Columns such as Sale_ID, Branch, City, Customer_Type, Product_Name, and Product_Category were formatted as Text because they contain categorical information. The Quantity column was set as Number with 0 decimal places, while Total_Price was formatted as Currency with 2 decimal places. Even though Sale_ID includes numbers, it was treated as Text since it is used as an identifier, not for calculations.

**2.2. Checked for missing values**

**Step 1:** Select all data → go to Home → Find & Select → Go To Special → Blanks.

Excel highlights all blank cells.

<img width="818" height="433" alt="image" src="https://github.com/user-attachments/assets/e3f3e751-81f1-4dbd-8748-c867e064d27e" />

_**Figure 1: Missing values (row 20 - column: quantity)**_

<img width="945" height="512" alt="image" src="https://github.com/user-attachments/assets/6c1fa2e4-224c-45bf-8c88-c7a277f70a9b" />

_**Figure 2: Missing values (row 30, 31, 32, 35 - column customer_type & product_category)**_

<img width="976" height="545" alt="image" src="https://github.com/user-attachments/assets/b4b24b27-429d-489b-83fe-43f4dd2792f0" />

_**Figure 3: Missing values (row 44, 49, 61 - column customer_type, product_category & quantity)**_

<img width="1014" height="612" alt="image" src="https://github.com/user-attachments/assets/ba8ab2db-e21d-449e-9013-d29a9ee1c384" />

_**Figure 4: Missing values (row 68, 87 - column product_category)**_

<img width="1037" height="200" alt="image" src="https://github.com/user-attachments/assets/61fd8d04-8db7-4cef-8992-28f1bc46c0fb" />

_**Figure 5: Missing value (row 99 - column product_category)**_

A total of 12 missing values were identified in the dataset across three columns. Missing entries were found in:
- quantity column: rows 20, 44, 61
- customer_type column: rows 31, 35, 44
- product_category column: rows 30, 32, 49, 68, 87, 99

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;These missing values represented incomplete sales information, such as unknown quantities, customer types, or product categories. Such missing data could reduce the accuracy of descriptive statistics and lead to biased insights.

**Step 2:** Delete rows that contain missing data (Right-click → Delete → Entire Row ).

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;A total of 12 missing values were found in important columns like quantity, customer_type, and product_category. These columns are necessary for analyzing sales and customer purchasing behavior. Using estimated values might affect the correctness of the results, so the incomplete records were removed to keep the dataset accurate and reliable for descriptive analysis.

**2.3. Checked for duplicate records**

**Step 1:** Select the whole table (ctrl A)

**Step 2:** Go to Data → Remove Duplicates.

**Step 3:** Tick all columns → OK.

<img width="1160" height="646" alt="image" src="https://github.com/user-attachments/assets/b75ddfec-0462-4418-aece-fff09c962e42" />

_**Figure 6: Duplicate values**_

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;After handling the missing data, the dataset was checked again to identify duplicate records by using Excel’s Remove Duplicates feature. As a result, 3 repeated rows were removed from the dataset. After the cleaning process, the dataset contains 239 records and 8 columns with complete and non-duplicated data, making it suitable for further analysis and visualization.

**3. Descriptive Statistics**

<img width="654" height="365" alt="image" src="https://github.com/user-attachments/assets/40d7eff4-1bec-450c-a1fb-f84fed81d9cf" />

_**Figure 7: Summary statistics**_

**Quantity**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Customers usually purchase around 10 items per transaction, showing a stable and moderate shopping pattern. This consistent buying behavior can help the supermarket predict product demand and manage inventory more efficiently.

**Total price**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The average spending per transaction is about USD 127, though some customers spend much higher amounts. This indicates the presence of high-value customers who contribute significantly to total revenue,a key group for targeted promotions or loyalty programs.

<img width="739" height="425" alt="image" src="https://github.com/user-attachments/assets/f5fb3549-3cf9-46fb-8b58-fd102c67cea0" />

_**Figure 8:  Box Plot of Total Price per Transaction**_

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The box plot presents the spread of total spending for each transaction. The median transaction value is about USD 106.59, while the mean is higher at USD 127.04, which indicates a slightly right-skewed distribution. Most transaction amounts are between USD 40 and USD 200, based on the interquartile range (IQR). The lowest transaction value is USD 2.18, and the highest is USD 427.14. This shows that most customers spend a moderate amount, while a small number of expensive purchases increase the average transaction value. In general, the distribution is consistent with the descriptive statistics results and shows differences in customer spending patterns. This information is useful for understanding customer behavior before analyzing deeper business insights.

<img width="749" height="474" alt="image" src="https://github.com/user-attachments/assets/9d913259-0a49-495b-8a7e-ff17bc29bde6" />

_**Figure 9: Distribution of quantity per transaction**_

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The histogram above shows how many products customers buy in one transaction. Most customers buy between 8 and 11 items, with around 55 transactions. Buying 1–4 items and 15–18 items is also common, with about 50–55 transactions. Only a smaller number of customers buy more than 18 items, with around 30 transactions. This means most customers make medium-sized purchases instead of very small or very large ones. Overall, the chart shows a fairly balanced buying pattern, so customer behavior is quite consistent. After understanding the overall distribution, the next step is to identify important business insights.

**3.1. Insight 1: Regional Revenue Performance (Based on Total Sales Revenue by Branch)**

<img width="807" height="524" alt="image" src="https://github.com/user-attachments/assets/360f28ab-3d0d-44f4-acae-2f10346e20d9" />

_**Figure 10: Total Sales Revenue by Branch**_

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The descriptive analysis shows that Branch A earned significantly higher revenue than Branch B, with total sales of USD 21,427 compared to USD 8,935. This means Branch A generated approximately 2.4 times more sales, indicating a much stronger business performance in that location. This disparity may stem from location advantages or higher customer demand; therefore, the company should consider prioritizing investment and expansion efforts in Branch A to further drive future revenue growth.

**3.2. Insight 2: Customer Contribution and Loyalty (Based on Total Sales by Customer Type)**

<img width="792" height="487" alt="image" src="https://github.com/user-attachments/assets/e7738f22-066c-49ce-9abf-285496edcbf0" />

_**Figure 11:Total Sales Distribution between Member and Normal Customer**_

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The pie chart illustrates that Member customers contributed 58% of total sales, while Normal customers accounted for 42%. This 16% gap indicates that Members play a more pivotal role in the supermarket's overall sales performance. The results suggest that membership programs effectively encourage higher spending, and management should focus on converting more Normal shoppers into Members through targeted promotions to sustain this high-value revenue stream.

**4. Conclusion**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;In conclusion, the exploratory data analysis of the Supermarket Sale dataset has successfully identified key drivers of revenue performance. The significant sales gap between Branch A and Branch B, combined with the strong contribution from Member customers (58%), highlights the importance of strategic location management and customer loyalty programs. These findings provide a solid foundation for management to optimize resource allocation and enhance membership marketing strategies to ensure sustainable growth in the future.

















