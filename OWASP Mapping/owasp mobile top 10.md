# OWASP Mobile Top 10 Mapping

## Overview
This document maps the identified security findings from the Android application penetration test to the OWASP Mobile Top 10 risks. Only applicable categories are included to ensure accurate and honest reporting.

---

## M1: Improper Platform Usage
**Status:** Not Identified

**Reason:**
- No misuse of platform features such as intents, permissions, or WebView APIs was observed during analysis.

---

## M2: Insecure Data Storage
**Status:** Identified

**Mapped Finding:**
- Insecure Local Storage

**Description:**
The application uses local storage mechanisms such as SharedPreferences or local databases without applying encryption. Sensitive data stored in this manner may be accessible on rooted devices or through malware.

---

## M3: Insecure Communication
**Status:** Identified

**Mapped Finding:**
- Insecure Network Communication

**Description:**
The application communicates with backend services over unencrypted HTTP. This exposes sensitive information to interception and manipulation through man-in-the-middle attacks.

---

## M4: Insecure Authentication
**Status:** Identified

**Mapped Finding:**
- Excessive Client-Side Trust in Authentication Flow

**Description:**
The application relies heavily on client-side logic and backend responses without strong client-side validation, increasing the risk of authentication abuse and request manipulation.

---

## M5: Insufficient Cryptography
**Status:** Identified

**Mapped Finding:**
- Lack of Encryption for Stored and Transmitted Data

**Description:**
Sensitive data is neither encrypted at rest nor adequately protected during transmission, indicating insufficient cryptographic implementation.

---

## M6: Insecure Authorization
**Status:** Not Identified

**Reason:**
- Authorization checks were not conclusively identified during static analysis.
- Requires deeper backend testing to confirm.

---

## M7: Client Code Quality
**Status:** Identified

**Mapped Finding:**
- Hardcoded Endpoints

**Description:**
Hardcoded backend URLs embedded in the client application increase exposure to reverse engineering and backend enumeration.

---

## M8: Code Tampering
**Status:** Not Identified

**Reason:**
- No code integrity or tamper detection mechanisms were observed.
- Exploitation was not required for this assessment.

---

## M9: Reverse Engineering
**Status:** Identified

**Mapped Finding:**
- Lack of Code Obfuscation

**Description:**
The application does not use obfuscation techniques, making reverse engineering trivial and exposing internal logic.

---

## M10: Extraneous Functionality
**Status:** Not Identified

**Reason:**
- No hidden, test, or debug functionality was discovered during analysis.

---

## Summary Table

| OWASP ID | Risk Category | Status |
|--------|---------------|--------|
| M1 | Improper Platform Usage | Not Identified |
| M2 | Insecure Data Storage | Identified |
| M3 | Insecure Communication | Identified |
| M4 | Insecure Authentication | Identified |
| M5 | Insufficient Cryptography | Identified |
| M6 | Insecure Authorization | Not Identified |
| M7 | Client Code Quality | Identified |
| M8 | Code Tampering | Not Identified |
| M9 | Reverse Engineering | Identified |
| M10 | Extraneous Functionality | Not Identified |
