# Privacy Policy

**Grenadier OBD2**
**Last updated: May 24, 2026**

---

## Overview

Grenadier OBD2 is a diagnostic companion app exclusively designed for INEOS Grenadier vehicles. We are committed to handling your data with transparency and respect. This policy explains what data we collect, why we collect it, and how it is protected.

---

## What We Collect and Why

### 1. Vehicle Identification Number (VIN)
When you first launch the app, we read your vehicle's VIN via the OBD2 interface. The VIN is used solely to **verify and activate your app license** — confirming that the app is being used with a genuine INEOS Grenadier vehicle. Your VIN is stored securely in our license database and is never shared with third parties.

### 2. Anonymous Vehicle Metrics
To improve future versions of the app, we collect diagnostic data and vehicle configuration details from your Grenadier. This data is collected **entirely anonymously** using a one-way cryptographic process:

- Your VIN is converted into a **vehicle_uuid** using the SHA-256 hashing algorithm
- SHA-256 is a one-way function — it is mathematically impossible to reverse a vehicle_uuid back to the original VIN
- All collected metrics (sensor readings, configuration details, fault codes, etc.) are stored in a separate vehicle database linked only to this anonymous vehicle_uuid
- Your raw VIN is **never stored** in the vehicle metrics database

This approach — known as pseudonymisation — means that even in the unlikely event of a data breach, no vehicle identity or owner information could ever be recovered from the metrics database.

### 3. Purpose of Data Collection
This first version of Grenadier OBD2 is an **exploratory release**. Its primary goal is to discover and document the wide variety of vehicle configurations found in INEOS Grenadier models worldwide — different markets, model years, option packages, and regional specifications. The insights gained will directly shape the next version of the app, making it more accurate, meaningful, and useful for all Grenadier owners globally.

---

## What We Do NOT Collect

- No personal information (name, email, address, phone number)
- No location or GPS data
- No driving behavior or journey data
- No payment information
- No data from any source other than your vehicle's OBD2 interface

---

## Data Storage and Security

| Data | Storage | Linked to you? |
|---|---|---|
| VIN | Secure license database | Yes — for license verification only |
| Vehicle metrics | Anonymous vehicle database | No — linked to SHA-256 derived vehicle_uuid only |

All data is transmitted over encrypted connections (TLS) and stored on secured servers. Your VIN is never stored alongside your vehicle metrics, and the SHA-256 transformation ensures this separation is cryptographically guaranteed.

---

## Your Rights

You may request at any time:
- **Access** to what data we hold about your vehicle
- **Deletion** of your VIN from our license database
- **Deletion** of your anonymous vehicle data (provide your vehicle_uuid from the app settings)

To make a request, contact us at the email address below.

---

## Third Parties

We do not sell, rent, or share your data with any third party for commercial purposes. No advertising networks or analytics platforms receive your data.

---

## Children's Privacy

This app is not directed at children under the age of 13 and we do not knowingly collect data from minors.

---

## Changes to This Policy

If we make material changes to this privacy policy, we will update the "Last updated" date above and notify users via the app. Continued use of the app after changes constitutes acceptance of the revised policy.

---

## Contact

If you have any questions or requests regarding your privacy, please contact:

**Dieter Reuter**
📧 dieter.reuter@icloud.com

