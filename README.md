# mobile-app-update-rules
📱 Static JSON configuration for iOS and Android apps update management (forced and optional updates, version rules, and changelog).

# iOS/Android App Update Rules

This repository hosts a **static JSON file** (`update-rules.json`) used to manage **forced** and **optional** updates for an iOS/Android application already published on the App Store.

The JSON file provides:
- **Minimum supported version** → anything below this triggers a *forced update*.
- **Latest version** → anything below this (but above min supported) triggers an *optional update*.
- **Custom messages** for forced/optional popups.
- **Version history log** for displaying "What's New" in update prompts.
- **Store country code** for App Store lookup.

---

## 📄 JSON Structure

```json
{
  "minSupportedVersion": "1.5.0",
  "latestVersion": "1.7.0",
  "storeCountry": "IN",
  "messages": {
    "forced": "A new version is required to continue using the app.",
    "optional": "A new version is available with improvements. Would you like to update?"
  },
  "versionHistory": {
    "1.7.0": [
      "Added dark mode support",
      "Improved performance on iOS 18",
      "Bug fixes for login issues"
    ],
    "1.6.0": [
      "Introduced push notifications",
      "Enhanced profile editing features"
    ],
    "1.5.0": [
      "Major UI refresh",
      "Security improvements"
    ]
  }
}
