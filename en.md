# YuRadio Privacy Policy

**Last updated**: August 10, 2026
**Applies to**: YuRadio Android app (package `kr.nexteco.yuradio`)

NexTeco ("the Developer") values the privacy of YuRadio users and complies with applicable laws. This policy describes what information the app collects, uses, and shares.

## 1. Information Collected

The app **does not require account signup or login**, and does not collect personally identifiable information (name, email, phone, etc.).

The following data is used in a limited manner.

### 1.1 Data stored locally on the device

- Favorite stations (name, URL, frequency, tags)
- Selected country preset
- UI settings (language, sort order, etc.)
- Last played station ID (for auto-resume on restart)
- Data usage statistics (daily traffic, split by Wi-Fi/mobile)
- Anonymous install identifier (a random value generated on first launch - see 1.4)

Identified song details are kept in memory for display only and are discarded when
you change channels or close the app. No history is stored.

**All of this data is stored only in the device's internal SQLite database and is never sent externally.**

### 1.2 Data transmitted over the network

The app communicates with the following external services for functionality.

| Service | Data sent | Purpose |
|---|---|---|
| Radio Browser (radio-browser.info) | Country code, search query | Station directory lookup |
| Broadcaster streaming servers | HTTP requests | Radio audio playback |
| AcoustID (acoustid.org) | Audio fingerprint, duration | Song identification (optional) |
| MusicBrainz (linked) | Recording ID | Metadata for identified songs |
| Broadcaster now-playing APIs (MBC, SBS) | HTTP requests | Show the current song/program (optional) |
| Listening stats server (Cloudflare) | Anonymous install identifier, app version | Regional listening statistics (optional - see 1.4) |

An **audio fingerprint** is a short hash extracted from ~16 seconds of audio; **the original audio cannot be reconstructed from it.** It is not sent when auto-identify is disabled.

### 1.4 Anonymous listening statistics

The app aggregates how many people are listening in each region and shows this on a
public map.

**What is sent** is only the **random install identifier** generated on first launch
and the **app version**. It is not a device ID or advertising identifier, and
reinstalling the app creates a new value. **No location data (GPS) and no information
about which channel you are listening to is sent.**

**The server infers only the country and first-level administrative region** (e.g.
province/state) from your IP address. Finer divisions are not collected because IP
based accuracy is poor at that level, and map coordinates are rounded to roughly
11 km. **The original IP address is never stored.**

Data is sent only while a station is playing, about every 5 minutes. Stopping
playback or exiting the app removes you from the count immediately.

**Retention**

| Item | Period |
|---|---|
| Current listening session | Deleted within 24 hours of the last signal |
| Install identifier record (for unique user/install counts) | 400 days after last access |
| Daily regional aggregates (not personally identifiable) | 400 days |

**How to turn it off**: App → Settings → About tab → Listening Map →
**Share anonymous listening stats**. Sending stops immediately and the current
session record on the server is deleted right away.

This aggregation is processed and stored on servers operated by Cloudflare, Inc.
(Cloudflare Workers and D1).

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
- Cloudflare: https://www.cloudflare.com/privacypolicy/

## 3. Ads / Analytics / Crash Reporting

- **No advertising SDKs**
- **No analytics SDKs** (Firebase Analytics, Google Analytics, etc.)
- **No crash reporting SDKs** (Crashlytics, Sentry, etc.)

No third-party analytics tools are used. The one exception is the app's own listening
statistics described in 1.4, which can be turned off in Settings.

## 4. Children

This app is not directed at children under 13. While rated "Everyone", we recommend parental supervision for younger users.

## 5. Data Deletion

**On-device data** is removed entirely when you uninstall the app. Individual items
can be deleted in the app:

- Favorite stations: Settings → Channels, or long-press a station in the list
- Data usage records: Settings → About → Reset usage
- Everything: Android Settings → Apps → YuRadio → Storage → Clear Data

**Server-side data** is limited to the listening statistics described in 1.4:

- Turning off Settings → About → Listening Map → Share anonymous listening stats
  stops sending and immediately deletes the current session record
- What remains is only access dates tied to an anonymous install identifier, deleted
  automatically after the retention periods above
- Reinstalling the app generates a new identifier, so it cannot be linked to earlier records
- For any other deletion request, please contact us using the details below

## 6. Changes to this Policy

Any changes will be announced via app update and on this page.

## 7. Contact

For privacy inquiries, please contact:

**NexTeco**
Email: nexteco.kr@gmail.com
