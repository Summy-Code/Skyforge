Skyforge

An Android app that writes Skylanders figure dumps onto cheap NFC cards, so they work on the portal like the real figure.

Import your dumps once, tap a figure, hold a card to the phone, done.

[!WARNING]
This app is vibecoded. It was built with an AI assistant and has only been tested on one real Android device.
It may not work perfectly. 
Use it at your own risk.

Features

All dumps in one library, with name, game and card artwork assigned automatically
Writes and verifies a card in one go (keys are calculated from the card's UID, no PC needed)
Read a card to see what is on it, or back up your own figure
Tap the big card to flip it: matching card back, holo / chrome / gloss effects that follow your finger and phone tilt
Print the cards at real size (54 × 85.5 mm) with a cut frame to stick on your NFC cards:
front, back or both, 9 cards per A4 page or 1 per page, via the Android print dialog or as PDF

Languages: English, German, French, Spanish, Italian, Dutch, Portuguese (follows the system language)

What you need
Android 7 or newer with NFC
A phone whose NFC chip supports MIFARE Classic (many Samsung, Pixel and Xiaomi phones do; some with
other NFC chips don't – the app tells you)
MIFARE Classic 1K (S50) cards or stickers with a 4-byte UID. NTAG213/215 stickers do not work.

Dump files of your figures (.dump, .bin, .sky, 1024 bytes)
Dumps
A collection of Skylanders dumps can be found here:

https://drive.google.com/drive/folders/1eO3DKfwCbKJ657OnhVC3JwtqCrelqOQZ

Download the folder (or a ZIP of it) to your phone. Only use dumps of figures you own.
No dumps are included in this app or repository.

Install

Download Skyforge-x.y.apk from the Releases page.

Open it on your phone and allow installing apps from this source.

Google Play Protect doesn't know the app and may warn you – choose "Install anyway".

How to use

Tap + and pick the dump folder (subfolders are read too) or a ZIP file.

Tap a figure.

Hold a card to the back of the phone until the checkmark appears.

Long-press a figure to rename it, set your own picture, mark it as favorite or delete it.

The printer button at the top lets you select cards for printing. In the print dialog choose
"Actual size" / 100 %, not "Fit to page".

Credits

Images: card artwork, card backs, logos and character pictures from

GITHUB LINK. 

Card artwork by Sobersu and Mr Shadow.

Key calculation and dump conversion based on
TheSkyLib

(tnp3xxx.py by Vitorio Miliano, Python 3 version by Toni Cunyat, UID.py by Nitrus).

Figure name list generated from the ID tables of the Dolphin
and RPCS3 emulators (GPL-2.0).

Fonts: Lilita One and Atkinson Hyperlegible (SIL Open Font License).

Disclaimer
Unofficial fan project, not affiliated with or endorsed by Activision. Skylanders is a trademark of
Activision. This app contains no figure dumps and needs no internet access.
