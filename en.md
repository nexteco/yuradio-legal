# YuRadio Privacy Policy

**Effective**: August 12, 2026
**Last updated**: August 12, 2026
**Applies to**: YuRadio Android app (package `kr.nexteco.yuradio`)

NexTeco ("the Developer") values the privacy of YuRadio users and complies with applicable laws. This policy describes what information the app collects, uses, and shares.

## Summary

- **No account signup.** No name, email, phone number, or account is required.
- **Nothing is sent to the Developer's servers.** The Developer does not collect or store any user data.
- **No location permission.** GPS coordinates are never collected.
- **No microphone use.** Song identification analyzes the radio audio the app itself is playing, inside the app. It does not listen to your surroundings.
- **No ads, no advertising identifier (AAID), and no analytics or crash-reporting SDKs.**
- Saved stations and settings stay **on your device only**.

## 1. Information Collected

The app **does not require account signup or login**, and does not collect personally identifiable information (name, email, phone, etc.).

### 1.1 Data stored locally on the device

- Favorite stations (name, URL, frequency, tags)
- Groups and the selected country preset
- UI settings (language, sort order, auto-identify on/off, etc.)
- Last played station ID (for auto-resume on restart)
- Data usage statistics (daily traffic, split by Wi-Fi/mobile)

Identified song details are kept in memory for display only and are discarded when you change channels or close the app. No history is stored.

**All of this data is stored only in the device's internal SQLite database and is never sent externally.** It is removed when you uninstall the app.

### 1.2 Data transmitted over the network

The app communicates with the following external servers for functionality. **All of them are operated by third parties; the Developer runs no server of its own.** As is inherent to internet communication, your IP address and access time are visible to these services, and are handled under each service's own privacy policy.

| Service | Data sent | Purpose |
|---|---|---|
| Radio Browser (radio-browser.info) | Country code, search query, played station identifier (for its popularity stats) | Station directory lookup |
| Broadcaster streaming servers (KBS, MBC, SBS, CBS, etc.) | HTTP requests | Radio audio playback |
| AcoustID (acoustid.org) | Audio fingerprint, duration | Song identification (optional) |
| MusicBrainz (linked) | Recording ID | Metadata for identified songs |
| Broadcaster now-playing APIs (MBC, SBS) | HTTP requests | Show the current song/program (optional) |

An **audio fingerprint** is a short hash extracted from ~16 seconds of audio; **the original audio cannot be reconstructed from it.**

**Turning off auto-identify** stops all AcoustID, MusicBrainz, and now-playing API traffic (the "Auto-identify" button in the app).

### 1.3 Information collected by the Developer

**None.** The Developer does not collect or retain any user data on any server. The app contains no functionality that sends information to a Developer-operated collection server.

### 1.4 System Permissions

| Permission | Purpose | Required/Optional |
|---|---|---|
| `INTERNET` | Download radio streams and call APIs | Required |
| `FOREGROUND_SERVICE` / `FOREGROUND_SERVICE_MEDIA_PLAYBACK` | Background playback and notification controls | Required |
| `WAKE_LOCK` | Keep the connection alive while the screen is off | Required |

The app **does not request** location, contacts, photos, or microphone permissions.

## 2. Data Sharing

Because the Developer collects no data, there is no user data to sell, rent, or share with third parties.

When required for app functionality, the app communicates with the external services listed in 1.2, and each service processes that traffic under its own policy.

- Radio Browser: https://www.radio-browser.info/
- AcoustID: https://acoustid.org/privacy
- MusicBrainz: https://metabrainz.org/privacy

## 3. Ads / Analytics / Crash Reporting

- **No advertising SDKs**
- **No analytics SDKs** (Firebase Analytics, Google Analytics, etc.)
- **No crash reporting SDKs** (Crashlytics, Sentry, etc.)
- **No first-party analytics or aggregation server**

## 4. Children

This app is not directed at children under 13. While rated "Everyone", we recommend parental supervision for younger users.

## 5. Data Deletion

The Developer holds no server-side data, so there are no server records subject to a deletion request.

**On-device data** is removed entirely when you uninstall the app. Individual items can be deleted in the app:

- Favorite stations: Settings → Channels, or long-press a station in the list
- Data usage records: Settings → About → Reset usage
- Everything: Android Settings → Apps → YuRadio → Storage → Clear Data

## 6. Changes to this Policy

Any changes will be announced via app update and on this page. If usage statistics are added in a future version, that feature will ship **off by default (opt-in)**, and this policy together with the Play Store Data safety declaration will be updated before it takes effect.

## 7. Contact

For privacy inquiries, please contact:

**NexTeco**
Email: nexteco.kr@gmail.com

---

[한국어](index.md)
