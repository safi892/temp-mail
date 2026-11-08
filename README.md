# TempMailCode — Free Temp Mail & OTP Verification Engine

[![Live Website](https://img.shields.io/badge/Live_Website-tempmailcode.com-2fd6c3?style=for-the-badge&logo=googlechrome&logoColor=black)](https://tempmailcode.com/)
[![Developer API](https://img.shields.io/badge/Developer_API-OpenAPI_3.1-6366f1?style=for-the-badge&logo=openapiinitiative&logoColor=white)](https://tempmailcode.com/api)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)](https://tempmailcode.com/terms)

> **[TempMailCode.com](https://tempmailcode.com/)** provides free, instant, disposable temporary email addresses with automatic OTP (One-Time Password) and verification code extraction. No registration, no password, no tracking.

---

## ⚡ What is TempMailCode?

When registering for forums, software trials, or public WiFi portals, services demand an email address to send an activation code. Using your personal inbox exposes you to tracking pixels, data leaks, and promotional newsletters.

**[TempMailCode](https://tempmailcode.com/)** solves this by generating an ephemeral mailbox on demand with an in-memory catch-all SMTP server. Instead of forcing you to hunt through spam-filled HTML emails, the engine automatically extracts the **4 to 8 digit verification code** and displays it in a single-click copy button.

### 🌟 Key Features
* **Zero Signup:** A random temporary mailbox is generated immediately on page load.
* **Automatic Code Extraction:** Extracts OTPs, confirmation tokens, and activation PINs with regex heuristics.
* **Privacy by Design:** Remote tracking pixels and images are blocked by default.
* **RAM-Only Lifecycle:** Emails are stored strictly in volatile memory and deleted automatically after 60 minutes.
* **Receive-Only:** Cannot be abused for outbound spamming.
* **Blocklist Mitigation:** Automatic domain rotation and wildcard subdomains ensure verification codes arrive smoothly.

---

## 🛠️ Developer REST API

Looking to automate user onboarding tests in Playwright, Cypress, or Selenium? **TempMailCode** provides a credentialed JSON REST API.

* **Documentation & Endpoints:** [https://tempmailcode.com/api](https://tempmailcode.com/api)
* **OpenAPI 3.1 Specification:** `https://tempmailcode.com/api/v1/openapi.json`

### Quick cURL Example
```bash
# 1. Claim a temporary address
curl -X POST https://tempmailcode.com/api/v1/addresses \
  -H "Authorization: Bearer $API_KEY" \
  -H "Content-Type: application/json" -d '{}'

# 2. Poll messages (OTP code is surfaced on messages[0].otp directly)
curl -H "Authorization: Bearer $API_KEY" \
  "https://tempmailcode.com/api/v1/addresses/YOUR_ADDRESS/messages"
```

---

## 📚 Architectural Resources
* **Official Website:** [https://tempmailcode.com/](https://tempmailcode.com/)
* **Developer API Reference:** [https://tempmailcode.com/api](https://tempmailcode.com/api)
* **Temp Mail vs Email Aliases Guide:** [https://tempmailcode.com/guide](https://tempmailcode.com/guide)
* **Privacy Policy & Retention Limits:** [https://tempmailcode.com/privacy](https://tempmailcode.com/privacy)

---

## ⚖️ License & Terms
The public documentation and client showcase is open-sourced under the MIT License. The live mail delivery service is governed by the [Terms of Use](https://tempmailcode.com/terms).
