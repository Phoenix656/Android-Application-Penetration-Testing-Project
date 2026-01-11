# Methodology – Runtime Instrumentation

## Objective
To analyze and manipulate application behavior at runtime in order to identify excessive client-side trust and weak security controls.

---

## Approach
Runtime instrumentation was performed using dynamic hooking techniques to observe and influence application execution without modifying the APK.

---

## Steps Performed

1. Runtime Attachment
   - The application process was identified on the emulator.
   - A runtime instrumentation tool was attached to the running application.

2. Method Hooking
   - Application methods related to authentication and validation were hooked.
   - Runtime values and method calls were observed.

3. Security Control Bypass
   - Client-side checks were bypassed to test trust boundaries.
   - Application behavior after bypass was analyzed.

4. Runtime Observation
   - Memory and method execution flow were inspected.
   - Impact of client-side trust decisions was evaluated.

---

## Tools Used
- Frida
- Objection

---

## Outcome
Runtime instrumentation demonstrated that critical security decisions were enforced on the client side and could be bypassed during execution.
