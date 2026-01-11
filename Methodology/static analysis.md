# Methodology – Static Analysis

## Objective
To analyze the Android application without executing it, in order to identify insecure design patterns, hardcoded values, and client-side security weaknesses.

---

## Approach
Static analysis was performed by decompiling the application APK and inspecting its source code, configuration files, and resources.

---

## Steps Performed

1. APK Inspection
   - The APK file was opened using Android Studio APK Analyzer.
   - Basic application metadata was reviewed (package name, version, size).

2. Decompilation
   - The APK was decompiled using JADX.
   - Java source code and AndroidManifest.xml were reviewed.

3. Manifest Analysis
   - Permissions requested by the application were examined.
   - Exported components and debuggable settings were identified.

4. Code Review
   - Authentication logic was reviewed.
   - Hardcoded URLs and endpoints were identified.
   - Local storage usage (SharedPreferences / databases) was analyzed.
   - Absence of encryption mechanisms was noted.

---

## Tools Used
- Android Studio (APK Analyzer)
- JADX

---

## Outcome
Static analysis helped identify insecure communication design, hardcoded endpoints, and insecure local storage usage without interacting with the backend server.
