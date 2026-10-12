# CorebiQ GSTR-1 workspace

## Deploy
Upload the contents of this folder to any static host (GitHub Pages, Netlify, Hostinger public_html). Open `index.html`. The project does not require a backend. Google Fonts and Lucide are loaded from CDNs; if you need fully offline use, vendor those assets locally.

## Included modules
B2B, B2B Credit Notes (CDNR), B2C Small, E-commerce, Exempted/Nil, Export, Documents and HSN B2B. Each has a separate HTML file under `pages/`. Drafts are stored in the browser localStorage. CSV templates, CSV import, pasted CSV import, editable rows, draft saving and a combined JSON download are included.

## Official-tool reference and limitations
The uploaded GST Offline Tool source was inspected for section mapping, including B2CS keys (`sply_ty`, `rt`, `typ`, `pos`, `txval`, tax values), HSN fields, nil supply fields and document issue grouping. The uploaded package metadata appears older than the 3.2.4 version shown in the screenshot. Therefore the generated JSON is a practical draft serializer, **not certified or guaranteed filing-ready**. Test with dummy data in your exact official GST Offline Tool version and compare its accepted output schema before using for a return. In particular, the GST utility's expected wrapper/schema for HSN, e-commerce and amendments may vary.

## Data safety
The application processes data in the browser and saves drafts in localStorage on the current device. Clearing browser data removes saved drafts. No server upload is implemented.
