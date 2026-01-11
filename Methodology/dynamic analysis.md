# Methodology – Dynamic Analysis

## Objective
To analyze the application behavior during runtime in order to observe network communication, authentication flow, and data handling.

---

## Approach
Dynamic analysis was conducted by running the application on an Android emulator and monitoring its runtime behavior and network interactions.

---

## Steps Performed

1. Environment Preparation
   - Android Emulator was launched using Android Studio.
   - The target application was installed using ADB.

2. Application Interaction
   - The application was opened on the emulator.
   - Login and navigation flows were observed.
   - Error handling and user feedback were noted.

3. Network Traffic Analysis
   - Emulator network traffic was routed through Burp Suite.
   - HTTP requests and responses were intercepted.
   - Authentication requests were analyzed for insecure transmission.

4. Request Manipulation
   - Captured requests were modified and replayed.
   - Server responses were observed to assess trust assumptions.

---

## Tools Used
- Android Emulator
- ADB
- Burp Suite

---

## Outcome
Dynamic analysis confirmed insecure communication over HTTP and demonstrated the exposure of sensitive data during network transmission.
