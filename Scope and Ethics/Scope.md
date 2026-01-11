# Scope of Assessment

## Overview
This document defines the scope of the Android application penetration testing assessment conducted as part of an educational security exercise.

Clearly defining scope ensures that testing activities remain controlled, authorized, and ethical.

---

## In-Scope Assets
The following assets were included in the scope of this assessment:

- Android Application: InsecureBankv2
- Package Name: com.android.insecurebankv2
- Platform: Android Emulator
- Android Version: Android 9 (API 28)
- Testing Environment: Local, controlled lab setup

---

## Type of Testing
- Static Analysis (APK decompilation and code inspection)
- Dynamic Analysis (runtime behavior and network traffic analysis)
- Runtime Instrumentation (client-side behavior inspection)

---

## In-Scope Activities
- Decompiling the APK for source code analysis
- Inspecting AndroidManifest.xml and application logic
- Observing network communication behavior
- Identifying insecure storage and authentication patterns
- Mapping findings to OWASP Mobile Top 10

---

## Out-of-Scope Assets
The following are explicitly excluded from the scope:

- Real-world or production Android applications
- Applications without explicit authorization
- Real user data or credentials
- Attacks against external infrastructure
- Denial-of-Service or destructive testing

---

## Limitations
- The assessment focuses on client-side security.
- Backend server testing was limited to functional interaction only.
- No exploitation was performed against live or production systems.

---

## Scope Statement
All testing activities were conducted strictly within the defined scope using intentionally vulnerable applications in a controlled environment.
