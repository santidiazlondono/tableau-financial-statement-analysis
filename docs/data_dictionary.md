# Data Dictionary

The field definitions below were recovered from the Tableau workbook metadata.

## Balance Sheet Data

Original source range metadata: `A1:AG524:no:A1:AG524:0`

| Field | Data Type |
|---|---|
| Ticker | string |
| Name | string |
| Industry | string |
| Year | integer |
| Financial Statement | string |
| Cash | integer |
| Short Term Investment Cash | integer |
| Cash & Short Term Investments | integer |
| Accounts Receivables | integer |
| Inventories | integer |
| Other Current Assets | integer |
| Total Current Assets | integer |
| Gross Property, Plant and Equipment | integer |
| Total Depreciation | integer |
| Intangible Assets | integer |
| Total Other Assets | integer |
| Total Assets | integer |
| Accounts Payable | integer |
| Short Term Debt | integer |
| Accrued Expenses (Liability) | integer |
| Other Current Liabilities | integer |
| Other Liabilities | integer |
| Long Term Debt | integer |
| Deferred Taxes (Liability) | integer |
| Other Liabilities 1 | integer |
| Total Liabilities | integer |
| Minority Interest (Equity) | integer |
| Preferred Stock (Equity) | integer |
| Common Equity | integer |
| Total Shareholder Equity | integer |
| Common Shares Outstanding | integer |
| Prepaid Expenses | integer |
| Cash Due From Banks (Asset) | integer |

## Income Statement Data

Original source range metadata: `A1:AL517:no:A1:AL517:0`

| Field | Data Type |
|---|---|
| Ticker | string |
| Year | integer |
| Financial Statement | string |
| Net Revenues | integer |
| Cost of Goods Sold | integer |
| Depreciation And Amortization Expense | integer |
| Gross Income | integer |
| General Expenses | integer |
| Research And Development Expense | integer |
| Total Operating Expenses | integer |
| Operating Income | integer |
| Extraordinary Credit | string |
| Extraordinary Charge | string |
| Interest Expense On Debt | integer |
| Other Non-Operating Expenses | integer |
| Pre-Tax Income | integer |
| Income Tax Expense | integer |
| Net Income | integer |
| Shares To Calculate EPS | integer |
| Shares To Calculate EPS Diluted | integer |
| Earnings Per Share | real |
| Diluted Earnings Per share | real |
| Discontinued Operations | integer |
| Extraordinary Items | integer |
| Minority Interest | integer |
| Pre-Tax Equity Earnings | integer |
| Equity In Earnings | integer |
| Other Operating Expenses | integer |
| Preferred Dividend | integer |
| Other Operating Income | integer |
| Loan Loss Provision | integer |
| Interest Expense Total | integer |
| Interest Income | integer |
| Non-Interest Income Total | integer |
| Non-Interest Expense | integer |
| Underwriting Expenses | integer |
| Premiums Earned | integer |
| Claim And Loss | integer |

## Calculated Fields

| Calculated Field | Tableau Formula |
|---|---|
| Roe for industry | `{Fixed[Industry],[Year]: MEDIAN([Net Income]/[Total Shareholder Equity])}` |
| profit margin for industry | `{FIXED [Industry],[Year]: MEDIAN([Net Income]/[Net Revenues])}` |
| Asset turnover for industry | `{FIXED [Industry],[Year]:MEDIAN([Net Revenues]/[Total Assets])}` |
| financial leverage for industry | `{FIXED [Industry],[Year]:MEDIAN([Total Assets]/[Total Shareholder Equity])}` |
| net income for industry | `{FIXED [Industry],[Year]:MEDIAN([Net Income])}` |
| total shareholder's equity for indsutry  | `{FIXED [Industry],[Year]:MEDIAN([Total Shareholder Equity])}` |
| net revenue for industry | `{FIXED [Industry],[Year]:MEDIAN([Net Revenues])}` |
| total assets for industry | `{FIXED [Industry],[Year]:MEDIAN([Total Assets])}` |
| ROE(income/Equity) | `[Net Income]/[Total Shareholder Equity]` |
| Profit Margin(income/sales) | `[Net Income]/[Net Revenues]` |
| Asset turnover(sales/assets) | `[Net Revenues]/[Total Assets]` |
| financial leverage(assets/equity) | `[Total Assets]/[Total Shareholder Equity]` |