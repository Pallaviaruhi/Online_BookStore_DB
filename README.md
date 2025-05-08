# Online_BookStore_DB
```markdown
# Online Bookstore Database: Insights & Analysis  
**A SQL-based database system for managing books, customers, and orders, with automated inventory updates and sales analytics.**  

---

## 📊 Key Insights from Data Analysis  

### 1. **Sales Trends**  
- **Monthly Revenue Peaks**:  
  - Highest revenue in **May** ($8,288.07) and lowest in **June** ($3,991.68).  
  - *Action*: Run promotions during low-demand months (e.g., June) to boost sales.  

- **Top-Performing Genres**:  
  | Genre           | Total Revenue   |  
  |------------------|-----------------|  
  | Romance          | $13,086.98      |  
  | Mystery          | $12,788.45      |  
  | Science Fiction  | $11,770.51      |  
  - *Insight*: Romance and Mystery genres drive 60% of total revenue.  

---

### 2. **Customer Behavior**  
- **Geographic Distribution**:  
  - Top countries: **Cuba** (7 customers), **Micronesia** (6), **Zimbabwe** (6).  
  - *Opportunity*: Target localized marketing campaigns in these regions.  

- **Repeat Customers**:  
  - **27.8%** of customers placed more than one order.  
  - *Top Spender*: Kim Turner ($1,398.90 total).  
  - *Recommendation*: Introduce a loyalty program for repeat buyers.  

---

### 3. **Inventory Management**  
- **Low-Stock Alerts**:  
  | Title                              | Stock Remaining |  
  |------------------------------------|-----------------|  
  | Networked Systemic Implementation  | 0               |  
  | Advanced Encompassing Implementation | 2              |  
  - *Action*: Prioritize restocking for books with stock ≤ 2 units.  

- **Stock Accuracy**:  
  - The trigger `trg_UpdateStock` ensures real-time stock updates after orders.  

---

### 4. **Author Performance**  
- **Top Authors by Sales**:  
  | Author             | Books Sold |  
  |--------------------|------------|  
  | Patrick Contreras  | 28         |  
  | Melissa Taylor     | 27         |  
  - *Strategy*: Highlight bestselling authors on the platform’s homepage.  

---

## 🚀 Business Recommendations  
1. **Promote Underperforming Genres**:  
   - Fiction accounts for only 9.6% of revenue despite having the most titles.  
   - Bundle Fiction books with top genres (e.g., "Buy Fiction + Mystery at 15% off").  

2. **Restock Critical Titles**:  
   - Use the `Low-Stock Alerts` query to automate purchase orders for books like *"Networked Systemic Implementation"*.  

3. **Loyalty Program**:  
   - Reward top 5 customers (e.g., Kim Turner, Jonathon Strickland) with exclusive discounts.  

4. **Seasonal Campaigns**:  
   - Capitalize on high-revenue months (May, November) with themed sales.  

---

## 🛠️ How to Use  
### Generate Monthly Sales Report:  
```sql  
EXEC usp_GenerateMonthlyReport @Month = 11, @Year = 2023;  
```  
**Sample Output**:  
| Genre          | Revenue   | Units Sold |  
|----------------|-----------|------------|  
| Mystery        | $1,181.04 | 44         |  
| Romance        | $612.21   | 18         |  

---

## 📁 Repository Structure  
```  
OnlineBookstore/  
├── Data/                 # CSV files for Books, Customers, Orders  
├── Triggers/             # Automated stock update logic 
├── StoredProcedures/     # Monthly sales report generator  
└── Queries/              # SQL scripts for analysis    
```  

---

## 🔮 Future Enhancements  
- Integrate **age demographics** for personalized recommendations.  
- Add **dynamic pricing** logic for low-demand genres.  
- Develop a **web dashboard** for real-time analytics.  

---

 
