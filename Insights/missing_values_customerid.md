# Missing Value Analysis: CustomerID

## Summary
During the exploratory data analysis (EDA) phase, we identified a significant amount of missing values in the `CustomerID` column. I found that 24% of the data has missing CustomerID values. Rather than simply treating it as "missing data," I explored deeper to understand what might be causing this and how it impacts the analysis. This report outlines the findings, insights, and implications of these missing values on the analysis.

## Key Findings
1. **Total Missing Values**: The `CustomerID` column has **135,080 missing values**, which is a substantial portion of the dataset.
2. **Missing Values by Country**:
   - The proportion of missing values varies across different countries.
   - **Hong Kong** has **100% missing CustomerID**, while other countries like the United Kingdom and Israel also show notable missing rates.
3. **Relationship with InvoiceNo**:
   - We found that invoices with missing `CustomerID` are linked to **3,710 unique InvoiceNo entries**.
   - This suggests that certain transactions systematically lack customer identification.
4. **Potential Reasons for Missing Values**:
   - **Guest Checkouts or Unregistered Customers**: Some purchases might have been made without customer registration.
   - **Bulk/Wholesale Orders**: Certain orders, especially those categorized under `Unspecified` countries, may represent bulk purchases that don’t require customer tracking.
   - **System Errors**: Some data might be missing due to technical issues in data recording.

## Implications
- **Impact on Customer Segmentation**: Since CustomerID is crucial for identifying repeat customers, the missing values limit our ability to perform customer behavior analysis.
- **Sales Trend Analysis**: If a large portion of sales come from transactions with missing CustomerID, we must reconsider whether customer-based segmentation is necessary for our analysis.
- **Alternative Approaches**:
  - Proceed with **invoice-level** analysis instead of customer-level analysis.
  - Investigate whether missing values correlate with specific **products, seasons, or discount offers**.

## Next Steps
- Given the high proportion of missing values, we will **conduct sales analysis without relying on CustomerID**.
- The missing value patterns and insights will be documented in the portfolio to justify the decision to exclude customer-level analysis.


