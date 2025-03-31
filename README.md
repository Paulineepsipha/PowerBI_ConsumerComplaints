# PowerBI_ConsumerComplaints
Power BI project analyzing Bank of America consumer complaints (2017-2023). It explores trends, common issues, seasonal patterns, resolution methods, and untimely responses using CFPB data. Includes interactive visualizations for insights.

# Consumer Complaints Dashboard

### Dashboard Link : ----

## Problem Statement

Analysis of Consumer Complaints on Financial Products & Services:
	The dataset contains consumer complaints related to financial products and services for Bank of America from 2017 to 2023. These complaints, submitted to the Consumer Financial Protection Bureau (CFPB), include details such as the complaint date, product, issue, and the company’s response. The goal of this analysis is to derive actionable insights from these consumer complaints to improve customer experience, enhance the company's response mechanisms, and identify key patterns in consumer dissatisfaction.

### Analysis Questions:
	
1. Do consumer complaints show any seasonal patterns?
	Investigate whether consumer complaints show any seasonal patterns over the years. This can help identify periods of high complaint volumes and potentially indicate systemic issues or seasonal spikes in customer dissatisfaction.

2. Which products present the most complaints? What are its most common issues?
	Determine which financial products (e.g., credit cards, loans, mortgages, etc.) are the most frequently complained about. Additionally, explore the most common issues associated with each product to highlight areas for product improvement and customer service focus.
	
3. How are complaints typically resolved?
	Analyze how complaints are typically resolved. This includes examining the company’s response times and categorizing the resolution outcomes (e.g., timely response, no response, issue resolved, or issue pending). Understanding this can inform improvements in the company's resolution process.
	
4. Can you learn anything from the complaints with untimely responses?
	Investigate complaints that received untimely responses from the company. Understanding why certain complaints had delayed responses and identifying common patterns in these cases can provide valuable insights for improving response times and customer satisfaction.

### Steps Followed for Data Transformation in Power BI

- Step 1: Load Data
		Loaded data from an Excel file using the Excel.Workbook function to access the dataset.
		Located and selected the "Data" sheet from the Excel file to begin working with the data.
- Step 2 : Promote Headers
		Promoted the first row of the dataset as column headers using the Table. PromoteHeaders function to ensure the data is correctly labeled for further transformations.
- Step 3 : Change Data Types
		Applied the Table.TransformColumnTypes function to ensure all columns had the correct data types, such as:
			-Complaint ID, State, Product, Sub-product, Issue, Sub-issue, Company public response, Company response to consumer, and Timely response? as Text.
			-Date submitted, Date received as Date.
- Step 4 : Handle Missing Values (Null Handling)
		Replaced null values in multiple columns to handle missing data:
			Replaced null in Company public response with "No response given".
			Replaced null in Timely response? with "Still in progress".
			Replaced null in Sub-issue with "Not specified".
			Replaced null in Sub-product with "Not specified".
- Step 5 : Output Final Data
		The final dataset after transformations was returned as "Replaced Value3" for further analysis or reporting.
