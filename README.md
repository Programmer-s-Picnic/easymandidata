# Easy Mandi Android downloads

- [Download Easy Mandi APK for most Android phones (64-bit)](https://raw.githubusercontent.com/Programmer-s-Picnic/easymandidata/main/releases/EasyMandi-arm64-v1.apk)
- [Download Easy Mandi APK for older 32-bit phones](https://raw.githubusercontent.com/Programmer-s-Picnic/easymandidata/main/releases/EasyMandi-armeabi-v7a-v1.apk)

The latest APKs were built from [easymandi commit 3a010e5](https://github.com/Programmer-s-Picnic/easymandi/commit/3a010e5a241123c9d15e58f717225371bdfae0a6) and published from a checksum-verified Android workflow artifact. Their app ID and signing key are unchanged, so installing the appropriate APK updates the earlier Easy Mandi installation.

When online, the app reads the live catalog from `https://cserver.learnwithchampak.live/easymandi/api/catalog.php`. Product names, prices, availability, delivery charges and minimum order are controlled from the [Easy Mandi admin website](https://programmer-s-picnic.github.io/easymandi/admin/). The packaged catalog remains an offline fallback; it can be older than the server data. Use the app's Refresh catalog button after an admin update. Admin editing is only on the website.

## Current APK SHA-256

```text
811863190b5612917fecac150a6708a1bc68dee9c40711563b48cbab2687a3c5  EasyMandi-arm64-v1.apk
631f3d2af7d4125671de6381210f04fc77d66536cb11629128ea03d8be2633f2  EasyMandi-armeabi-v7a-v1.apk
```

The `catalog/products.json` file in this repository is a legacy fallback from early builds. The active catalog lives on cserver. APKs are published by [the verified artifact workflow](https://github.com/Programmer-s-Picnic/easymandidata/actions/workflows/publish-from-artifact.yml). Checkout saves a pending order in cserver MySQL, then offers an optional WhatsApp message containing its order reference. The admin website lists and updates order status. No payment is collected.
