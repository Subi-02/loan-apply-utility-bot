🛠️ Loan Application Utility Bot – UiPath
📄 Overview
This UiPath Utility Bot automates the end-to-end process of loan application form submission using data from an Excel file. The bot performs the following actions:

Reads applicant data from an Excel file (using Workbook Read Range).

Opens a loan application website in a browser.

Inputs each applicant’s data into the form.

Submits the application and retrieves loan rate and eligibility information.

Updates the original Excel file with the response.

Renames the processed file with a timestamp for future reference.

🧰 Technologies Used
UiPath Studio

UiPath.UIAutomation.Activities

UiPath.System.Activities

Excel (via Workbook activities, not Excel Application Scope)

Web browser (preferably Chrome or Edge)

📁 Folder Structure
css
Copy
Edit
LoanApplicationUtilityBot/
├── Main.xaml
├── Input/
│   └── LoanData.xlsx
├── Output/
│   └── Processed_LoanData_YYYYMMDD_HHMMSS.xlsx
├── Screenshots/
│   └── (Optional - screenshots for documentation)
├── README.md
📌 Prerequisites
UiPath Studio installed

Chrome/Edge browser with UiPath browser extension

Excel installed (optional, since using Workbook activities)

Valid Excel file in Input/ folder with required columns

📥 Input Format
The Excel file must be placed inside the Input/ folder and should include columns like:

Name

Age

Income

LoanAmount

LoanTenure

🔁 Process Flow
Read Excel File: Reads data from LoanData.xlsx using Workbook Read Range.

Browser Automation:

Launches browser and navigates to the loan application website.

Loops through each row to fill in the application form.

Submission & Data Retrieval:

Clicks the "Submit" button.

Waits for and extracts the loan rate and eligibility result.

Excel Update:

Writes the results back to the corresponding row in the same file.

File Rename:

Renames the file with a timestamp and moves it to the Output/ folder.

✅ Output
A processed Excel file renamed to:

Copy
Edit
Processed_LoanData_YYYYMMDD_HHMMSS.xlsx
It will include additional columns like:

LoanRate

EligibilityStatus

🧪 Testing & Validation
Test with a small number of entries initially.

Ensure consistent element selectors in the web form.

Use logs and message boxes during development for debugging.

📌 Notes
All data is processed sequentially.

Web form changes may require selector updates.

Error handling and retry scope are recommended for production-grade bots.
