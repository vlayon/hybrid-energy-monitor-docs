---
title: Beta Tester Guide
---

# Hybrid Energy Monitor – Beta Tester Guide

Thank you for helping test **Hybrid Energy Monitor**!

The app shows the live **energy flow** of a Toyota hybrid on an Android head unit: when the engine drives the wheels, when the battery helps, when the car charges or regenerates. It also has pages with engine and battery data: temperatures, voltages and fuel use. The data comes from the car's OBD2 port through a small Bluetooth adapter.

During the beta, **all features are unlocked**. After the beta, every tester gets the Pro version for free as a thank-you.

> Hybrid Energy Monitor is not affiliated with or endorsed by Toyota Motor Corporation. Toyota and the model names are trademarks of their owners.

---

## 1. What you need

### A Toyota hybrid (2009 or newer)
| Model | Status |
|---|---|
| Yaris Hybrid (2012–2020) | ✅ tested, everything works |
| Prius c / Aqua, Prius (3rd and 4th gen), Prius+ / Prius v | ⚠️ not tested yet, **we need you!** |
| Auris Hybrid, Corolla Hybrid, Camry Hybrid | ⚠️ not tested yet, **we need you!** |
| C-HR Hybrid, RAV4 Hybrid (FWD and AWD) | ⚠️ not tested yet, **we need you!** |

On the untested models, the energy flow will probably work. Some values (battery %, temperatures) may still show "--". Your report helps us fix that for your model.

### An Android head unit (or tablet)
- Android 5.0 or newer, with Bluetooth.
- With Google Play: install through the beta link (section 2). Without Play: ask for the APK file (section 2).

### An ELM327 OBD2 adapter: please read carefully
The app is tested with this kind of adapter. Others often **do not work**.

| | Requirement |
|---|---|
| ✅ **Chip version** | **ELM327 v1.5.** Good copies use the **PIC18F25K80** chip; sellers often mention it. |
| ✅ **Connection** | **Bluetooth "Classic"**, the kind you pair in Android's Bluetooth settings with a PIN (usually **1234** or **0000**). |
| ❌ **"v2.1" adapters** | Avoid them. Most are faulty copies that lack commands the app needs, and they fail with Toyota hybrids. |
| ❌ **Bluetooth LE-only adapters** | Do not work. These are often sold "for iPhone / iOS". |
| ❌ **Wi-Fi adapters** | Do not work. |

The adapter plugs into the **OBD2 port** under the dashboard. On most Toyotas it's below the steering wheel, on the left.

You can check your adapter's version in the app: **Settings → Send report → Save to file**. The report shows a line like `ATI=ELM327 v1.5`.

---

## 2. Installing the app

### With Google Play (recommended)
Use the same Google account as the Play Store on your head unit or phone.
1. **Join the testers group:** <https://groups.google.com/g/hybrid-energy-monitor-testers> → **"Ask to join group"**. Places are limited; we approve requests by hand, usually within a day.
2. When you're approved, open the **beta link**: <https://play.google.com/apps/testing/com.hybridflow.monitor> and tap **"Become a tester"**.
3. Tap **"Download it on Google Play"** and install. Updates arrive automatically through the Play Store.
4. **Please stay in the beta for at least 14 days.** Google requires this before the app can be published for everyone.

### Without Google Play
Write to **support.hybridflow@gmail.com**, and we'll send you the APK file. Install it from a USB stick with the head unit's file manager. If asked, allow "install from unknown sources".

---

## 3. First start
1. **Pair the adapter:** plug it in, switch the car on (READY), then pair it in the head unit's **Android Bluetooth settings** (PIN 1234 or 0000).
2. Open **Hybrid Energy Monitor** → **Settings**:
   - **OBD adapter → Choose:** pick your adapter from the list;
   - **Car model → Change:** pick your model.
3. Go to **Energy Flow**. Within a few seconds, the badge at the top should say READY, EV MODE, ENGINE… and the arrows should move.

If the badge says **IGNITION OFF**, the adapter is connected but the car isn't answering. Switch the car on (READY).

---

## 4. What to test
Please try what you can. Every report helps, even "everything works".

**Energy Flow**
- [ ] Does the badge match what the car does? EV MODE when driving electric, ENGINE + BATTERY when accelerating, REGENERATING when braking, CHARGING at standstill with the engine running.
- [ ] Do the arrows point the right way? Is the right car picture shown for your model?
- [ ] Do speed, rpm, battery kW and charge % make sense?

**Engine page**
- [ ] rpm, coolant and intake temperature, accelerator pedal, fuel use.

**Battery page**
- [ ] Battery % (compare it with the car's own display if it has one), current, pack voltage, battery temperature.

**Display**
- [ ] Day and night mode (the ☀/☾ button, top right; press and hold it for automatic).
- [ ] Is everything readable on your screen size? A photo helps a lot.

**A scan, very important for untested models**
- [ ] Car in **READY** → **Settings → Scan Toyota data codes → Scan**. Wait until it says "Scan finished" (about 1 minute).
- [ ] Then send a report (section 5). The scan is included automatically.
- [ ] If you can: one scan right after a cold start, and one after a 20+ minute drive.

---

## 5. How to report
A report from the app is the most useful, because it includes the technical data we need.

### Option A – save the report and email it (works on every head unit)
1. **Settings → Send report**, and write a short comment: what happened, and on which model.
2. Tap **Save to file**. The app shows where it was saved: `Download/HybridEnergyMonitor/hybrid-report-R-XXXX.txt`.
3. Get the file off the head unit, whichever way is easiest:
   - copy it to a **USB stick** with the head unit's file manager, then attach it to an email from your computer;
   - or use the head unit's file manager to send it to your **phone** (e.g. by Bluetooth), then email it from the phone.
4. Email the file to **support.hybridflow@gmail.com**, with your car model in the subject.

### Option B – share it directly (if your head unit supports it)
In **Settings → Send report**, tap **Share via app** instead. If the head unit has an email app (or Telegram, WhatsApp…), it opens with the report attached and **support.hybridflow@gmail.com** already filled in. If nothing opens or sending fails, use Option A; it always works.

Each report has an ID like **R-7F3K**. Mention it if you also write in the forum.

### Or write to us
- **Email:** support.hybridflow@gmail.com
- **Forum thread:** `[link will be added here]`

**What a report contains:** the app version, car model, adapter type, the last 500 messages between the app and the car, and the scan results. **No location, no VIN, no personal data.**

---

## 6. Known issues
- **Bluetooth drops:** if a phone streams music over the head unit's Bluetooth at the same time, the connection to the adapter can drop now and then. The app reconnects by itself within a few seconds.
- **Small icon:** some head-unit launchers draw all downloaded apps on a coloured plate, so the icon looks small. That's the launcher's style, not the app.
- **Grey values with "(last)":** with the ignition off, the car doesn't answer, so the app shows the last known battery % in grey.

Thank you! 🙏
