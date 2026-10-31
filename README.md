# SmartCart AI — iPhone web app

This is a personal-use web app package. It works in Safari and can be added to the iPhone Home Screen after it is hosted on an HTTPS website.

## Included
- Shopping cart with item prices in NZD
- Adjustable budget and remaining-budget indicator
- Mark items purchased and remove items
- Camera/photo upload for shelf labels or receipts
- Browser-based OCR via Tesseract.js (the OCR library loads from a CDN, so first use needs internet)
- Local device storage using browser localStorage
- PWA manifest and service worker for Home Screen installation and basic offline caching

## Important limitations
- This is a helpful prototype, not a live supermarket price comparison service.
- OCR is heuristic: it may misread prices or product names. Always check the detected values before adding them.
- It does not connect to Woolworths, New World, PAK'nSAVE, or any live retailer feed.
- Cart data is stored in the browser on this device. Do not clear Safari website data if you want to keep it.
- No account, cloud sync, or SmartCart server is used. The static app files must be hosted somewhere over HTTPS to install it as a Home Screen web app. The OCR script is fetched from jsDelivr when needed.

## Easiest setup on iPhone
1. Upload the contents of this folder to a static HTTPS host (for example, a static-site hosting service). The host will give you a website address.
2. Open that address in Safari on your iPhone.
3. Tap Share → Add to Home Screen → Add.
4. Launch SmartCart from its Home Screen icon.

The hosting service stores the app files, not your shopping list. Your cart stays in Safari storage on your iPhone.

## Testing
You can open `index.html` in a desktop browser for a quick preview, but camera access and Add to Home Screen installation require an HTTPS-hosted site (or localhost during development).
