
# 🛒 Kirana Register

A mobile-first shop management app built for small kirana store owners. Manage stock, record sales with a multi-item cart, track expenses, and view daily summaries — all from your phone, with no internet required.

---

## Table of Contents

- Features
- Tech Stack
- Getting Started
- Project Structure
- Data Storage
- How to Use
- Mobile Usage
- Future Improvements
- License

---

## Features

**Stock Tab**
View all items with name, category, unit, quantity, buy price, and sell price. Set a reorder level for each item. Automatic low stock alert highlights items in red when quantity falls below reorder level. Add new items and delete existing ones. Stock updates automatically after every sale.

**Sales Tab**
Multi-item cart system — select multiple items in a single flow. Search bar to quickly filter items by name. Checkbox to select or deselect items. Plus and minus buttons to set quantity per item. Auto price fill from stock when an item is selected. Bill preview shows all items and total before saving. Add customer name and date to each bill. One-click bill save with automatic stock deduction. View past bills and share them via WhatsApp or clipboard.

**Expense Tab**
Record daily expenses such as electricity, rent, and salary. Select a category for each entry. All past expenses are listed with date and amount. Delete any entry with confirmation.

**Summary Tab**
View total sales, total expenses, net profit, and total stock items in one place. Reorder alert list shows which items are running low and how many are left.

---

## Tech Stack

- React — UI framework
- JavaScript ES6 — application logic and calculations
- CSS-in-JS Inline Styles — mobile-friendly styling without external libraries
- localStorage — offline data persistence in the browser
- Web Share API — native share sheet on mobile for WhatsApp and SMS
- Clipboard API — fallback for devices that do not support the Share API

---

## Project Structure

kirana-register/
├── public/
│ └── index.html
├── src/
│ ├── App.jsx
│ └── index.js
├── package.json
└── README.md

---

## Data Storage

This app uses an offline-first architecture. No backend or internet connection is required. All data is stored in the browser's localStorage.

localStorage Keys:
- kirana_stock2 — Stock items
- kirana_sales2 — Bills and sales records
- kirana_expenses2 — Expense entries

Stock item example:
{ "id": 123, "name": "Aata (5kg)", "category": "Grocery", "qty": 20, "unit": "Bag", "buyPrice": 180, "sellPrice": 210, "reorder": 5 }

Bill example:
{ "id": 124, "date": "2026-06-18", "customer": "Ramesh Ji", "items": [{ "name": "Aata (5kg)", "qty": 2, "price": 210, "total": 420 }], "grandTotal": 420 }

Warning: Clearing browser data will permanently delete all records. Use the Share button regularly to export your data.

---

## How to Use

**Add a New Stock Item**
1. Open the Stock tab
2. Tap the Add New Item button
3. Fill in name, category, quantity, unit, buy price, sell price, and reorder level
4. Tap Save

**Create a Bill**
1. Open the Sales tab
2. Search for items or browse the list
3. Tap the checkbox to select items
4. Use plus and minus buttons to set quantity for each item
5. Tap the blue Bill bar at the top
6. Confirm customer name and date
7. Tap Save Bill — stock will be deducted automatically
8. Share the bill via WhatsApp

**Record an Expense**
1. Open the Expense tab
2. Tap Add New Expense
3. Fill in date, description, category, and amount
4. Tap Save

---

## Mobile Usage

This app is designed for phone use. For the best experience open it in Chrome on Android. Tap the browser menu and select Add to Home Screen. The app will appear as an icon on your home screen and feel like a native app.

---

## Future Improvements

- Udhaar Khata — customer-wise credit tracking
- PWA support — installable app with offline mode
- Google Sheets sync via Apps Script
- Monthly and weekly reports with date filters
- Barcode scanner for fast billing
- GST invoice generation
- Firebase or MongoDB backend for multi-device sync
- Customer management with purchase history
- Product image support

---

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Open a Pull Request

Bug reports and feature suggestions are welcome via GitHub Issues.

---

## License

MIT License — free to use, modify, and distribute.
Copyright (c) 2026
