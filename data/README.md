# Data Folder

`financial_statements.hyper` is the Tableau extract embedded inside the original packaged `.twbx` workbook.

The workbook metadata shows that the original source was an Excel `.xls` file with two source sheets:

- **Balance Sheet Data**
- **Income Statement Data**

The original Excel file itself was not packaged in the `.twbx`, but the Hyper extract contains the data Tableau uses to render the workbook. Therefore, keeping the `.hyper` file in this repository preserves the project data even when the original Excel workbook is no longer available.

If you later obtain the original Excel file, you can optionally add it here as `financial_statements_source.xls` or convert the sheets to CSV for easier viewing directly on GitHub.
