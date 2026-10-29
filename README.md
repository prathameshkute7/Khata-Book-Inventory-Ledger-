📒 Khata Book App – Detailed Project Description

🟦 1. What is this Project?

Khata Book is a single-file web application used for managing a small shop's credit ledger (Udhaar–Jama).

A shopkeeper can record:

🟢 Customer details
🔵 Products taken on credit
🟠 Payments received
🔴 Outstanding balance

It is a digital version of the traditional paper Khata notebook. The interface uses a white ledger-page design with a red margin line to give it a familiar notebook feel.

💻 2. Technology Stack
Technology	Purpose
🟧 HTML	Structure of the application
🟦 CSS	Styling and responsive design
🟨 JavaScript	Application logic and calculations
🟩 SheetJS	Reading Excel and CSV files
🟪 localStorage	Saving data in the browser
🔤 Google Fonts	Baloo 2 and Hind fonts

Note: The application has no backend, database, or login system. All data is stored locally in the user's browser.

⭐ 3. Main Features
👤 Customer Management
Add new customers
Edit customer details
Delete customers
Optional phone number
Search customers
Display balance beside each customer name
🛒 Credit Purchase

Record:

Date
Item
Quantity
Unit
Rate
Total amount
💰 Payment Received

Record:

Date
Payment amount
Payment note such as Cash / UPI
🧮 Automatic Calculation

The application automatically calculates:

Amount = Quantity × Rate

Example:

5 kg Rice × ₹60 = ₹300

📅 4. Monthly View

The application provides a monthly ledger view.

Using the ‹ Previous and Next › buttons, the shopkeeper can switch between months.

Each month displays:

Total credit sales
Total payments
Previous balance
Current balance
Customer entries
📊 5. Balance Calculation

The balance is calculated using:

Balance Due = Previous Balance + Purchases − Payments

🔴 Positive Balance: Customer still has to pay.

🟢 Negative Balance: Customer has paid extra, shown as Advance.

The previous month's balance automatically carries forward to the next month.

📁 6. Excel Upload

The application supports importing customer and product information from:

.xlsx
.xls
.csv

Supported columns include:

Type | Customer Name | Phone | Product Name | Rate

Duplicate customers with the same name are automatically skipped.

🔐 7. Backup & Restore

Users can create a JSON backup containing all application data.

The backup can be:

📋 Copied
💾 Saved safely
📥 Pasted back to restore data

There is also an option to Delete All Data.

🧪 8. Demo Data

When the application is empty, the Load Demo Data option creates 4 sample customers so that users can understand how the application works.

🗂️ 9. Data Structure

The application stores two main types of data:

Customers

ID
Name
Phone

Entries

Purchase entries
Payment entries

Each entry contains a Customer ID (cid) that connects the transaction with the correct customer.

🖥️ 10. Main Screens
🏠 Overview / Home

Displays:

Monthly credit sales
Payments received
Total pending amount
Customer list
Customer balances

Customers with higher outstanding dues are displayed first.

👤 Customer Detail

Displays:

Previous balance
Current purchases
Payments
Final balance
Monthly transaction list
Items bought summary
Add Purchase form
Add Payment form
🪟 Modals

The application includes:

New Customer
Edit Customer
Delete Confirmation
Backup / Restore
🎨 11. UI/UX Features

📱 Responsive Design
Works on desktop and mobile devices.

🌙 Dark Mode
Automatically follows the device's theme.

♿ Accessibility
Includes keyboard support, focus outlines, ARIA labels and live announcements.

🛡️ XSS Protection
User-entered information is escaped before being displayed.

🇮🇳 Indian Number Format
Uses ₹ and Indian number formatting such as:

₹1,25,000

⚠️ 12. Current Issues

🔴 Hardcoded Date
The application currently uses 29 September 2026 instead of the actual date. Therefore, October entries cannot be created properly.

🔴 Products Not Saved
Imported products are stored only temporarily and disappear after refreshing the page.

🔴 Excel Upload Issue
After Restore or Delete All, Excel uploads may use outdated store data until the page is refreshed.

🔴 No Entry Editing
Existing entries can only be deleted and added again.

🔴 Backup is Copy-Paste Only
There is currently no direct JSON file download/upload option.

🔴 Internet Dependency
SheetJS and Google Fonts are loaded from CDNs, so some features do not work completely offline.

🚀 13. Future Improvements

The project can be improved by adding:

🟢 Automatic Date & Month Detection

🟢 Product Management
Add, edit and delete products with saved rates.

🟢 Edit Transaction
Allow users to directly modify existing purchases and payments.

🟢 WhatsApp / SMS Reminders
Send payment reminders to customers.

🟢 PDF / Excel Export
Generate printable customer statements and reports.

🟢 Downloadable Backup
Download and upload .json backup files.

🟢 Cloud Synchronization
Use Firebase or Supabase to access data across multiple devices.

🟢 Hindi / English Language Toggle

🟢 Charts & Reports
Monthly sales, payments and outstanding customer balances can be shown using charts.

🎯 Project Summary

Khata Book is a simple and user-friendly digital ledger application designed for small shopkeepers. It replaces the traditional paper-based Udhaar–Jama Khata with a browser-based system that provides customer management, transaction tracking, automatic balance calculation, monthly records, Excel import and backup/restore functionality.
