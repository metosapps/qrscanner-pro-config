# QR Scanner Pro — Remote Config

Live configuration for the **QR Scanner Pro** Android app (`com.qrpro.scanner` / `com.qrpro.scanner.gx`).

The app fetches **`config.json`** from this repo's raw URL on every launch (3-hour cache):

```
https://raw.githubusercontent.com/metosapps/qrscanner-pro-config/main/config.json
```

Edit `config.json` and every install picks up the change within ~3 hours — **no app update needed**.

## Keys

| Key | What it controls |
|-----|------------------|
| `admob_open_ad_id` | AdMob App Open ad unit |
| `admob_banner_id` | AdMob banner ad unit |
| `admob_interstitial_id` | AdMob interstitial ad unit |
| `yandex_banner_id` | Yandex banner ad unit |
| `yandex_interstitial_id` | Yandex interstitial ad unit |
| `ads_enabled` | Master kill-switch for ALL ads |
| `ad_provider` | `"admob"` or `"yandex"` — which network serves banners/interstitials |
| `open_ad_enabled` | Toggle App Open ads only |
| `open_ad_cooldown_min` | Minimum minutes between App Open ads |
| `interstitial_every_n_scans` | Show an interstitial every N scans |
| `privacy_policy_url` | Privacy policy link (Settings + GDPR) |
| `terms_url` | Terms of service link |
| `more_apps_url` | Galaxy Store seller page (More Apps button) |
| `galaxy_store_app_url` | App page deep link (Share button) |
| `galaxy_store_review_url` | Review deep link (Rate App button) |

Blank/missing keys fall back to the app's built-in defaults.

## Hosted pages (GitHub Pages)

- Privacy policy: https://metosapps.github.io/qrscanner-pro-config/privacy.html
- Terms of service: https://metosapps.github.io/qrscanner-pro-config/terms.html

## ⚠️ Current state

Ad IDs are **Google/Yandex TEST ads** — replace with real ad unit IDs before/after store release. `more_apps_url` still needs the real Samsung Seller ID.
