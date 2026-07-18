# TestFlight Submission Details
**App:** Grenadier OBD2
**Bundle ID:** net.perlan.GrenadierOBD
**Last updated:** July 18, 2026

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

### v0.9.0 Build 50 (Beta-2b)

What to Test — Beta-2b (v0.9.0, Build 50)

Focus: Same walkthrough as Beta-1 below — this is a maintenance build with one reliability
improvement, nothing new to try. Everything from Beta-2 stays the same.

Improved in Beta-2b
- Your saved vehicle data — Service Reminder, TPMS Information, ECU Information, DTC history,
  and My Grenadier details — now reliably carries over when you update the app to a newer
  build. Previously a data cache could be dropped on update, forcing a fresh read; that's
  fixed, so your cached figures stay put across updates.

### v0.9.0 Build 49 (Beta-2)

What to Test — Beta-2 (v0.9.0, Build 49)

Focus: New feature — ECU Information. Same walkthrough as Beta-1 below, plus one new card to try.

New in Beta-2
- ECU Information: a new card on the main screen that reads the hardware and software part
  numbers and version details from every module in your Grenadier — the same identification
  data a workshop tool reads.

Test Steps (in addition to the Beta-1 walkthrough)
1. Connect to your Grenadier in Key On, Engine Off (KOEO).
2. Tap "ECU Information" and let it read.
3. Check each ECU shows its part numbers / software versions. Please report any ECU that shows
   no data or looks wrong.

### v0.9.0 Build 48 (Beta-1d)

What to Test — Beta-1d (v0.9.0, Build 48)

Focus: Same walkthrough as Beta-1 below — this build fixes a Service Reminder issue several
of you reported. If you hit this before, please try again on this build.

Fixed in Beta-1d
- Service Reminder: "Remaining Distance" and "Remaining Engine Hours" could show "—" after
  you calibrated, even though your calibration was saved correctly. Fixed.
- Service Reminder: "Read Service Details" could occasionally do nothing when tapped, with
  no feedback at all. It now shows a message if a read fails, so you know to try again.

### v0.9.0 Build 47 (Beta-1c)

What to Test — Beta-1c (v0.9.0, Build 47)

Focus: Same walkthrough as Beta-1 below — this build fixes a couple more small issues
and improves My Grenadier. If you hit any of these before, please try again on this build.

Fixed in Beta-1c
- My Grenadier: Country and Market now pre-fills automatically based on your phone's region (you can
  still change it if it's wrong for your car).
- Diagnosis Report: fixed the "Engine" row on page 1,
  showing incorrect or garbled text for certain engine variants.

### v0.9.0 Build 46 (Beta-1b)

What to Test — Beta-1b (v0.9.0, Build 46)

Focus: Same walkthrough as Beta-1 below — this build fixes issues reported by testers
using Build 45, plus a couple of speed and polish improvements. If you hit any of these
before, please try again on this build.

Fixed in Beta-1b
- Adapter setup screen could get stuck for testers who had already registered an adapter in
  an earlier build — no way to reach Connect. Fixed.
- Service Reminder could hang after "Read Service Details," with no new data even after
  retrying several times. Fixed — also faster now.
- The "Calibrate at least once" reminder on Service Reminder no longer keeps showing after
  you've already calibrated.
- TPMS Information reads a bit faster.
- "Adapter busy" popup no longer appears unexpectedly in the middle of "Probe ECUs."
- TPMS and Service Reminder both read a bit faster still (removed a couple of unnecessary
  round trips).

What to Test — Beta-1 (v0.9.0)

Focus: Welcome to the Beta! This is your first walkthrough of the app — follow the steps
below in order to see everything it can do for your Grenadier.

Test Steps

1. Scan for your BLE OBD2 adapter, tap it to test compatibility, then tap Add to
   register it. Tap Connect.
2. Turn your key to Key On, Engine Off (KOEO) — do not start the engine.
3. The app automatically reads your VIN, Odometer, Engine Hours, and Last Engine Run.
4. Tap "Probe ECUs" to determine all the modules that are online in your Grenadier.
5. Open the Grenadier Card info ("i" icon), tap "My Grenadier", and fill in the empty
   fields — this is information only you know as the owner; the app can't read it from
   the car's ECUs.
6. Tap "TPMS Information" and read your TPMS sensor details — you'll see all four tyre
   sensor IDs plus the spare, and their positions.
7. Tap "Service Reminder", then tap "Read Service Details" to read your service data. Then
   tap "Calibrate" and enter the three values shown on your Grenadier's own "Service Interval"
   screen — the app can't read these directly from the ECUs.
8. Tap "ECU Health Check", then tap "Read ECU Health Check" to read all DTCs (fault codes)
   across your vehicle.
9. Finally, tap "Export Diagnosis Report" to create a PDF with all the vehicle data you
   just collected in the steps above.

Please Report

- Which adapter you used (BLE device name)
- Did each step above work as described, in the order given?
- Anything confusing, unclear, or that didn't behave as expected
- Any screen that showed no data or looked broken

Recommended BLE OBD2 Adapters
- OBDLink CX (OBDLink CX)
- vLinker BM+ (vLinker BM-IOS)
- vLinker MC+ (vLinker MC-IOS)

---

### v0.8.6 (Alpha-6)

What to Test — Alpha-6 (v0.8.6)

Focus: First-run adapter onboarding, BLE stability, quality-of-life fixes

What's New in Alpha-6
- NEW: Guided adapter setup — on first launch the app walks you through
  connecting your BLE OBD2 adapter step by step. All features are hidden
  until your adapter is registered, so there's nothing confusing to tap.
  Recommended adapters (OBDLink CX, vLinker BM+, vLinker MC+) are shown
  right on the setup card.
- NEW: "Adapter busy — tap again" toast — a small message now appears at
  the bottom of the screen if you tap a feature while the adapter is mid-read,
  instead of silently doing nothing.
- NEW: ECU Discovery Details button dims to gray when the engine is running
  (ECU identification requires engine off — the button now makes this obvious).
- NEW: Informational banners on the main screen — if the engine is running,
  ignition is off, or the adapter can't be found, a banner now explains why
  and what to do. No more guessing why a feature isn't responding.

Fixed in Alpha-6
- BLE reconnect: turning ignition on/off after a BLE drop (going out of
  range and back) could freeze the ignition state display — fixed.
- Connect while engine running: if the engine was already running when the
  app connected, it incorrectly showed "ignition off" for several seconds —
  fixed.
- TPMS: tapping Read when the adapter was busy showed "Not connected"
  instead of "Adapter busy" — fixed.

Test Steps

1. IMPORTANT — Existing users: after installing this build the app will ask
   you to set up your adapter again (once only). Go through the setup flow,
   tap your adapter, wait for green, tap Add. Your cached data (Service
   Reminder, TPMS, etc.) should all still be there.
2. New users: follow the 5-step setup card on the main screen.
   - Plug adapter into OBD2 port under dashboard
   - Turn on ignition, keep engine off
   - Tap Scan — your adapter should appear
   - Tap it to test compatibility (wait for green)
   - Tap Add — setup card disappears, full app revealed
3. After setup: connect to your Grenadier and verify all cached data is intact
   (Service Reminder, TPMS).
4. With ignition OFF: confirm the orange "Ignition Off" banner appears on
   the main screen. Turn ignition ON — banner disappears.
5. With engine running: confirm the orange "Engine Running" banner appears
   and ECU Discovery Details buttons are dimmed gray (not orange).
6. Tap any feature card while a read is in progress → confirm the
   "Adapter busy — tap again" toast appears briefly at the bottom.
7. Then explore the app and let us know what you think!

Please Report
- Did the adapter setup flow work smoothly on first launch?
- Did all your cached data reappear after completing setup?
- Which adapter you are using (BLE device name)
- Any screen that still shows empty or broken after setup
- Anything that looks wrong or unexpected

Recommended BLE OBD2 Adapters
- OBDLink CX (OBDLink CX)
- vLinker BM+ (vLinker BM-IOS)
- vLinker MC+ (vLinker MC-IOS)

---

### v0.8.5 (Alpha-5)

What to Test — Alpha-5 (v0.8.5)

Focus: Service Reminder overdue, iPad improvements, iOS 16.6 support

What's New in Alpha-5
- NEW: iOS 16.6 support — the app now works on iPhone 8 and newer (previously iPhone 12+)

Fixed in Alpha-5
- Service Reminder: if your service is overdue, the app now shows the correct overdue
  amounts ("Time Overdue: 529 d") — previously it displayed a wrong large number like
  "65007 days remaining"
- Service Reminder Calibrate: you can now enter overdue amounts — a Remaining/Overdue
  toggle appears per field when your service is past due
- iPad: several screens previously showed as a narrow column — now display full-width

Fixed in Alpha-4e
- Service Reminder got some bug fixes — please test and calibrate again!
- Service Reminder: "More Details" now shows estimated last service date (useful when
  the dealer used a different service reset tool)
- Service Reminder "Read Service Details" is somewhat slower, because of reading more details
- TPMS "Read TPMS Sensor Details" is ~1.4 seconds faster
- ECU Discovery is more stable — race condition causing occasional "CAN Bus Asleep" fixed

Test Steps

1. Connect to your Grenadier and verify VIN is read correctly
2. Service Reminder (main screen card)
   - Tap "Read Service Details" with ignition ON
   - If your service is overdue: check the card header shows "SERVICE OVERDUE"
     and each overdue field shows "Time Overdue", "Distance Overdue" etc.
   - If not overdue: check "Remaining Until Service" matches your head unit
   - Tap Calibrate if any value differs from what your dashboard shows
   - Close the app and reopen -- confirm the reading is still shown
4. TPMS Information (main screen card)
   - Tap "Read TPMS Sensor Details" with ignition ON
   - Check all 5 sensor IDs and pressures match your head unit
   - Close the app and reopen TPMS -- confirm last reading is still shown
5. Export Diagnosis Report
   - Tap "Export Diagnosis Report" on the main screen
   - Verify your VIN, odometer, My Grenadier details and TPMS sensor IDs are correct
6. ECU Health Check → tap any ECU row → DTC History
   - Tap the trash icon to clear that ECU's history — confirm it works
7. Then explore the app and let us know what you think!

Please Report

- Which adapter you are using (BLE device name)
- If your service is overdue: does the overdue display look correct?
- If you are on iPad: do all screens display full-width and in dark theme?
- Any Service Reminder values that look wrong compared to your dashboard
- Any TPMS sensor ID or pressure that looks wrong
- Anything that looks wrong or unexpected

Recommended BLE OBD2 Adapters (BLE device name)
- OBDLink CX (OBDLink CX)
- vLinker BM+ (vLinker BM-IOS)
- vLinker MC+ (vLinker MC-IOS)
- Vgate iCar Pro BLE (IOS-Vlink)

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
| 0.8.4 | -- | 2026-06-28 | Alpha-4e | Petrol connect flow fix, CAN Bus Asleep after ECU Health Check fixed, Service Reminder + TPMS faster, Refresh buttons in ECU Info + Health Check detail, Est. Last Service date in Service Reminder |
| 0.8.5 | -- | 2026-06-29 | Alpha-5 | Service Reminder overdue support, iPad dark mode + full-width screens, Fleet Management fixes, DTC History per-ECU clear, iOS 16.6 support |
| 0.8.6 | -- | 2026-07-02 | Alpha-6 | First-run adapter onboarding flow, full UI gate until adapter registered, BLE reconnect fix, "Adapter busy" toast, TPMS error message fix, delete individual DTC history entries, ECU Discovery engine-running UX |
| 0.9.0 | 45 | 2026-07-08 | Beta-1 | First Beta build actually shipped to TestFlight — DPF Monitor, BLE background recovery, KOFF/KOEO/KOER terminology, MIL indicator, ECU Discovery corruption fix (5 rounds), AT-bus race fixes |
| 0.9.0 | 46 | 2026-07-11 | Beta-1b | Adapter Onboarding dead end fix, Service Reminder hang fix + DID trim (10→5 HU DIDs, removed 8-ECU research sweep), Calibrate banner hide-after-use, TPMS DID trim (6→4), cross-VIN data leak fix |
| 0.9.0 | 47 | 2026-07-12 | Beta-1c | My Grenadier Country+Market auto-fill from locale (also fixed an appearance regression), Diagnosis Report engine-variant display fix, ECU Health Check missing DTC codes fix (internal — not called out to testers) |
| 0.9.0 | 48 | 2026-07-13 | Beta-1d | Service Reminder dashes-after-calibration fix, silent read-failure fix (now shows a message) — other work this build (DPF Monitor/Engine Metrics redesigns, ECU Information HU DID, main screen reorder) internal, still Pioneer-Key-gated, not called out to testers |
| 0.9.0 | 49 | 2026-07-17 | Beta-2 | ECU Information now a standard feature for all testers (B63). Beta-1e work folded in here (Registration Number, PDF share subject/body, DTC-clear fix, etc.) — only ECU Information called out to testers; the rest not mentioned per instruction. DPF Monitor/Engine Metrics remain Pioneer-Key-gated, not mentioned. |
