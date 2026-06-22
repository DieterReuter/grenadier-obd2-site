# TestFlight Submission Details
**App:** Grenadier OBD2
**Bundle ID:** net.perlan.GrenadierOBD
**Last updated:** June 20, 2026

---

## Versioning Convention

| Stage | Version | Description |
|---|---|---|
| Alpha-0 | 0.8.0 | First TestFlight, invited alpha testers only |
| Alpha-1 | 0.8.1 | First iteration based on Alpha-0 feedback |
| Alpha-2 | 0.8.2 | Second iteration |
| Alpha-3 | 0.8.3 | Third iteration |
| Alpha-4 | 0.8.4 | Fourth iteration |
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
Grenadier OBD2 is the first dedicated diagnostic app for INEOS Grenadier owners. Using a standard Bluetooth Low Energy (BLE) ELM327 OBD2 adapter, the app connects directly to your vehicle to read live sensor data, explore your Grenadier's unique configuration, and retrieve fault codes -- all from your iPhone. This first release focuses on discovery: understanding the full range of Grenadier configurations worldwide to build a richer, more powerful experience in the next version.

**Feedback Email:** dieter.reuter@icloud.com

**Marketing URL:** *(leave empty)*

**Privacy Policy URL:** https://dieterreuter.github.io/grenadier-obd2-site/privacy-policy.html

---

## What to Test (per build, in TestFlight -> Builds)

### v0.8.4 (Alpha-4)

What to Test -- Alpha-4 (v0.8.4)

Focus: PDF Diagnosis Report, Odometer, Service Reminder, TPMS Information, Stability

What's New in This Build

- NEW: Export Diagnosis Report -- a new button on the main screen
  generates a PDF with your vehicle details, service reminder and tyre sensor IDs.
  Share it via email, AirDrop, or save to Files.
- NEW: Odometer reading shown in km and miles on the main screen,
  read directly from the ECU (BCM, DDE and Head Unit all cross-checked)
- NEW: Service Reminder - just have a look
- Improved: Connect flow is faster -- VIN and odometer read in under 2 seconds
- Improved: TPMS reads are more reliable

Test Steps

1. Connect to your Grenadier and verify VIN is read correctly
2. Check the odometer shows your current km and miles -- compare
   with your dashboard, both should match
3. My Grenadier -- fill in your exact vehicle details now, before
   generating the PDF, as this data will be printed in the report
   - Model Year: your MY (e.g. MY23, MY24, MY25, MY26)
   - Body Style: Standard 5-Seater, Standard 2-Seater,
     Quartermaster, or Quartermaster Chassis Cab
   - Engine: Diesel or Petrol
   - Drive: LHD or RHD
   - Trim: Standard, Fieldmaster, Trialmaster, Trialmaster X, 1924 Edition, or Black Edition
   - Country: your country
   - Market: your market (e.g. EU, UK, US, AU)
   - Leave the screen -- it saves automatically
   - Reopen My Grenadier and confirm everything was saved correctly
4. Service Reminder (main screen card)
   - Tap "Read Service Details" with ignition ON
   - Check card "Remaining Until Service" data
   - Compare with the details from for Head Unit
   - If there is a difference in Days and Engine Hours, 
     click on Calibrate and correct those values!
   - Close the app and reopen Service Reminder -- confirm last reading is still shown
5. TPMS Information (main screen card)
   - Tap "Read TPMS Sensor Details" with ignition ON
   - Check all 5 sensor IDs and pressures match your head unit
   - Tap a tyre card to open Tyre Sensor Details -- check the car
     pictogram highlights the correct wheel
   - Close the app and reopen TPMS -- confirm last reading is still shown
6. Export Diagnosis Report (NEW!)
   - Tap "Export Diagnosis Report" on the main screen
   - Wait a few seconds while the PDF is generated
   - Share it via email or AirDrop to check it looks correct
   - Verify your VIN, model year, engine, odometer km/miles,
     My Grenadier details and TPMS sensor IDs are all correct
7. Grenadier Details -- check all rows look correct for your car
8. Then explore the app and let us know what you think!

Please Report

- Which adapter you are using
- Whether the PDF export worked and the data looks correct
- Any odometer reading that looks wrong (check against your dashboard)
- Any Details in Service Reminder are wrong
- Any TPMS sensor ID or pressure that looks wrong
- Anything that looks wrong or unexpected

Recommended BLE OBD2 Adapters (BLE device name)
- vLinker BM+ (vLinker BM-IOS)
- vLinker MC+ (vLinker MC-IOS)
- Vgate iCar Pro BLE (IOS-Vlink)
- OBDLink CX (OBDLink CX)

---

### v0.8.3 (Alpha-3)

**Focus:** ECU Discovery & Details, TPMS, My Grenadier

**What's New / Fixed in This Build**

- **Fixed:** ACM and BCM CAN addresses were swapped throughout the app — ECU names and addresses are now correct (ACM=0x688/0x608, BCM=0x681/0x601)
- **New:** TPMS Information screen — read tyre sensor IDs, live pressure and temperature (bar/psi, °C/°F), plus reference pressure
- **New:** Tap any tyre on the TPMS screen for Tyre Sensor Details (full sensor ID for cloning, pressure/temp, car position pictogram)
- **New:** TPMS results are cached on your phone — you can review the last reading even offline, without being connected to the car
- **New:** My Grenadier — added Seating (5-Seater / 2-Seater), simplified Type of Use (Passenger / Commercial / Quartermaster / Prototype), added MY22 and MY27 to Model Year
- **Changed:** My Grenadier now saves automatically when you leave the screen — no more separate "Confirm & Save" button
- **Updated:** VIN decoding — covers more markets, model years and prototype VINs

**Test Steps**

1. Connect to your Grenadier and verify VIN is read correctly
2. Probe ECUs — confirm all ECUs show as online
3. ECU Discovery (Settings → ECU Discovery → Scan)
   - Verify all ECUs found (17 on Diesel, 16 on Petrol — even more on MY24/25/26)
   - EGS, GWS shown green with EX: address
   - SCR shown on Diesel, absent on Petrol
   - Confirm ACM and BCM both show online with correct addresses
4. Read Details on every ECU — tap Details on each one and wait for it to complete
   - Look for green checkmark after each read
   - Report any ECU that shows all — or fails to read
5. TPMS Information (main screen card)
   - Tap "Read TPMS Sensor Details" with ignition ON
   - Check all 5 sensor IDs, pressures (bar/psi) and temps (°C/°F) match your head unit's tyre pressure screen
   - Tap a tyre card to open Tyre Sensor Details — check the car pictogram highlights the correct wheel
   - Close the app and reopen TPMS — confirm last reading is still shown
6. Vehicle Details — check all rows look correct for your car
7. My Grenadier — set Seating, Type of Use, Market, Trim, Country, then leave the screen and reopen — confirm everything was saved
8. Then explore the app and let us know what you think!

**Please Report**
- Which adapter you're using
- Any ECU that failed to read Details
- Any TPMS sensor ID, pressure or temperature that looks wrong
- Anything that looks wrong or unexpected

**Recommended BLE OBD2 Adapters**
- vLinker BM+ (vLinker BM-IOS) — recommended
- vLinker MC+ (vLinker MC-IOS) — recommended
- Vgate iCar Pro BLE (IOS-Vlink) — recommended
- OBDLink CX — works

---

### v0.8.2 build 19 (Alpha-2b)

This build adds UX improvements to the My Grenadier screen based on Alpha-2 tester feedback.

**What's new in build 19**

- **My Grenadier guided workflow** — the My Grenadier card on the main screen now shows a clear 3-step guide: 1. Probe ECUs → 2. Fill in My Grenadier and submit → 3. Run ECU Discovery. Following this order gives us the best data!
- **Nudge badge** — an orange dot appears on the My Grenadier card when your vehicle is connected but you haven't submitted your configuration yet. It disappears once submitted.
- **Picker layout** — the picker fields in My Grenadier are now easier to read with a smaller font and better spacing

Please follow these 3 steps after connecting your Grenadier:
1. Probe ECUs
2. Fill in My Grenadier and submit
3. Run ECU Discovery

Then explore the app and let us know what you think!

---

### v0.8.2 build 18 (Alpha-2)

This build focuses on vehicle identification improvements and a new My Grenadier configuration screen.

**What's new in 0.8.2**

- **My Grenadier** — a new screen to configure your exact vehicle setup. Tap "My Grenadier" on the main screen after connecting to your Grenadier. The app pre-fills what it can from your VIN — just confirm or correct the details and save. This helps us improve VIN decoding for every Grenadier owner worldwide!
- **Country** — select your country from a full searchable list with flag emojis
- **ECU Inventory** — DDE and DME are now shown as a single entry. Before VIN is read it shows "DDE/DME — Diesel/Petrol". Once your VIN is read it updates to the correct name and variant label
- **FCM (Front Camera Module)** — added to ECU Inventory for MY24+ vehicles
- **Drive** — LHD or RHD is now correctly detected from your VIN and shown in Grenadier Details
- **Engine Type** — correct BMW engine code shown (B57D30 for Diesel, B58B30 for Petrol)
- **Hide VIN** — new privacy toggle in Settings, replaces last 5 digits with 00000 for screenshots

**Please test and confirm:**
- Does My Grenadier pre-fill your model year, body style, engine and drive correctly?
- Does the country field pre-select your country from iOS settings?
- Does the Confirm & Save button only activate when you change something?
- Does the Drive field show correctly for your vehicle (LHD or RHD)?
- Does the ECU Inventory show the correct Diesel or Petrol label after VIN is read?
- MY24+ only: Does FCM show as online in the ECU Inventory after Probe ECUs?
- US cars: Does FCM now appear in your ECU list? We know it was missing before!
- Does Hide VIN work correctly — do the last 5 digits show as 00000?

**Recommended BLE OBD2 Devices**
- vLinker BM+ — fully compatible, recommended
- vLinker MC+ — fully compatible, recommended
- Vgate iCar Pro Bluetooth 4.0 BLE — fully compatible, recommended

**Additional BLE OBD2 Devices**
- OBDLink CX — limited support, more testing required

All vehicle data collected is fully anonymised — your VIN is never stored alongside your vehicle metrics.

---

### v0.8.1 (Alpha-1)

This is an early exploratory build — your feedback directly shapes the next version of the app.

**Recommended BLE OBD2 Devices**
- vLinker BM+ — fully compatible, recommended
- vLinker MC+ — fully compatible, recommended

**Additional BLE OBD2 Devices**
- OBDLink CX — limited support, more testing required
- Vgate iCar Pro Bluetooth 4.0 BLE — limited support, more testing required

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
> - Vgate iCar Pro Bluetooth 4.0 BLE — fully compatible, recommended
>
> **Additional BLE OBD2 Devices**
> - OBDLink CX — limited support, more testing required
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
| vLinker BM-IOS | vLinker BM+ | Fully compatible | Recommended |
| vLinker MC-IOS | vLinker MC+ | Fully compatible | Recommended |
| IOS-Vlink | Vgate iCar Pro Bluetooth 4.0 (BLE) | Fully compatible | Recommended |
| OBDLink CX | OBDLink CX | Fully compatible | works |

---

## Version History

| Version | Build | Date | Stage | Notes |
|---|---|---|---|---|
| 0.8.0 | 1 | 2026-05-24 | Alpha-0 | First TestFlight, invited alpha testers only |
| 0.8.1 | -- | 2026-05-25 | Alpha-1 | Petrol detection, Drive removed, Vehicle UUID, ECU DME/DDE placeholder |
| 0.8.2 | 17 | 2026-05-29 | Alpha-2 | ECU DME/DDE single entry, Hide VIN, Drive LHD/RHD, Engine type fix, FCM |
| 0.8.2 | 18 | 2026-05-30 | Alpha-2 | My Grenadier screen, country field, vehicleConfig logging |
| 0.8.2 | 19 | 2026-06-02 | Alpha-2b | Picker font fix, nudge badge, CTA guided workflow |
| 0.8.3 | -- | 2026-06-14 | Alpha-3 | ACM/BCM address swap fix, TPMS feature (sensor IDs, pressure, temp, Tyre Sensor Details), My Grenadier Seating/Type of Use redesign, auto-save on exit, VIN decoding update |
| 0.8.4 | -- | 2026-06-20 | Alpha-4 | PDF Diagnosis Report export, Odometer reading (BCM+DDE+HU majority vote), connect flow faster, ECU Discovery + Details stability improvements |
