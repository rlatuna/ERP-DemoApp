# Northstar ERP DemoApp

A static, browser-based warehouse ERP prototype for customer order intake and fulfillment.

## Demo workflow

**Receiving → Picking → Packing → Shipping → Delivered**, with inventory control and order tracking available throughout.

## Features

- Role-specific navigation and sample views for Administrator, Purchasing, Customer Service, Warehouse, Logistics, Inventory Controller, and Management.
- Customer order creation and assignment.
- Tablet-first order quantities with SKU-specific automatic conversion to blisters.
- Example conversion: **111,000 tablets ÷ 10 tablets per blister = 11,100 blisters**.
- Product master, customer-to-SKU associations, barcode fields, stock ledger, reorder warnings, and bin locations.
- Order workflow advancement, carrier/tracking references, CSV exports, local JSON backup, and sample-data reset.
- Responsive desktop/tablet/mobile layout.
- GitHub Pages deployment workflow at `.github/workflows/pages.yml`.

## Run locally

Open `index.html` in a modern browser. No build step or third-party JavaScript dependency is required.

## Publish with GitHub Pages

1. In the repository, open **Settings → Pages**.
2. Under **Build and deployment**, choose **GitHub Actions** as the source.
3. Ensure the workflow `Deploy static ERP demo to GitHub Pages` is enabled.
4. Open **Actions** and wait for the **Deploy static ERP demo to GitHub Pages** workflow to complete successfully.
5. The expected site URL is https://rlatuna.github.io/ERP-DemoApp/ .

The workflow uses the official GitHub Pages actions to upload the repository root as a static site and deploy it.

## Demo data and limitations

- This is a **static demo**, not a production ERP.
- Role switching changes the visible demo pages and filters sample views; it is **not authentication or real access control**.
- Data changes are stored in the current browser's local storage. They do not synchronize between users or devices and can be cleared by the browser.
- No live barcode scanner, label printer, carrier API, purchasing system, or database is connected. Barcode and tracking workflows are illustrative only.
- No real customer, employee, inventory, or regulated product information should be entered.
- Inventory movement, lot/expiry control, quality release, approvals, audit security, backups, and multi-user consistency require a backend and production-grade design before operational use.

## Suggested future production roles

- **Quality Control (QC):** inspect lot, expiry, damage and quantity before stock release.
- **Procurement/Purchasing:** supplier POs, vendor records, expected receipts and purchase approvals.
- **Inventory Controller:** stock adjustments, cycle counts, lot/expiry management and reconciliation.
- **Administrator:** configuration, user permissions, audit access and reporting.
