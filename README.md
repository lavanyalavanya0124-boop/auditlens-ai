# AuditLens AI — Travel Expense Auditing Demo

A front-end prototype for an employee travel expenditure auditing workflow. It is designed as a portfolio/demo project inspired by common travel-and-expense audit processes. It is **not SAP Concur**, is not affiliated with SAP, and does not connect to a real company system.

## Features
- Executive spend overview and KPI cards
- Expense claims table with search, status and risk filters
- Rule-based policy-limit checks and potential duplicate receipt detection
- Claim detail modal with demo auditor decision workflow
- Department/category/status analytics
- CSV import and CSV report export
- Responsive desktop and mobile layout
- Fictional sample records only

## Run the website locally
### Easiest method
1. Extract the ZIP file.
2. Open the `auditlens-ai-demo` folder.
3. Double-click `index.html` to open it in a browser.

If the browser blocks any CDN resources, run it with a local web server:
1. Install Python 3.
2. Open a terminal in this folder.
3. Run `python -m http.server 8000`
4. Open `http://localhost:8000` in your browser.

The Chart.js library is loaded from a CDN, so charts need internet access. The rest of the prototype is static HTML/CSS/JavaScript.

## Import CSV format
Required column names (case-insensitive):
`claim_id, employee_id, employee, department, merchant, category, date, amount, receipt_id, status`

Optional:
`policy_limit`

Use the **Import expenses** button and upload a CSV. The included sample CSV can be downloaded from the in-app import modal.

## Demo workflow
1. Review the overview dashboard.
2. Open **Expense claims** and search/filter records.
3. Open a claim to inspect its rule-based flags.
4. Change the demo status and add an auditor comment.
5. Open **Audit findings** to review potential exceptions.
6. Export claims or findings to CSV.

## Current limitations / production checklist
This is a browser-only prototype. Data and decisions stay in browser memory and reset when the page is refreshed. It does not perform OCR on receipts, use a real ML model, authenticate users, or integrate with SAP Concur.

For a production-ready system, add:
- Secure backend API (for example, FastAPI)
- Database (PostgreSQL/MySQL)
- Authentication and role-based access
- Server-side validation and audit logs
- Secure receipt storage and privacy controls
- Real OCR extraction and human verification
- Tested policy configuration and exception handling
- Approved SAP Concur API access and integration testing
- Automated tests, deployment, monitoring, and security review

## Suggested next steps
1. Finish the front-end demo and take screenshots.
2. Add a FastAPI backend and SQL database.
3. Add OCR as a separate service.
4. Add anomaly detection only after you have a suitable labelled or validated dataset.
5. Explore official SAP Concur developer documentation for approved API integration.
