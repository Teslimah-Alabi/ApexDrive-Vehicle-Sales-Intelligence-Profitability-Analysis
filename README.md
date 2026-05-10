# ApexDrive-Vehicle-Sales-Intelligence-Profitability-Analysis

## Table of Content

* [Project Overview](#project-overview)

* [Tools and Methodology](#tools-and-methodology)

* [Business Questions](#business-questions)
  
* [Dataset Overview](#dataset-overview)
  
* [Analysis and Findings](#analysis-and-indings)
  
* [Business Insight](#business-insight)

* [Recommendations](#recommendations)

* [Limitations and Considerations](Limitations-and-Considerations)

### Project Overview
ApexDrive Auto Group is a multi-segment vehicle dealership operating within a competitive automotive market. The dealership’s portfolio spans luxury, utility, and environmentally sustainable vehicles, including electric, hybrid, diesel, and gasoline-powered models across multiple brands and pricing tiers. 

This analysis was conducted to evaluate the dealership’s commercial performance by examining revenue generation, premium vehicle sales, electric vehicle pricing behaviour, transaction segmentation, and salesperson productivity. 

### Tools and Methodology
The analysis was completed entirely in Microsoft Excel using structured formulas and conditional logic techniques. Several Excel functions were applied depending on the business requirement being addressed. These include:
*	SUM 
*	MAX 
*	XLOOKUP 
*	AVERAGEIFS 
*	IF 
*	AND 
*	COUNTIFS 
*	IFS 

### Business Questions
1. The CEO wants to understand the total revenue generated from all car sales combined.
2. The Head of the Luxury Car Division wants to know which car recorded the highest sale price.
3. The Sustainability Department wants to understand pricing trends for electric vehicles.
4. Management wants to categorize sales transactions based on value.
5. Management wants to evaluate individual salesperson performance.
6. The Finance Team wants to flag high-value electric car sales sold for over $40,000 for profitability tracking.

### Dataset Overview
The dataset consists of 1,000 rows and 9 columns. Each r representing vehicle sales activity within ApexDrive Auto Group. The dataset includes the following fields:
* Sales ID – Unique identifier assigned to each transaction
* Car Brand – Manufacturer of the vehicle sold
* Car Model – Specific model of the vehicle
* Fuel Type – Vehicle fuel category (Electric, Hybrid, Diesel, or Gasoline)
* Quantity Sold by Salesperson – Number of units sold by salesperson
* Sale Price – Selling price of each vehicle
* Revenue – Total revenue generated from each transaction
* Salesperson – Representative responsible for the sale
* Car Colour – Colour specification of the vehicle sold

### Analysis and Findings

#### 1.	Total Revenue from Sales
Revenue analysis was carried out by first creating a Revenue column using:
Revenue = Sale Price × Quantity Sold
The SUM function was then applied across the Revenue column to calculate the dealership’s total income from all transactions. This method ensures revenue reflects both vehicle price and sales volume rather than sale price alone.

##### Result:

Total Revenue: $1,603,568,042

<img width="507" height="151" alt="Screenshot 2026-05-09 220849" src="https://github.com/user-attachments/assets/2d2b8763-62bb-4ca3-976a-c805eae8ee20" />

#### 2.	Highest-Value Vehicle Sale
The MAX function was used to identify the highest sale price recorded in the dataset. To retrieve the corresponding vehicle, XLOOKUP was applied to return the associated car model linked to the maximum value.
This analysis helps identify the dealership’s highest-priced vehicle transaction and highlights premium-performing vehicle categories.

##### Result:
* Highest Sale Price: $99,948
* Car Model: Truck 

<img width="576" height="129" alt="Screenshot 2026-05-09 221458" src="https://github.com/user-attachments/assets/e9682776-c79e-4e56-a52b-31c4f6bafd44" />

#### 3.	Average Price of Electric Vehicles
To evaluate pricing trends within the electric vehicle segment, the AVERAGEIFS function was used to calculate the average selling price for only Electric vehicles. This analysis provides insight into the pricing strength and market positioning of electric vehicles within the dealership.

##### Result:
Average Selling Price of Electric Vehicles: $62,910

<img width="566" height="126" alt="Screenshot 2026-05-09 221529" src="https://github.com/user-attachments/assets/188fac16-d078-4552-91bf-4598dd1b106b" />
<img width="578" height="175" alt="Screenshot 2026-05-10 182552" src="https://github.com/user-attachments/assets/5936bc5a-e1c8-4c2c-bbe0-75bb1711434b" />

#### 4.	Sales Transaction Classification
Sales transactions were categorized into High-Value and Standard transactions using the IF function.
Transactions with sale prices (≥ $50,000) were classified as High-Value, while transactions (<  $50,000) were classified as Standard.

<img width="1920" height="931" alt="Screenshot 2026-05-09 221829" src="https://github.com/user-attachments/assets/a471eb01-3bd0-4f25-bd52-8e5fd7889945" />

#### 5. Salesperson Performance Classification
Salesperson performance evaluation was conducted using the IF and AND functions to classify representatives based on their sales performance.
The AND function was used to test multiple conditions within specific performance ranges, while the IF function applied the appropriate performance category based on the result of those conditions.
Classification thresholds:
*	31+ sales → Top Performer 
*	15–30 sales → Average 
*	Below 15 sales → Needs Improvement

<img width="1920" height="938" alt="Screenshot 2026-05-09 221904" src="https://github.com/user-attachments/assets/ac681bb7-e6c0-4900-9735-03f6b3cae61f" />

#### 6.	Identification of High-Value Electric Vehicle Transactions
To identify profitable electric vehicle transactions, the IFS and AND functions were combined to evaluate multiple conditions within the dataset.
The AND function was used to test whether transactions met all required conditions simultaneously:
*	Vehicle Type = Electric 
*	Sale Price > $40,000

The IFS function was then applied to classify and flag transactions that satisfied these conditions for profitability tracking and revenue analysis

<img width="1920" height="931" alt="Screenshot 2026-05-09 222004" src="https://github.com/user-attachments/assets/351e209a-5723-42bd-8725-ee052ba07cc2" />

### Business Insight
*	Total revenue generated from car sales amounts to $1,603,568,042
*	Truck is the car model with the highest sales price with $99,948 in revenue.
*	The average selling price of electric cars is $62,910
*	High-value transactions account for 68% of total sales, significantly exceeding standard sales, which highlights strong demand for premium-priced vehicles.
*	Electric vehicles sold above the $40,000 threshold represented a major share of electric vehicle transactions, reinforcing the dealership’s strong positioning within the premium electric vehicle market

### Recommendations
*	Increase investment in high-value vehicle categories such as trucks and electric vehicles to maximize revenue growth and profitability.
*	Strengthen electric vehicle inventory and sustainability initiatives to capitalize on rising demand and premium pricing opportunities.
*	Develop loyalty programs and personalized customer service strategies to encourage repeat purchases from high-value customers.
*	Implement performance-based incentives to improve salesperson productivity and maintain high sales performance

### Limitations and Considerations
Profitability classification for electric vehicles was based solely on sale price thresholds rather than actual profit margins, since operational costs and dealership expenses were not included in the dataset
Additionally, the analysis is based on a single transactional dataset and does not include historical sales trends or time-series analysis. As a result, seasonal patterns and long-term performance changes could not be evaluated.





