# Easy Mandi data

`catalog/products.json` is the public product catalog used by the Flutter app and web preview. Prices, stock flags, units, categories, delivery fee and minimum order can be edited there. Product `id` values must remain unique; `price` values are in INR for the stated unit. The Flutter app has a packaged fallback catalog for offline use; update its `assets/products.json` when releasing a new offline snapshot. APK releases go in `releases/`.

Demo prices and delivery details require confirmation before commercial use.
