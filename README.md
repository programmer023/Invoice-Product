# Invoice

A browser-based GST invoice generator for creating, previewing, and exporting professional tax invoices from a single HTML app.

## What this app does

This project turns `index.html` into a complete invoice studio with:

- Seller and bank details entry
- Buyer and order information capture
- Dynamic product / line-item entry
- GST tax calculation with CGST + SGST or IGST modes
- Live invoice preview matching a formal tax invoice layout
- PDF export using `pdfMake`
- Session-aware form persistence for recurring billing work
- Responsive layout for desktop and mobile use

## Features in the current workflow

### 1. Seller & Bank
- Add seller company name, address, GSTIN
- Store bank details such as bank name, account number, and IFSC
- Save delivery notes and terms
- Keep recurring seller data available in session storage

### 2. Buyer & Order
- Add buyer client name and billing address
- Enter invoice number and date
- Capture order number, delivery note, dispatch references, and payment terms

### 3. Products / Items
- Add multiple line items with:
  - description
  - HSN/SAC code
  - quantity
  - unit rate
  - tax type
  - CGST / SGST / IGST values
- Instant tax and subtotal calculation
- Customer-friendly table / card display of invoice entries

### 4. Preview, PDF Export & Round-Trip Prefill
- See the invoice update in real time in a document-style preview pane
- Review totals, tax split, amount in words, and footer details
- Export the final invoice to PDF directly from the browser
- **Prefill & Update from Existing PDF**: Upload or drag-and-drop any previously generated PDF to automatically restore the entire invoice, line items, buyer info, and settings with exact precision for quick edits and re-exports!

## How to use

### Open the app

Open `index.html` directly in a browser, or serve the folder locally:

```bash
cd Invoice
python -m http.server 8000
```

Then visit:

```text
http://localhost:8000
```

### Typical invoice flow

1. Fill in Seller Details
2. Add Buyer and Order information
3. Add each product or service item
4. Review the live invoice preview
5. Export the invoice as PDF

### Helpful actions

- Sample: populate example invoice data quickly
- Reset: clear the current form
- Save as Default Seller: reuse common seller profile details

## Project structure

```text
Invoice/
├── index.html
├── README.md
```

## Notes

- The app is front-end only and runs in the browser.
- Invoice data is managed within the page and browser session state.
- PDF export relies on the `pdfMake` library loaded from CDN.

## License

This project is currently provided as a local utility and does not include a formal license file unless added separately.
