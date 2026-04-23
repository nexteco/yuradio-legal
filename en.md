# YuRadio Privacy Policy

**Last updated**: April 23, 2026
**Applies to**: YuRadio Android app (package `kr.nexteco.yuradio`)

NexTeco ("the Developer") values the privacy of YuRadio users and complies with applicable laws. This policy describes what information the app collects, uses, and shares.

## 1. Information Collected

The app **does not require account signup or login**, and does not collect personally identifiable information (name, email, phone, etc.).

The following data is used in a limited manner.

### 1.1 Data stored locally on the device

- Favorite stations (name, URL, frequency, tags)
- Selected country preset
- UI settings (sort order, etc.)
- Last played station ID (for auto-resume on restart)
- Song identification history (up to 50 entries, removed when the app is uninstalled)

**All of this data is stored only in the device's internal SQLite database and is never sent externally.**

### 1.2 Data transmitted over the network

The app communicates with the following external services for functionality.

| Service | Data sent | Purpose |
|---|---|---|
| Radio Browser (radio-browser.info) | Country code, search query | Station directory lookup |
| Broadcaster streaming servers | HTTP requests | Radio audio playback |
| AcoustID (acoustid.org) | Audio fingerprint, duration | Song identification (optional) |
| MusicBrainz (linked) | Recording ID | Metadata for identified songs |

An **audio fingerprint** is a short hash extracted from ~16 seconds of audio; **the original audio cannot be reconstructed from it.** It is not sent when auto-identify is disabled.

### 1.3 System Permissions

| Permission | Purpose | Required/Optional |
|---|---|---|
| `INTERNET` | Download radio streams and call APIs | Required |
| `FOREGROUND_SERVICE` / `FOREGROUND_SERVICE_MEDIA_PLAYBACK` | Background playback | Required |
| `WAKE_LOCK` | Keep audio playing while screen is off | Required |

The app **does not request** location, contacts, photos, or microphone permissions.

## 2. Data Sharing

The Developer does not sell, rent, or share user data with third parties.

When required for app functionality, the app communicates with the external services listed in 1.2, and each service processes the traffic under its own policy.

- Radio Browser: https://www.radio-browser.info/
- AcoustID: https://acoustid.org/privacy
- MusicBrainz: https://metabrainz.org/privacy

## 3. Ads / Analytics / Crash Reporting

- **No advertising SDKs**
- **No analytics SDKs** (Firebase Analytics, Google Analytics, etc.)
- **No crash reporting SDKs** (Crashlytics, Sentry, etc.)

## 4. Children

This app is not directed at children under 13. While rated "Everyone", we recommend parental supervision for younger users.

## 5. Data Deletion

All app data resides only on the device, so uninstalling the app removes all data.

You can also delete items individually:

- Favorite stations: Settings → swipe or long-press a station → Delete
- Identification history: Android Settings → Apps → YuRadio → Storage → Clear Data

Because **no user data is stored on any server**, a separate deletion request process is not required.

## 6. Changes to this Policy

Any changes will be announced via app update and on this page.

## 7. Contact

For privacy inquiries, please contact:

**NexTeco**
Email: nexteco.kr@gmail.com
