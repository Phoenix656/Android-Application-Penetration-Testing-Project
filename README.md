# Android Application Penetration Testing

## Project Overview
This repository documents an Android application penetration testing assessment conducted on **InsecureBankv2**, an intentionally vulnerable application designed for security training and educational purposes.

The project follows a structured methodology aligned with **OWASP Mobile Security Testing Guide (MSTG)** and demonstrates how common Android security weaknesses can be identified through static and dynamic analysis.

---

## Objectives
- Understand Android application attack surfaces
- Perform static and dynamic security analysis
- Identify insecure design and implementation patterns
- Map findings to OWASP Mobile Top 10
- Propose effective remediation strategies
- Document a complete mobile penetration testing workflow

---

## Target Application
- Application Name: InsecureBankv2  
- Package Name: com.android.insecurebankv2  
- Platform: Android  
- Testing Environment: Android Emulator (API 28)  

The target application is intentionally vulnerable and used strictly for educational purposes.

---

## Repository Structure

Android-Application-Penetration-Testing/

├── README.md

│

├── lab-setup/

│ ├── environment.md

│ └── tools.md

│

├── scope-and-ethics/

│ ├── scope.md

│ └── ethics.md

│

├── target-apps/

│ └── insecurebankv2/

│ ├── app-info.md

│ └── apk-details.md

│

├── methodology/

│ ├── static-analysis.md

│ ├── dynamic-analysis.md

│ └── runtime-instrumentation.md

│

├── findings/

│ ├── hardcoded-endpoints.md

│ ├── insecure-communication.md

│ ├── insecure-local-storage.md

│ └── client-side-auth-trust.md

│

├── owasp-mapping/

│ └── owasp-mobile-top-10.md

│

├── remediation/

│ └── recommendations.md

│

├── reports/

└── final-report.md


---

## Methodology Summary
The assessment was conducted using a phased approach:

1. Lab Environment Setup  
2. Static Analysis (APK decompilation and code inspection)  
3. Dynamic Analysis (runtime behavior and network traffic observation)  
4. Runtime Instrumentation  
5. OWASP Mobile Top 10 Mapping  
6. Remediation and Reporting  

Detailed steps are documented in the `methodology/` directory.

---

## Key Findings
- Insecure communication over HTTP
- Insecure local storage without encryption
- Excessive client-side trust in authentication flow
- Hardcoded backend endpoints
- Lack of code obfuscation

Detailed findings are available in the `findings/` directory.

---

## OWASP Mobile Top 10 Coverage
Identified issues were mapped to relevant OWASP Mobile Top 10 categories, including:
- M2: Insecure Data Storage
- M3: Insecure Communication
- M4: Insecure Authentication
- M5: Insufficient Cryptography
- M7: Client Code Quality
- M9: Reverse Engineering

Full mapping is available in `owasp-mapping/owasp-mobile-top-10.md`.

---

## Remediation
Actionable remediation steps are provided for each identified issue, focusing on:
- Secure communication using TLS
- Encryption of sensitive data
- Reducing client-side trust
- Secure configuration management
- Code obfuscation and hardening

See `remediation/recommendations.md` for details.

---

## Report
A consolidated penetration testing report summarizing scope, methodology, findings, OWASP mapping, and remediation is available at:

reports/final-report.md

---

## Ethics & Disclaimer
This project was conducted strictly for educational purposes using an intentionally vulnerable application in a controlled lab environment.

- No real-world applications were tested
- No production systems were accessed
- No real user data was involved

Refer to `scope-and-ethics/` for full details.

---

## Conclusion
This repository demonstrates a complete Android application penetration testing workflow and highlights common security weaknesses found in mobile applications. It serves as a learning resource for understanding Android security testing methodologies and best practices.

---



