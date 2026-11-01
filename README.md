# EXYRON WIRE (Happ Proxy)

**Package:** `com.happproxy`  
**Version:** 4.7.1 (versionCode 1999)  
**ABI:** arm64-v8a only  

## Important

This app is **packed / protected**. The DEX contains only a small stub (`StubApp`).  
Real logic lives in native library `libgojni.so` (Go-based).  

Full Java/Kotlin source **cannot** be recovered by normal decompilation (apktool/jadx).

## Contents

| File | Description |
|------|-------------|
| `EXYRON-WIRE.apk` | Original APK (55 MB) — upload manually if not present |
| `.github/workflows/release.yml` | Publishes APK as GitHub Release / Actions artifact |

## Download APK

1. Go to **Actions** → latest successful run → Artifacts  
   **OR**
2. Go to **Releases** after workflow runs

## Rebuild / Re-sign (optional)

If you only need to re-package or change resources (icons, name):

```bash
# requires apktool + uber-apk-signer / apksigner
apktool d EXYRON-WIRE.apk -o decoded
# edit res/ or AndroidManifest.xml
apktool b decoded -o out.apk
# sign with your keystore
```

Because of packing, editing smali will **not** change core VPN behaviour.

## Legal

This repository only hosts the binary you provided for personal backup / CI.  
Respect the original app's license and terms.
