# Carvia Privacy Policy

Last updated: 10 November 2026
App: Carvia (Android package `com.sn.carvia`), version 0.7 and later
Developer / data controller: Soft Nova, Türkiye, Istanbul
Contact (privacy and deletion requests): softnova.global@gmail.com

## 1. Scope

This policy explains what data the Carvia app processes on your phone and on the Android Auto screen, why, who receives it, and what rights you have. Carvia does not read speed, fuel level, mileage or any other data from your vehicle. You enter vehicle information yourself.

The main policy is written in English. The KVKK notice for users in Turkey (section 14) is also available in Turkish (`kvkk-aydinlatma.tr.md`) and English (`kvkk-aydinlatma.en.md`) in the same repository.

## 2. Data we process

### 2.1 Data you enter
- Vehicle details: nickname, make, model, year, fuel type, inspection date, body type.
- Fuel and charging entries: odometer, cost, currency, quantity, unit, date, fuel settings.
- Maintenance records and plans: dates, odometer, descriptions, cost, parts, next service date or distance, reminder state.
- Home shortcuts and web favorites (URLs, titles, order).

This data is stored on your device. If you sign in, it is also stored in the cloud (section 5).

### 2.2 Account data and guest identifier
- If you sign in with Google or with email and password, we process your email address, display name and an account ID (uid) through Firebase Authentication. We never see or store your password; Firebase handles it.
- If you continue as a guest, the app silently creates an anonymous Firebase account. It only has an anonymous ID (uid) and is used to keep your "Access time" balance (section 2.5). When you later sign in, the anonymous account is linked to your real account.

### 2.3 Location
- With your permission, your approximate or precise location is used while the app is in use to show nearby fuel and charging stations on the map, on your phone and on the Android Auto screen. The app does not request background location.
- To find stations, the app sends the coordinates of the search area and a search radius to third-party servers (section 6). The coordinates are rounded to a grid so that nearby searches share one cached answer. Your IP address is visible to those servers. The app does not send your location to our own servers or to your account.
- In-app route to a station: only when you tap "Start navigation" (and again when the app recalculates the route after you leave it), your current coordinates and the station's coordinates are sent to Geoapify to calculate the route (section 6). Geoapify also sees your IP address and the identifier bound to the app's API key. We do not store the route: it is kept in the app's memory while you navigate (plus a 60-second in-memory cache) and is not sent to our servers or to your account. While a route is active the app keeps reading your location only while the map is open on the phone or the Android Auto screen; it still does not request background location. To keep within the free service limits, the app stores on your device only the number of route requests made today and, if the service rejected the app's key, the time until in-app routing may be tried again; these contain no location.
- If you set the car browser or screen sharing to work "Only when stopped", the phone's GPS speed is read on the device to tell whether the vehicle is moving. Speed and location are not stored or sent.

### 2.4 Receipt photos, files, screen sharing and voice search
- Receipt photo: a fuel receipt photo you take is read on the device with Google ML Kit text recognition. It is not uploaded and not added to your account.
- Excel files: when you import or export records as .xlsx, only the file you choose through the Android file picker is used.
- Screen sharing: only if you start it. Android asks for your permission and shows a continuous notification with a Stop button while it runs. Your phone screen is shown on the Android Auto display; no audio is captured. The image is not recorded, saved, or sent to our servers. You can stop sharing from the notification, the app home screen or the widget.
- Voice search: on the car web page, if you allow the microphone, speech is processed by the speech recognition service of your device (usually Google). Carvia does not record or store audio.

### 2.5 Access time, ads and purchases
- Access time: the web browser and screen sharing features use a usage-based "Access time" balance. New signed-in accounts receive a welcome amount once. Watching a rewarded ad adds more. We store in Firestore, under your account or anonymous ID, the amount granted, the amount used, and timestamps of the last grant and open usage interval.
- Welcome marker (anti-abuse): to give the welcome amount only once per email address, we store a marker record whose name contains your lower-cased email address and which holds your account ID. This marker is not removed when you delete your account (see section 9).
- Advertising: Carvia shows ads with Google AdMob (rewarded, native and banner ads). AdMob may use your device's advertising ID and other device and ad-interaction data to serve and measure ads, including personalized ads where permitted and where you have given consent. See section 7.
- Purchases: the app contains Google Play Billing code to check subscription entitlement. A paid PRO subscription (which could remove ads and Access time limits) is not available in this version and may be added in the future. If it is added, Google Play will process payments; we will not receive your card details, and this policy will be updated.

### 2.6 Web browser
The in-app browser uses Android WebView. Websites you visit may set their own cookies and store their own data on your device (third-party cookies are enabled). Their privacy practices apply to what they collect. Carvia does not send your browsing history to its own servers. It stores only the favorites you save.

### 2.7 Technical and crash data
In release builds Firebase Crashlytics collects crash and error reports: stack traces, device model, Android version, app version, an installation ID generated by Firebase, and diagnostic lines such as screen names, timings, Android Auto connection state and the reason the previous session ended. We do not add vehicle names, plates, addresses or account data to these reports. Firebase App Check (Play Integrity) checks that requests to our Firebase backend come from a genuine copy of the app and may process device integrity signals. The app has no analytics library.

## 3. Why we process data and legal bases

| Purpose | Data | Legal basis (GDPR / UK GDPR; KVKK) |
| --- | --- | --- |
| Provide the app (garage, fuel, maintenance, map, web) | 2.1, 2.3, 2.4, 2.6 | Contract, Art. 6(1)(b); KVKK Art. 5/2-c |
| Account, sign-in, cloud sync | 2.1, 2.2 | Contract, Art. 6(1)(b) |
| Maintenance reminder notifications | 2.1 | Contract; notification permission |
| Nearby station search | 2.3 | Contract for the feature you request, Art. 6(1)(b), with the Android location permission as technical control (where the law of your country treats the permission as consent, Art. 6(1)(a)); KVKK Art. 5/2-c |
| In-app route to a station | 2.3 | Contract for the feature you request, Art. 6(1)(b); KVKK Art. 5/2-c |
| Access time ledger and welcome marker (fair use, fraud prevention) | 2.2, 2.5 | Legitimate interests, Art. 6(1)(f); KVKK Art. 5/2-f |
| Ads (including personalization) | Ad and device data | Consent where Google's consent message is shown, Art. 6(1)(a); elsewhere legitimate interests, Art. 6(1)(f); KVKK Art. 5/2-f. See section 4 and 14 |
| Crash detection, security, app integrity | 2.7 | Legitimate interests, Art. 6(1)(f) |

## 4. Consent for ads and your privacy choices

In the EEA, the UK and some other regions, Carvia shows Google's consent message (Google User Messaging Platform) before requesting ads. Ads are requested only when consent allows it. You can reopen "Ad privacy settings" in the app Settings where the app offers it, and change your choice at any time. You can also reset or delete your advertising ID in Android Settings > Google > Ads.

## 5. Where data is stored

- On your device: all data is first stored in app storage. Guest data stays on the device (plus the anonymous Access time record in section 2.2 and 2.5). Routes to stations are kept only in memory while you navigate (section 2.3) and are never stored in the cloud.
- In the cloud (only if you sign in, plus the Access time records of guests): Google Firebase Cloud Firestore, in the multi-region location eur3 (Europe). Your vehicles, fuel and maintenance data, shortcuts, favorites, email and display name are stored in one document accessible only by your own account (Firestore security rules).
- Android backup: app backup is enabled by the app. Some app files (settings, widget links, access cache) are excluded. Other app data may be included in your Google backup according to your device settings.

## 6. Who receives data

| Recipient | Purpose | Data |
| --- | --- | --- |
| Google Firebase (Authentication, Firestore, Crashlytics, App Check), Google Play services | Sign-in, sync, access ledger, crash reports, integrity | Account data, data in 2.1 and 2.5, technical data |
| Google AdMob and Google User Messaging Platform | Ads, consent | Device and advertising data, ad interactions, consent status, IP address |
| Overpass API servers (overpass.openstreetmap.fr, overpass-api.de, overpass.private.coffee, overpass.kumi.systems; tried in this order, the next one only when the previous one does not answer) | Station search | Rounded search coordinates, radius, IP address, app User-Agent (app version and our project contact, no user data) |
| OpenStreetMap tile servers (tile.openstreetmap.org) | Map tiles | Requested tile coordinates, IP address, app User-Agent (app version and our project contact, no user data) |
| Geoapify (api.geoapify.com) | In-app route calculation | Start and destination coordinates, IP address, identifier bound to the app's API key |
| Brand catalog and logo hosts, Google favicon service (google.com/s2/favicons) | Brand logos, favorite icons | IP address, domain of the favorite site |
| Websites you open in the browser | Web browsing | Their own practices apply |

Overpass, OpenStreetMap and Geoapify servers are operated by third parties, not by us. Geoapify processes route requests under its own terms and privacy policy. Geoapify is a company based in Germany; its default servers and main data centers are located in the European Union. We do not sell your personal data. We may disclose data when the law requires it.

International transfers: Google and other recipients may process data outside your country, including in the United States. Transfers rely on safeguards such as the EU-US Data Privacy Framework or Standard Contractual Clauses, as applicable to the provider. For Turkey see section 14.

## 7. Advertising, children and age

Carvia is intended for users aged 13 and over. It is not designed for children under 13. The app contains ads, an account system, a web browser and location features, which are not suitable for a child-directed service. We do not knowingly collect personal data from children under 13 (or under the digital consent age in your country: 13 to 16 in the EU depending on the country, 13 in the UK, 13 in the US under COPPA; in Turkey, persons under 18 need parental consent for consent-based processing). If you believe a child gave us data, write to softnova.global@gmail.com and we will delete it.

## 8. Retention

- Device data: until you delete it, clear app data or uninstall.
- Cloud account data: until you delete your account. When you delete your account in the app, we delete your Firestore documents and your Firebase account right away and we do not keep a copy or a backup period of our own. Firebase and Google may need a short technical time to remove copies from their own systems.
- Access time ledger: deleted together with your account on a best-effort basis; a leftover ledger grants nothing.
- Welcome marker: kept after account deletion without a time limit, to prevent repeated welcome grants (section 2.5); it contains your lower-cased email address and your account ID. Basis: our legitimate interest in preventing abuse.
- Guest (anonymous) records and other leftover records: an anonymous guest account and its Access time record, and Access time records that no longer have an account, are kept without a time limit. We keep them as part of our abuse, fraud and security controls: they help us detect and block tampering with Access time (for example modified or hacked app copies) and prevent repeated welcome credits. They contain no name or email address. You can ask us to remove them earlier (section 9). Basis: our legitimate interest in preventing abuse and keeping the service secure.
- Crashlytics reports: kept by Firebase for about 90 days under its standard retention.
- Receipt photos: not stored by the app.
- Routes to stations: not stored; kept in memory while you navigate and in a 60-second in-memory cache. The daily route request count and a possible 24-hour routing pause stay on your device until the next day or until you clear app data.

## 9. Deleting your data and account

- In the app: Settings > Account > Delete account. You confirm your identity again (Google or password). Your Firestore documents and your Firebase account are deleted. You can choose whether the data on this phone is also deleted.
- One vehicle: in My Garage, tap the delete button on the vehicle and confirm. The vehicle and its fuel purchases, fuel settings, maintenance records and maintenance plan are deleted from this phone and, when you are signed in, from your cloud account copy at the next sync.
- Local data only: clear app data in Android settings or uninstall the app.
- Guests: guest data is on your device. The anonymous Access time record is kept without a time limit for abuse, fraud and security controls (section 8). For earlier removal write to softnova.global@gmail.com; because the record has no name or email, we can delete it only if we can identify it from the details you send.
- Exception: the welcome marker described in section 2.5 may remain because it is needed to prevent abuse. It contains your email address and account ID. To ask us to review or remove it, write to softnova.global@gmail.com from your account email address.
- Public web page for deletion requests: https://sncarvia.web.app/account-deletion

## 10. Your rights

Depending on where you live, you can ask to access, correct, delete, restrict or object to processing of your data, receive a copy in a portable form, and withdraw consent at any time (withdrawal does not affect processing done before). You can export your fuel and maintenance records as Excel in the app. You can turn off location, microphone and notification permissions in Android settings.

- EEA, UK (GDPR, UK GDPR): you can also complain to your data protection authority (for the UK, the Information Commissioner's Office).
- United States (CCPA/CPRA and other state laws): you can ask to know, access, delete and correct personal information, and to opt out of "sale" or "sharing" for cross-context behavioral advertising. We do not sell data for money. Personalized ads through AdMob may count as "sharing" in some states; you can opt out through the in-app ad privacy settings and Android advertising ID settings. We will not discriminate against you for using these rights. We do not use sensitive personal information to infer characteristics about you.
- Turkey: see section 14.

Contact softnova.global@gmail.com. We answer within 30 days (45 days for CCPA requests, extendable as the law allows).

## 11. Security

Transfers use HTTPS. Cloud data is protected by Firebase Authentication, Firestore security rules and App Check. No system is perfectly secure.

## 12. Changes to this policy

We will update the date at the top when this policy changes. If we add PRO purchases or any new data use, we will update this policy before it starts and, where the law requires, ask for your consent.

## 13. Contact

Soft Nova, Türkiye, Istanbul
softnova.global@gmail.com

## 14. Notice for users in Turkey (KVKK Information Notice, Law No. 6698, Art. 10)

This notice is also provided in Turkish (`kvkk-aydinlatma.tr.md`) and English (`kvkk-aydinlatma.en.md`) in the same repository.

- Data controller: Soft Nova, Türkiye, Istanbul, softnova.global@gmail.com. [VERBIS registration status - TO BE CONFIRMED BY SOFT NOVA.]
- Personal data processed: identity and contact data (email, display name), user transaction data (vehicle, fuel, maintenance records, Access time), location data, device and technical data, advertising and consent data (see section 2).
- Purposes: providing the app, account and sync, location-based station search, in-app route calculation to a station, fair use and security, advertising, crash analysis, legal obligations.
- Legal grounds (Art. 5 of Law No. 6698): performance of a contract (providing the app, your account and cloud sync, Access time, and the location-based station search and in-app route you ask for, Art. 5/2-c); legitimate interests that do not harm your fundamental rights (fair use and fraud prevention, security and crash analysis, and serving and measuring ads where Google's consent message is not shown, Art. 5/2-f); legal obligation (Art. 5/2-ç). We do not process special categories of personal data (Art. 6). Location is read only after you grant the Android location permission, which you can withdraw at any time in Android settings. Where Google's consent message is shown for ads, ads follow your choice there and you can change it in the app's ad privacy settings. You can also reset or delete your advertising ID in Android Settings > Google > Ads. This is an information notice under Art. 10; it does not ask for your consent.
- Recipients and transfer abroad: Google (Firebase, AdMob, Google Play services), Geoapify (route calculation: start and destination coordinates, IP address, identifier bound to the app's API key) and the servers in section 6. Data is transferred abroad under Art. 9 of Law No. 6698 as amended by Law No. 7499: on an adequacy decision of the Personal Data Protection Board, or with appropriate safeguards such as the Board's standard contract, which is notified to the Authority within the legal period, or, only for occasional transfers, on the exceptions listed in Art. 9. We do not rely on a general explicit consent for these transfers.
- Collection method: automatically through the app and the SDKs, and from you directly.
- Your rights under Art. 11: learn whether your data is processed, request information, learn the purpose and whether it is used appropriately, learn the recipients in Turkey or abroad, ask for correction, ask for deletion or destruction, ask that these actions be notified to recipients, object to results against you made only by automated analysis, and claim compensation for damage from unlawful processing.
- How to apply: write to softnova.global@gmail.com. We answer within 30 days at the latest. You may also complain to the Personal Data Protection Board (KVKK).
