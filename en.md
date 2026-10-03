# YuRadio Privacy Policy

**Effective**: October 3, 2026
**Last updated**: October 3, 2026
**Applies to**: YuRadio Android app 1.4.0 and later (package `kr.nexteco.yuradio`)

NEXTECO ("the Developer") values the privacy of YuRadio users and complies with applicable laws. This policy describes what information the app collects, uses, and shares.

## Summary

- **No account signup.** No name, email, phone number, or account is required.
- **The Developer receives and stores nothing.** The Developer runs no server that receives user information.
- **Location is used only if you allow it, and only approximate location.** Picking your region happens entirely on the device. To show the weather, the app sends coordinates rounded to about 1 km to a weather service (MET Norway). The app works the same if you decline.
- **No microphone use.** Song identification analyzes the radio audio the app itself is playing, inside the app. It does not listen to your surroundings. This feature is off by default.
- **No ads, no advertising identifier (AAID), and no analytics or crash-reporting SDKs.**
- Favorites, settings and schedules are stored **on your device**. Recordings are saved to the phone's Music folder and remain after you uninstall the app.

## 1. Information Collected

The app **does not require account signup or login**, and does not collect personally identifiable information (name, email, phone, etc.).

### 1.1 Data stored on the device

Stored inside the app (app-private storage):

- Favorites: the favorite buttons on the radio screen (per country) and starred internet stations. Channel lists and groups saved in earlier versions are also kept, not deleted (name, URL, frequency, tags)
- The selected country and region, the band (FM/AM), and the last station played (to resume on restart)
- Display and sound settings: language, theme, dial style, volume, tone, lyrics text size, sort and view options, and on/off settings (lyrics, auto identify, notification display)
- Schedules (auto power-on, scheduled recording): time, days, station
- A reduced copy of the one photo you chose as the dial window background
- Lyrics cache: so the same song is not looked up again, the title and artist of songs that were looked up and the lyrics found, for roughly the 600 most recent songs
- Weather cache: the last weather received, the coordinates used for it (rounded to about 1 km, or the coordinates of the region's representative city), and the time. Only the most recent value is kept
- Whether the location permission has already been asked, and the region found from your location
- Data usage statistics (daily traffic, split by Wi-Fi/mobile)
- A copy of the station table (frequency list) received from the server

Stored in the phone's shared Music folder:

- Recordings: saved to `Music/YuRadio`. They are visible in file managers and other music apps, and **remain after you uninstall the app.** (On Android 9 and earlier they are saved to an app-private folder and removed with the app.)

Details of the song now playing are kept in memory for display only and are discarded when you close the app. Apart from the lyrics cache above, the app keeps no history of the songs or stations you listened to.

None of this data is sent to the Developer. Data stored inside the app is removed when you uninstall it. However, if you have turned on your phone's backup feature (Google backup), Android may back up app data to your own Google account. That backup is managed by Google and the Developer cannot access it.

### 1.2 Data exchanged with external services

The app communicates with the following external servers for functionality. As is inherent to internet communication, your IP address and access time are visible to these services, and are handled under each service's own privacy policy. No request carries an identifier for the user or the device.

| Service | Data sent | Purpose | When, and how to turn it off |
|---|---|---|---|
| Broadcaster streaming servers (KBS, MBC, SBS, CBS, EBS, broadcasters abroad, etc.) | Playback requests | Radio audio playback and recording | While you listen to or record a station |
| Stream address servers (official KBS and MBC servers, stream address servers of broadcasters abroad, and a third-party server that provides the SBS stream address) | Station channel identifier | Get a currently valid stream address | When you tune to that station |
| Broadcaster program and song information (KBS, MBC, SBS, CBS, EBS, Gugak FM) | Station channel identifier | Show the current program and song | While you listen to that station |
| Radio Browser (radio-browser.info) | Country code, search query, identifier of the station played (for its popularity stats) | Internet station list and search | When the app starts (to load the list), and when you search for or play an internet station |
| LRCLIB (lrclib.net) | Song title, artist name, and the album name and song length when known | Show lyrics | When the song is known. Not sent if you turn off "Lyrics" under Settings › About › Now Playing & Lyrics |
| AcoustID (acoustid.org) | Audio fingerprint, duration | Find songs by sound | Only if you turn on "Auto identify" (off by default) |
| MET Norway (api.met.no, the Norwegian Meteorological Institute) | Coordinates. See 1.3 | Show the weather | While the app is on screen, usually once every 30 minutes. If you do not allow location, the coordinates of the selected region's representative city are sent instead of yours |
| GitHub Pages (nexteco.github.io) | A file request only, no user information | Keep the station table (frequency list) up to date | When the app starts, at most once an hour |

The station table is a file the Developer publishes on GitHub Pages. Access logs are managed by GitHub and are not provided to the Developer. All other services are operated by third parties.

As required by their terms of use, requests to LRCLIB and MET Norway include the app name, version, and the address of this policy.

An **audio fingerprint** is a short hash extracted from about 16 seconds of broadcast audio; **the original audio cannot be reconstructed from it.** Turning off "Auto identify" stops all communication with AcoustID. Broadcaster program and song information is fetched regardless of that setting.

Some broadcaster servers only offer unencrypted connections (HTTP). When you listen to such a station, which station you are listening to may be visible along the network path.

### 1.3 Location

The app uses **approximate location** only (`ACCESS_COARSE_LOCATION`) and never requests precise location. The permission is optional, and the app works the same without it. It is used in two places.

| Use | What it does | What leaves the device |
|---|---|---|
| Matching your region ("Locate") | Picks the country and region (for example Seoul · Gyeonggi) from your location and shows that region's station table | Nothing. The calculation is done on the device |
| Weather | Shows the weather where you are | Coordinates rounded to two decimal places (about 1 km) are sent to MET Norway. If you are outside the selected region, the coordinates of that region's representative city are sent instead of yours |

- The permission is asked once when you first start the app, and when you tap "Locate".
- Location is checked only while the app is on screen. The app does not use background location.
- The rounded coordinates are kept on the device together with the last weather (1.1). No location history is built; only the most recent value is kept.
- When picking a region, the app reads the mobile network's country code (for example KR) on the device. It does not read your phone number or subscriber information.
- To stop, choose "Don't allow" under Android Settings › Apps › YuRadio › Permissions › Location. After that, the region is the one you pick yourself and the weather is shown for that region's representative city.

### 1.4 Information collected by the Developer

**None.** The Developer does not collect or retain any user data on any server. The app does not send user information to any server operated by the Developer.

### 1.5 System permissions

| Permission | Purpose | Required/Optional |
|---|---|---|
| `INTERNET` | Play radio streams and communicate with external services | Required |
| `ACCESS_NETWORK_STATE` | Check the connection and tell Wi-Fi from mobile data (data usage display) | Required |
| `FOREGROUND_SERVICE` / `FOREGROUND_SERVICE_MEDIA_PLAYBACK` | Background playback and recording, notification controls | Required |
| `WAKE_LOCK` | Keep playback and recording going while the screen is off | Required |
| `ACCESS_COARSE_LOCATION` | Matching your region, weather (1.3) | Optional. The app asks |
| `POST_NOTIFICATIONS` | Recording and schedule result notifications, playback notification (Android 13 and later) | Optional. Asked when you save your first schedule |
| `SCHEDULE_EXACT_ALARM` | Start a scheduled power-on or recording at the exact time | Optional. Allowed under "Alarms & reminders" in device settings |
| `RECEIVE_BOOT_COMPLETED` | Re-register schedules after the phone restarts | Automatic |
| `MODIFY_AUDIO_SETTINGS` | Tone effects (vacuum tube, AM radio) | Automatic |
| `VIBRATE` | A short vibration when turning the dial | Automatic |

The app **does not request** microphone, contacts, precise location, or photo and media access permissions. The dial window photo is chosen through Android's photo picker, and the app receives only the one photo you choose. Saving recordings to the Music folder does not use a storage permission either.

## 2. Data Sharing

Because the Developer collects no data, there is no user data to sell, rent, or share with third parties.

Only when required for functionality, the app communicates from the device directly with the external services listed in 1.2, and each service processes those requests under its own policy. Four of them carry content related to the user: the coordinates in weather requests (MET Norway), the song title and artist in lyrics requests (LRCLIB), the audio fingerprint in song identification requests (AcoustID), and the internet station search query and the identifier of the station played (Radio Browser).

- MET Norway: https://www.met.no/en/About-us/privacy
- LRCLIB: https://lrclib.net/
- AcoustID: https://acoustid.org/privacy
- Radio Browser: https://www.radio-browser.info/
- GitHub: https://docs.github.com/site-policy/privacy-policies/github-general-privacy-statement
- Broadcaster servers: each broadcaster's own privacy policy

## 3. Ads / Analytics / Crash Reporting

- **No advertising SDKs**
- **No analytics SDKs** (Firebase Analytics, Google Analytics, etc.)
- **No crash reporting SDKs** (Crashlytics, Sentry, etc.)
- **No first-party analytics or aggregation server**

## 4. Children

This app is not designed for children under 13. The app content itself is rated for general audiences and contains no objectionable material.

## 5. Data Deletion

The Developer holds no server-side data, so there are no server records subject to a deletion request.

**On-device data** can be deleted item by item in the app:

- Favorite buttons: on the radio screen, long-press a filled button and choose "Clear"
- Starred internet stations: on the Internet screen, long-press the station to remove the star
- Schedules: on the Schedule screen, open the schedule and choose "Delete schedule"
- Recordings: choose "Delete" under "Play" in the menu. You can also delete the `Music/YuRadio` folder in a file manager
- Dial window photo: Settings › Display › "Remove photo"
- Data usage records: Settings › About › "Reset usage"
- Stop using location: Android Settings › Apps › YuRadio › Permissions › Location › "Don't allow"
- Everything (including the lyrics and weather caches and channel lists from earlier versions): Android Settings › Apps › YuRadio › Storage › Clear data

Uninstalling the app removes everything stored inside it. **Recordings remain in the Music folder**, so delete them separately if you wish. App data left in a Google backup can be deleted from the backup settings of your Google account.

Access logs kept by external services are managed by each service under its own policy. The Developer cannot view or delete them.

## 6. Changes to this Policy

Any changes will be announced via app update and on this page. If usage statistics are added in a future version, that feature will ship **off by default (opt-in)**, and this policy together with the Play Store Data safety declaration will be updated before it takes effect.

Change history:

- October 3, 2026: Revised for app 1.4.0. Added location (matching your region, weather), the lyrics and weather services, recording and schedules, the permission list, and the deletion steps
- August 12, 2026: First version

## 7. Contact

For privacy inquiries, please contact:

**NEXTECO**
Email: nexteco.kr@gmail.com

---

[한국어](index.md)
