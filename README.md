<div align="center">

# Skyforge

**Write Skylanders figure dumps onto cheap NFC cards – right from your Android phone.**

Import your dumps once, tap a figure, hold a card to the phone. Done.

![Android 7+](https://img.shields.io/badge/Android-7%2B-3DDC84?logo=android&logoColor=white)
![NFC](https://img.shields.io/badge/NFC-MIFARE%20Classic%201K-blue)
![Languages](https://img.shields.io/badge/languages-7-orange)
![Vibecoded](https://img.shields.io/badge/vibecoded-%E2%9C%A8-ff69b4)

</div>

> [!WARNING]
> **This app is vibecoded.** It was built with an AI assistant and has only been tested with automated tests and in a desktop browser – not thoroughly on real phones, cards and portals. It may not work perfectly. Use it at your own risk and please report problems in the [issues](../../issues).

---

## Contents

- [Features](#features)
- [What you need](#what-you-need)
- [Dumps](#dumps)
- [Install](#install)
- [How to use](#how-to-use)
- [Building](#building)
- [Credits](#credits)
- [Disclaimer](#disclaimer)

---

## Features

### Cards
- **One library for all dumps** – name, game and card artwork are assigned automatically
- **Write and verify in one go** – keys are calculated from the card's UID, no PC needed
- **Read any card** to see what is on it, or back up your own figure
- **Element effects** while a card is being written – fire, water, air, earth, life, undead, magic, tech, light, dark

### Skylander inventory
- Save figures from cards **with their progress**: level, XP, gold, play time, nickname, upgrade path
- Browse them as **coins** – each figure is kept once with its newest state
- Keep **extra save states** on purpose and write any of them back to a card
- Optional **automatic save** before a card is overwritten (asked the first time)

### Look & sound
- **Flip the card** to see the matching card back, with holo / chrome / gloss effects that follow your finger and phone tilt
- **Voice lines** – the Skylander speaks when you select it, read its card or write it (about 190 characters)
- A few **sound effects** and a quiet **ambience** in the inventory – each can be switched off with the speaker button
- …and somebody is hiding somewhere in the app 👀

### Printing
- Print cards at **real size (54 × 85.5 mm)** with a cut frame to stick on your NFC cards
- Front, back or both · 9 cards per A4 page or 1 per page · Android print dialog or PDF

### Languages
English, German, French, Spanish, Italian, Dutch and Portuguese – follows the system language.

---

## What you need

| | |
|---|---|
| 📱 **Phone** | Android 7 or newer with NFC |
| 📡 **NFC chip** | Must support **MIFARE Classic** – many Samsung, Pixel and Xiaomi phones do, some with other NFC chips don't (the app tells you) |
| 💳 **Cards** | **MIFARE Classic 1K (S50)** cards or stickers with a **4-byte UID** |
| 📂 **Dumps** | Dump files of your figures (`.dump`, `.bin`, `.sky`, 1024 bytes) |

> [!IMPORTANT]
> NTAG213 / NTAG215 stickers do **not** work.

---

## Dumps

A collection of Skylanders dumps can be found here:

### 👉 [Skylanders dumps (Google Drive)](https://drive.google.com/drive/folders/1eO3DKfwCbKJ657OnhVC3JwtqCrelqOQZ)

Download the folder (or a ZIP of it) to your phone.

> [!NOTE]
> Only use dumps of figures you own. No dumps are included in this app or repository.

---

## Install

1. Download `Skyforge-x.y.apk` from the [**Releases**](../../releases) page.
2. Open it on your phone and allow installing apps from this source.
3. Google Play Protect doesn't know the app and may warn you – choose **"Install anyway"**.

---

## How to use

### Write a card
1. Tap **+** and pick the dump folder (subfolders are read too) or a ZIP file.
2. Tap a figure.
3. Hold a card to the back of the phone until the checkmark appears. ✅

### Inventory
- Hold a written card to the phone in the library to read it, then tap **Add to inventory**.
- The **Inventory** tab shows all saved figures – tap a coin for its stats and extra saves.

> [!NOTE]
> Level and stats are read from the figure's save data. The XP layout of Giants and later games is partly based on community research and may be off for some figures.

### More
- **Long-press** a figure to rename it, set your own picture, mark it as favorite or delete it.
- The **printer button** at the top lets you select cards for printing.

> [!TIP]
> In the print dialog choose **"Actual size" / 100 %**, not "Fit to page" – otherwise the cards won't have the right size.

---

## Building

```bash
# 1. create your own signing key (once)
mkdir -p keystore && keytool -genkeypair -keystore keystore/skyforge.jks -alias skyforge \
  -keyalg RSA -keysize 4096 -validity 36500 -dname CN=Skyforge

# 2. build the APK
KS_PASS=<your password> TOOLS=/path/to/tools ./build.sh
```

**Requirements:** a JDK, Google's `bundletool-all.jar` (contains aapt2, D8 and the signer) and `android.jar` (API 34). Details are at the top of `build.sh`.

**Tests:** `test/run_all.sh`

> [!CAUTION]
> Never commit your keystore – updates must be signed with the same key.

---

## Credits

| What | By |
|---|---|
| 🖼️ **Images** – card artwork, card backs, logos, character pictures | **[GITHUB LINK](https://github.com/)** · card artwork by Sobersu and Mr Shadow · coins by Sobersu, fruitsnack, Cha0s and Mirakel |
| 🔑 **Key calculation & dump conversion** | [TheSkyLib](https://github.com/DevZillion/TheSkyLib) – tnp3xxx.py by Vitorio Miliano, Python 3 version by Toni Cunyat, UID.py by Nitrus |
| 📋 **Figure name list** | ID tables of the [Dolphin](https://github.com/dolphin-emu/dolphin) and [RPCS3](https://github.com/RPCS3/rpcs3) emulators (GPL-2.0) |
| 🔊 **Voice lines, sound effects, ambience** | Skylanders game rips (Spyro's Adventure to Imaginators) – property of Activision |
| 🧸 **Trigger Snappy 3D model** | Skylanders: Imaginators rip – property of Activision |
| 🧊 **3D rendering** | [three.js](https://threejs.org) (MIT) |
| 🔤 **Fonts** | Lilita One and Atkinson Hyperlegible (SIL Open Font License) |
