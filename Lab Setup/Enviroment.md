# Lab Environment Setup

## Overview
This document describes the controlled lab environment used for Android application penetration testing. The environment is intentionally isolated and configured only for educational security testing.

---

## Host System
- Operating System: Windows
- Architecture: x64
- Purpose: Running Android emulator and security tools

---

## Android Environment
- Android Emulator: Android Studio AVD
- Emulator Device Profile: Pixel 3
- Android Version: Android 9 (API 28)
- System Image: Google APIs (non–Play Store)
- Root Access: Emulator default (sufficient for testing)

---

## Emulator Configuration
- RAM: 4 GB
- Internal Storage: 10 GB
- Graphics: Hardware acceleration
- Boot Mode: Cold boot
- Network: Default (NAT)

---

## Connectivity Verification
- Emulator connectivity verified using Android Debug Bridge (ADB)
- Command used:
  adb devices


  Target Application Deployment

Target App: InsecureBankv2

Installation Method: ADB

Command used:

adb install InsecureBankv2.apk


Application launched and tested for basic functionality
