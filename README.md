# ForgeFlow — Workshop Billing

A simple browser-based billing site for machine parts and workshop services.

## Features

- **Built-in MRP price list** (`data/mrp-june-2025.json`, 65,208 parts from *MRP June'25*). Check any part's price from the Home page by part number or description.
- **Fast billing:** type a part number or name, press Enter, and the MRP and GST rate fill in. Adding the same part again increases its quantity. Add labour lines, discounts and notes.
- **GST invoices:** MRP is treated as GST-inclusive by default, with taxable value, CGST/SGST or IGST, round off and amount in words on the printed bill.
- **New price lists:** upload next month's MRP Excel file (columns like Material, Desc, MRP, GST rate) under *Price list & parts*. It is stored in this browser and replaces the built-in list on this device.
- Customers are remembered from past bills; their details fill in when you type their name.
- Share a bill summary on WhatsApp or email, print or save it as PDF, export bills to CSV, and back up or restore data.

## Data and privacy

Bills, business settings and your own items are stored in the browser on the device where the site is used. Uploaded price lists are read in the browser and kept in its IndexedDB storage; they are not sent anywhere. Use **Business settings → Download backup** to move bills to another device.

## Updating the built-in price list

Replace `data/mrp-june-2025.json` with a file of the same shape (`{"name": "...", "rows": [[partNo, description, mrp, gstRate], ...]}`) and update `BUILT_IN_LIST` in `index.html` if the file name changes.

## Live site

The site is published with GitHub Pages from the `main` branch:

https://digvijay165.github.io/machine-shop-billing/
