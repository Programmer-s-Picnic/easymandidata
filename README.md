# Easy Mandi data and client APKs

## Client downloads

- [Android 64-bit APK (recommended)](https://raw.githubusercontent.com/Programmer-s-Picnic/easymandidata/main/releases/EasyMandi-arm64-v1.apk) — 17.8 MB, for most current Android phones.
- [Android 32-bit APK](https://raw.githubusercontent.com/Programmer-s-Picnic/easymandidata/main/releases/EasyMandi-armeabi-v7a-v1.apk) — 15.2 MB, for older Android phones.

Install the appropriate APK on an Android phone. Android may ask permission to install an app from the browser or file manager. Both APKs have the same app ID and version; choose one for your device. The demo loads updated products from this repository when online and uses a bundled catalog offline.

## Catalog

`catalog/products.json` defines products, categories, pricing, availability, minimum order and delivery fee. Prices are in INR for the stated unit. Keep each product `id` unique. The Flutter app and web preview live in [easymandi](https://github.com/Programmer-s-Picnic/easymandi). Update its `assets/products.json` when releasing a new offline catalog snapshot.

The shopping cart persists on the device. Checkout opens a WhatsApp order enquiry and lets the tester choose a recipient because `store.supportPhone` is blank. Set it to a confirmed Easy Mandi business number before taking real orders. Demo prices and delivery availability need confirmation. No payment is collected.

## Release integrity

The APKs are assembled from `release-parts/` by [the publish workflow](https://github.com/Programmer-s-Picnic/easymandidata/actions/workflows/publish-apks.yml) and checked against `release-parts/manifest.sha256`.

```text
8d28e63a7990d79bf08d31cebdc2525f9c3d4fb31281c25797f0a68cff06ec99  EasyMandi-arm64-v1.apk
a35b7a0a15dc0d9cf39ca6eff33e20b7d073ca4bb50a0c0d30c3ee7f1ee6cd17  EasyMandi-armeabi-v7a-v1.apk
```

## Contact and address format

Checkout formats are set in `catalog/products.json` under `checkout`: +91 followed by 10 digits beginning with 6–9, a house/building, a street/locality, optional landmark, and a six-digit Indian PIN. The current demo city is Varanasi; PIN syntax validation does not imply delivery coverage.
