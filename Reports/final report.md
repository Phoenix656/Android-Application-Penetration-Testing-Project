# Android Application Penetration Testing Report

## Project Title
Android Application Penetration Testing of InsecureBankv2

---

## Executive Summary
This report documents the results of an Android application penetration test conducted on **InsecureBankv2**, an intentionally vulnerable application designed for security training.  

The objective of this assessment was to identify common mobile application security weaknesses using a structured methodology aligned with OWASP Mobile Security guidelines. The testing was performed in a controlled lab environment for educational purposes only.

---

## Target Application Details

- Application Name: InsecureBankv2
- Package Name: com.android.insecurebankv2
- Platform: Android
- Environment: Android Emulator (API 28)
- Assessment Type: Educational / Ethical Penetration Testing

---

## Scope of Assessment
The assessment was limited to the following:

- Static analysis of the application APK
- Dynamic analysis of runtime behavior
- Client-side security assessment
- OWASP Mobile Top 10 mapping

Out-of-scope activities included testing of real-world applications, unauthorized systems, and production environments.

---

## Methodology
The assessment followed a phased approach:

1. Lab Setup and Environment Configuration  
2. Static Analysis using decompilation techniques  
3. Dynamic Analysis of application behavior  
4. Runtime Instrumentation  
5. OWASP Mobile Top 10 Mapping  
6. Documentation and Reporting  

Detailed methodology steps are documented in the `methodology/` directory.

---

## Summary of Findings

| ID | Finding | Description |
|----|--------|------------|
| F-01 | Insecure Communication | Application communicates with backend services over HTTP |
| F-02 | Insecure Local Storage | Sensitive data may be stored locally without encryption |
| F-03 | Excessive Client-Side Trust | Authentication relies heavily on client-side logic |
| F-04 | Hardcoded Endpoints | Backend API endpoints embedded in client code |
| F-05 | Lack of Code Obfuscation | Application is easily reverse engineered |

---

## OWASP Mobile Top 10 Mapping

| OWASP ID | Risk Category | Status |
|--------|---------------|--------|
| M2 | Insecure Data Storage | Identified |
| M3 | Insecure Communication | Identified |
| M4 | Insecure Authentication | Identified |
| M5 | Insufficient Cryptography | Identified |
| M7 | Client Code Quality | Identified |
| M9 | Reverse Engineering | Identified |

Detailed mapping is available in `owasp-mapping/owasp-mobile-top-10.md`.

---

## Risk Assessment
The identified vulnerabilities collectively indicate a **weak security posture**, particularly in areas involving data protection and communication security.  

If present in a real-world application, these issues could expose sensitive user data and enable unauthorized access.

---

## Remediation Summary
Key remediation actions include:

- Enforcing HTTPS with TLS for all communications
- Encrypting sensitive data stored locally
- Reducing client-side trust and enforcing server-side validation
- Removing hardcoded configuration values
- Applying code obfuscation techniques

Detailed remediation guidance is provided in `remediation/recommendations.md`.

---

## Conclusion
This assessment demonstrates how common security flaws can be identified in Android applications through structured penetration testing techniques.  

The project highlights the importance of secure communication, data protection, and defensive coding practices in mobile application development.

---

## Disclaimer
This report is intended strictly for educational purposes.  
All testing was conducted on an intentionally vulnerable application in a controlled lab environment. No real-world systems or user data were involved.
