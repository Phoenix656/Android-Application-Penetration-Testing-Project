# Tools Used in Android Application Penetration Testing

## Overview
This document lists the tools used to perform a complete Android application penetration test on an intentionally vulnerable Android application. The tools were used across static analysis, dynamic analysis, runtime inspection, and documentation phases.

---

## 1. Android Studio
**Purpose**: Android SDK and emulator management

**Usage**:
- Installed and managed Android SDK components
- Created and configured Android Virtual Devices (AVD)
- Used APK Analyzer for preliminary APK inspection
- Provided integrated terminal for ADB 

---

## 2. Android Emulator (AVD)
**Purpose**: Simulated Android device for testing

**Usage**:
- Installed and executed the target application
- Observed runtime behavior
- Provided an isolated and safe testing environment

**Configuration:**
- Device Profile: Pixel 3
- Android Version: Android 9 (API 28)
- System Image: Google APIs (non-Play Store)

---

## 3. Android Debug Bridge (ADB)
**Purpose**: Communication and control interface for Android devices

**Usage**:
- Verified emulator connectivity
- Installed APK files
- Accessed application runtime environment

**Command Used**:
```bash
adb devices
adb install InsecureBankv2.apk
adb uninstall com.android.insecurebankv2
adb shell
adb shell pm list packages
adb pull /data/data/

---


## 4. JADX (Java Decompiler)
**Purpose**: Static analysis and reverse engineering of Android applications

**Usage**:
- Decompiled APK into readable Java source code
- Inspected AndroidManifest.xml
- Identified hardcoded endpoints
- Analyzed authentication logic and local storage **Usage**

**Command Used**:

bash
Copy code
jadx-gui InsecureBankv2.apk

---

## 5. APKTool
**Purpose**: Resource-level APK analysis

**Usage**:
- Decoded APK resources and configuration files
- Inspected XML files and application assets

**Command Used**:


bash
Copy code
apktool d InsecureBankv2.apk

---

## 6. Burp Suite
**Purpose**: Network traffic interception and analysis

**Usage**:
- Intercepted application network traffic
- Analyzed authentication requests and responses
- Observed insecure HTTP communication
- Identified plaintext data transmission

**Actions Performed**:
- Configured emulator proxy to Burp listener
- Captured HTTP requests and responses
- Modified requests for logic testing

---

## 7. Frida
**Purpose**: Runtime instrumentation and dynamic analysis

**Usage**:
- Hooked application methods at runtime
- Inspected runtime behavior
- Bypassed client-side security checks

**Command Used**:

bash
Copy code
frida-ps -U
frida -U -n com.android.insecurebankv2

---

## 8. Objection
**Purpose**: Runtime mobile exploration framework

**Usage**:
- Performed live application inspection
- Assisted in runtime analysis without modifying the APK

**Command Used**:

bash
Copy code
objection -g com.android.insecurebankv2 explore

---

## 9. Backend Server (Target Application)
**Purpose**: Supporting backend-dependent testing

**Usage**:
- Enabled application-server interaction
- Supported authentication and API testing
- Allowed end-to-end application behavior analysis

---

## 10. Postman / cURL
**Purpose**: Direct backend and API testing

**Usage**:
- Sent crafted HTTP requests
- Tested authentication and authorization logic
- Verified server-side trust assumptions

**Command Used** (cURL):
bash
Copy code
curl http://<server-ip>:<port>/login
curl http://<server-ip>:<port>/transactions