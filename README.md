# Easy Mandi Android downloads

- [Download Easy Mandi APK for most Android phones (64-bit)](https://raw.githubusercontent.com/Programmer-s-Picnic/easymandidata/main/releases/EasyMandi-arm64-v1.apk)
- [Download Easy Mandi APK for older 32-bit phones](https://raw.githubusercontent.com/Programmer-s-Picnic/easymandidata/main/releases/EasyMandi-armeabi-v7a-v1.apk)

The latest APKs were built from [easymandi commit d4e116e](https://github.com/Programmer-s-Picnic/easymandi/commit/d4e116ed4781bdd9792790010e7f982cef73ac25) and published from a checksum-verified Android workflow artifact. Their app ID and signing key are unchanged, so installing the appropriate APK updates the earlier Easy Mandi installation.

When online, the app reads the live catalog from `https://cserver.learnwithchampak.live/easymandi/api/catalog.php`. Product names, prices, availability, delivery charges and minimum order are controlled from the [Easy Mandi admin website](https://programmer-s-picnic.github.io/easymandi/admin/). The packaged catalog remains an offline fallback; it can be older than the server data. Use the app's Refresh catalog button after an admin update. Admin editing is only on the website.

## Current APK SHA-256

```text
d039a57e7bff32b6e907b0e5cfcc2b3d82b2486ee2e1c0a4f4ef5d28addef39a  EasyMandi-arm64-v1.apk
fa90699e5ef6a55cfda731ce71c03887c2b3dcb0164418c60f1f1469d82cbea7  EasyMandi-armeabi-v7a-v1.apk
```

The `catalog/products.json` file in this repository is a legacy fallback from early builds. The active catalog lives on cserver. APKs are published by [the verified artifact workflow](https://github.com/Programmer-s-Picnic/easymandidata/actions/workflows/publish-from-artifact.yml). Checkout sends an order enquiry through WhatsApp; it does not create a server order or collect payment.
