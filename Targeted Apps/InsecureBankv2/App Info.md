# Application Recon — InsecureBankv2

## Application Overview
InsecureBankv2 is a deliberately vulnerable Android banking application designed for security testing and training purposes. The app simulates basic banking functionality and communicates with a backend service.

## Observed Features
- User login screen
- Credential-based authentication
- Network-dependent functionality
- Banking-style UI elements (accounts / transactions context)
![alt text](Screenshot_20260112_025602.png)

## Authentication Flow
- User is prompted for username and password.
- Authentication is performed after input submission.
- Error messages are displayed on invalid login attempts.
- No multi-factor authentication observed.

## Backend Dependency Observation
- Application login functionality depends on a backend API server.
- When backend is unavailable, login attempts produce no visible response.
- Application does not clearly inform the user of backend connectivity issues.

## Runtime Behavior
- Application requires network connectivity to function.
- App launches without crash and remains stable during basic interaction.
- Login attempts with invalid credentials return application-level responses.

## Permissions (Initial Recon)
- INTERNET permission: Present
- Other permissions: To be reviewed during manifest analysis

## Security-Relevant Observations (Non-conclusive)
- App heavily relies on client-side interaction before server response.
- No visible protections such as CAPTCHA, rate limiting, or secondary verification.
- Designed to demonstrate insecure mobile application patterns.

> This document records behavioral observations only.  
> No vulnerabilities are asserted at this stage.
