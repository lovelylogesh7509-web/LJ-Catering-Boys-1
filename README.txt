LJ CATERING BOYS — Android app source
======================================

Included:
- Mobile-first app for boys, event scheduling, per-person work status, salary earned/payment ledger, daily/monthly/yearly reports, and JSON backup/restore.
- Data is stored locally on the phone inside the app. No account or server is required.
- App source uses a small Android WebView wrapper with the HTML app bundled offline.

IMPORTANT:
This ZIP is the source project, not a prebuilt APK. To build an APK, install Android Studio (with Android SDK), open this folder as a project, allow Gradle sync, then use:
Build > Build Bundle(s) / APK(s) > Build APK(s)
The debug APK will normally appear under app/build/outputs/apk/debug/app-debug.apk

Build requirements:
- Android Studio with Android SDK Platform 35 and a compatible JDK (Android Studio's bundled JDK is fine).
- Gradle wrapper is not included in this starter source. Android Studio can import the project; if prompted to create/sync Gradle files, follow its instructions or generate a wrapper from a local Gradle installation.

Quick test without APK:
Open app/src/main/assets/index.html in a modern browser. Some browsers restrict local storage for file URLs; for reliable storage, use the Android app build.

Features:
- Add/edit/delete boys (name and optional phone number; no Boy ID)
- Add/edit/delete events with date, location, required headcount, start/end time, notes
- For each boy on each event: green check = ready, red X = unavailable, yellow dots = pending
- Mark events complete
- Enter salary earned per boy and payment given; balance is calculated
- Day/month/year/all-time reports
- Dashboard for upcoming work, headcount still needed, and salary balances
- Export/restore JSON backup and delete-all-data option

Notes:
- Keep regular backups from the Backup tab. Uninstalling/resetting the phone can remove local records.
- This starter version provides an in-app reminder checklist/dashboard. It does not guarantee scheduled Android notifications.
- Review all records carefully before relying on salary totals for real payments.
