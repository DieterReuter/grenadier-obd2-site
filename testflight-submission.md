# TestFlight Submission Details
**App:** Grenadier OBD2
**Bundle ID:** net.perlan.GrenadierOBD
**Last updated:** May 24, 2026

---

## Versioning Convention

| Stage | Version | Description |
|---|---|---|
| Alpha-0 | 0.8.0 | First TestFlight, invited alpha testers only |
| Alpha-1 | 0.8.1 | First iteration based on Alpha-0 feedback |
| Alpha-2 | 0.8.2 | Second iteration |
| Beta | 0.9.0 | Broader TestFlight, feature complete |
| Release Candidate | 0.9.x | Final polish before App Store |
| App Store Launch | 1.0.0 | Public release |

---

## App Information (App Store Connect)

| Field | Value |
|---|---|
| Name | Grenadier OBD2 |
| Bundle ID | net.perlan.GrenadierOBD |
| Category | Utilities |
| Privacy Policy URL | https://dieterreuter.github.io/grenadier-obd2-site/privacy-policy.html |

---

## Beta App Information

**Beta App Description:**
Grenadier OBD2 is the first dedicated diagnostic app for INEOS Grenadier owners. Using a standard Bluetooth Low Energy (BLE) ELM327 OBD2 adapter, the app connects directly to your vehicle to read live sensor data, explore your Grenadier's unique configuration, and retrieve fault codes — all from your iPhone. This first release focuses on discovery: understanding the full range of Grenadier configurations worldwide to build a richer, more powerful experience in the next version.

**Feedback Email:** dieter.reuter@icloud.com

**Marketing URL:** *(leave empty)*

**Privacy Policy URL:** https://dieterreuter.github.io/grenadier-obd2-site/privacy-policy.html

---

## What to Test (per build, in TestFlight → Builds)

This is an early exploratory build — your feedback directly shapes the next version of the app.

**Recommended BLE OBD2 Devices**
- vLinker BM+ — fully compatible, recommended
- vLinker MC+ — fully compatible, recommended

**Additional BLE OBD2 Devices**
- OBDLink CX — limited support, more testing required
- Vgate iCar Pro Bluetooth 4.0 (BLE) — limited support, more testing required

Please test with a physical INEOS Grenadier and one of the recommended BLE OBD2 dongles listed above. We'd love to know:
- Does the BLE Discovery find your OBD2 dongle reliably?
- Does the app connect successfully and show the live voltage reading?
- Is your VIN read and displayed correctly after turning on the ignition?
- Which ECUs does **Probe ECUs** detect in your specific Grenadier variant?
- Do you notice any missing data, crashes, or unexpected behaviour?

All vehicle data collected during testing is fully anonymised — your VIN is never stored alongside your vehicle metrics.

---

## Beta App Review Information

**Contact Information**
| Field | Value |
|---|---|
| First Name | Dieter |
| Last Name | Reuter |
| Phone | *(your phone number)* |
| Email | dieter.reuter@icloud.com |

**Sign-in required:** No

**Review Notes:**

> **Requirements**
> - A physical INEOS Grenadier vehicle
> - A Bluetooth Low Energy (BLE) ELM327 OBD2 dongle (see recommended devices below)
> - An iPhone with Bluetooth enabled
>
> **Note for Apple Reviewers:** This app requires a real vehicle connection and cannot be tested in the simulator or without OBD2 hardware.
>
> **Recommended BLE OBD2 Devices**
> - vLinker BM+ — fully compatible, recommended
> - vLinker MC+ — fully compatible, recommended
>
> **Additional BLE OBD2 Devices**
> - OBDLink CX — limited support, more testing required
> - Vgate iCar Pro Bluetooth 4.0 (BLE) — limited support, more testing required
>
> **Getting Started**
> 1. Plug your BLE OBD2 dongle into the vehicle's OBD2 port — leave the ignition off for now
> 2. Open the app and go to **Settings**
> 3. Tap **BLE Discovery** to scan for nearby BLE devices
> 4. Select your OBD2 dongle from the list — the app will verify compatibility
> 5. Once verified, tap **Register** to save the device
> 6. Return to the main screen and tap **Connect**
> 7. After a few seconds the live voltage reading from the OBD2 device confirms a successful connection
> 8. Turn on the ignition and wait a few seconds — the app will read and display your vehicle's VIN
> 9. Tap **Probe ECUs** to discover which Electronic Control Units are active and online in your vehicle

---

## License Agreement

*(Leave empty — no custom EULA)*

---

## Recommended BLE OBD2 Devices (Reference)

| BLE Device Name | Product Name | Status | Notes |
|---|---|---|---|
| vLinker BM-IOS | vLinker BM+ | ✅ Fully compatible | Recommended |
| vLinker MC-IOS | vLinker MC+ | ✅ Fully compatible | Recommended |
| OBDLink CX | OBDLink CX | ✅ Fully compatible | limited support, more testing required |
| IOS-Vlink | Vgate iCar Pro Bluetooth 4.0 (BLE) | ✅ Fully compatible | limited support, more testing required |

---

## Version History

| Version | Build | Date | Stage | Notes |
|---|---|---|---|---|
| 0.8.0 | 1 | 2026-05-24 | Alpha-0 | First TestFlight, invited alpha testers only |
