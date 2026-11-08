# St Sava Church myPOS Register

A custom Android/PWA point-of-sale register for St Sava Church, currently operating in clearly labelled demo mode.

## Current features

- myPOS-only register interface and account label
- Product catalogue, categories, basket, and custom one-off amounts
- Cash checkout with change calculation
- Local cash-sale history stored in this browser/device
- Android APK build workflow

## Payment status

**Real card and NFC payments are not enabled.** The card button remains disabled until an official myPOS integration is approved, configured, and tested with compatible hardware. The current application does not initiate or approve card payments and must not be represented as a live payment terminal.

## Build Android APK

The GitHub Actions workflow `.github/workflows/android-apk.yml` builds a debug APK when manually triggered or when relevant source files change. Download the `nfc-mypos-demo-apk` artifact from the completed workflow run and extract `app-debug.apk`.

## Data and security notes

Cash demo records and product settings are stored locally in the browser on this device. They are not automatically synced to a server or merchant account. Back up records before clearing browser data or changing devices. Do not put merchant credentials, API keys, or private keys in this repository or in the app's public frontend.

## Future myPOS integration

Before implementing live payments, confirm the supported integration route and device compatibility directly with myPOS. Keep credentials server-side where required and only record a card sale after an authenticated approval response from the official provider.