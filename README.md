# Online Retail Sales Analysis

**Online Retail Sales Analysis** is a data analytics practice project investigating the sales performance, product demand and customer purchasing behaviour of a UK-based online retailer. The project uses Python and Pandas for data preparation and exploratory analysis, followed by Power BI to communicate findings through an interactive dashboard.

The purpose is to identify patterns that could support business decisions while developing practical skills in descriptive statistics, data visualisation and business intelligence reporting.

## Dataset Content

The dataset was obtained from the **UCI Machine Learning Repository**:

- **Source:** [Online Retail — UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/352/online+retail)
- **Citation:** Chen, D. (2015). *Online Retail* [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C5BW33
- **Period covered:** 1 December 2010 to 9 December 2011
- **Records:** 541,909
- **Context:** Transactions from a UK-based online retailer selling mainly gift products, including sales to wholesalers.

### Dataset Attributes

| Column | Description |
|---|---|
| `InvoiceNo` | Invoice identifier. Numbers beginning with `C` indicate cancellations. |
| `StockCode` | Product identifier. |
| `Description` | Product description. |
| `Quantity` | Quantity of each product recorded on the transaction line. |
| `InvoiceDate` | Date and time of the transaction. |
| `UnitPrice` | Unit price in pounds sterling (£). |
| `CustomerID` | Customer identifier. |
| `Country` | Country associated with the customer. |

The dataset does not include product costs or a profit field, so the project will investigate **sales revenue rather than profitability**. Revenue can be calculated from `Quantity × UnitPrice`, but the treatment of cancellations and returns must first be considered.

## Business Requirements

The retailer's management would like a clearer understanding of sales activity, product performance and customer purchasing patterns to identify potential areas for improvement.

### BR1 — Sales Revenue Performance

**Business requirement:** Investigate how sales revenue changes over time to identify trends, seasonal patterns and periods of stronger or weaker performance.

**Initial investigation:**
- Inspect `InvoiceDate`, `Quantity` and `UnitPrice`.
- Establish how cancelled and returned transactions should be treated.
- Calculate transaction-line revenue and aggregate results by month.
- Compare monthly revenue with order volumes.

**Potential visualisations:** Line charts for trends over time and bar charts for comparisons between periods.

### BR2 — Product and Geographic Performance

**Business requirement:** Identify which products and countries contribute most to sales revenue and which areas may warrant further investigation.

**Initial investigation:**
- Inspect `StockCode`, `Description` and `Country`.
- Group sales by product and country.
- Compare revenue, quantities sold and distinct order counts.
- Investigate high- and low-performing groups, accounting for differences in transaction volume.

**Potential visualisations:** Ranked bar charts and comparative summaries.

### BR3 — Customer Purchasing Behaviour

**Business requirement:** Investigate customer purchasing patterns to understand repeat purchasing, order values and concentration of sales among customers.

**Initial investigation:**
- Inspect `CustomerID`, `InvoiceNo` and `InvoiceDate`.
- Investigate missing customer identifiers before customer-level analysis.
- Calculate distinct customers, order frequency and average order value using clearly defined valid orders.
- Examine the distribution of purchasing frequency and revenue across customers.

**Potential visualisations:** Histograms, bar charts and time-based comparisons.

## Project Plan

As a post-bootcamp practice project, the analysis will follow a structured process while allowing independent decisions about cleaning, analytical methods and dashboard design.

1. **Ideation and Business Understanding** — Define the retailer's business questions and determine which available variables could answer them. Generative AI will be used as a learning and ideation aid, with suggestions reviewed rather than accepted automatically.
2. **Data Collection and Understanding** — Obtain the original Excel dataset from UCI, review its documentation and inspect the available columns.
3. **Data Preparation and ETL** — Use Python and Pandas to check data types, missing values, duplicates, cancellations, returns and unusual quantities or prices. Document cleaning decisions and export an analysis-ready dataset while retaining the original file.
4. **Exploratory Data Analysis (EDA)** — Use descriptive statistics, grouped summaries and appropriate plots to investigate the three business requirements. Explain why each method was selected and interpret findings in plain language.
5. **Power BI Dashboard Development** — Import the prepared data into Power BI, build relevant DAX measures and create interactive reports focused on the business requirements.
6. **Interpretation and Recommendations** — Summarise supported findings, identify limitations and suggest practical areas for further business investigation.
7. **Documentation** — Record the workflow, analytical choices, visualisations and results in this README as the project progresses.

## Initial Data Quality Considerations

Before calculating business metrics, the dataset will be inspected for:

- Missing values, particularly in `CustomerID` and `Description`.
- Duplicate rows and whether they represent errors or legitimate repeated transaction lines.
- Invoice numbers beginning with `C`, indicating cancellations.
- Negative, zero or unusually large quantities.
- Zero, negative or unusual unit prices.
- Correct date and numeric data types.

Records will not be removed solely because they appear unusual. Cleaning decisions will be based on the dataset documentation and their potential impact on business measures.

## Analysis Techniques Used

*To be completed after the exploratory analysis, including the reasons for selecting each technique and any limitations encountered.*

## Dashboard Design

*To be completed as the Power BI report is developed. Planned areas include revenue trends, product and country comparisons, and customer purchasing behaviour.*

## Findings and Conclusions

*To be completed after the analysis. Findings will distinguish observed patterns from unsupported causal claims.*

## Development Roadmap

*To be updated with challenges, solutions and new skills learned throughout the project.*

## Main Data Analysis Libraries and Tools

- **Python and Pandas** — Planned for data inspection, cleaning, transformation and aggregation.
- **Matplotlib and Seaborn** — Planned for exploratory data visualisations.
- **Power BI, Power Query and DAX** — Planned for interactive reporting, data modelling and measures.

## Credits

### Dataset

Chen, D. (2015). *Online Retail* [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C5BW33

### Generative AI

ChatGPT (OpenAI) was used to help develop the initial business scenario, business requirements and README structure. Any further AI assistance with analysis, code or interpretation will be documented as the project progresses. Analytical findings will be verified against the dataset.
