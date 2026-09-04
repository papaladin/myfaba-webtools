# myfaba-webtools

Browser-based tools for the **Faba Box** (original offline version) storytelling device.  
No install. No upload. Everything runs locally in your browser.

---

## Tools

### 🎙 Faba Encoder
Convert your own MP3 files into the Faba Box format and package them as a ready-to-copy ZIP.

**→ [Open the encoder](https://papaladin.github.io/myfaba-webtools)**

---

## How it works

The Faba Box stores audio content in a proprietary encoded format on an internal microSD card. Each "figure" (an NFC tag placed on top of the box) maps to a folder of encoded audio tracks.

This tool:
1. Takes MP3 files you provide
2. Rewrites their ID3 tags to match the Faba naming convention
3. Applies the byte-level encoding the Faba Box expects
4. Packages everything into a ZIP you download and copy to your device

The encoding algorithm is a direct port of the work documented in [wansors/myfaba-hacks](https://github.com/wansors/myfaba-hacks), to whom full credit belongs for the original reverse-engineering work.

---

## Compatibility

| Device | Support |
|---|---|
| **Faba (offline)** | ✅ Fully supported |
| **Faba+** (connected, app-linked) | ❌ Not supported — different encoding, USB is charge-only |

> ⚠️ **Do not connect your original Faba Box to the official MyFaba app** after adding custom content. This may trigger an update that deletes folders not associated with purchased figures.

---

## Requirements

- A Faba Box (original offline version)
- Blank **NTAG213** NFC tags (widely available, ~$0.15–0.30 each)
- A phone with NFC and the **NFC Tools** app (iOS / Android, free)
- A modern browser (Chrome, Firefox, Safari, Edge)

---

## Disclaimer

### What this is — and isn't

✅ This tool is designed for loading **your own content** onto your own device.  
❌ It does **not** help you copy, share, or access Faba's original licensed audio content.  
❌ It is **not** affiliated with, endorsed by, or connected to MyFaba or its parent company in any way.

### Your responsibility

**By using this tool, you accept full and sole responsibility for:**

- The content you encode and load onto your device
- Ensuring you own the rights to any audio you process
- Any consequences arising from modifications to your device
- Compliance with the terms of service of your Faba device

The authors of this tool accept no liability whatsoever for device damage, data loss, account suspension, voided warranties, or any legal issues arising from its use.

**Do not use this tool to encode, reproduce, or distribute copyrighted content you do not own.**  
Encoding someone else's audio does not grant you rights to it.

### Device risk

Modifying your Faba Box carries inherent risk. While the original Faba (offline) has no phone-home capability and no known detection mechanism, you proceed entirely at your own risk. The authors of this tool are not responsible if your device is damaged, bricked, or rendered non-functional.

---

## Credits

Encoding algorithm and original reverse-engineering: [wansors/myfaba-hacks](https://github.com/wansors/myfaba-hacks) — go star that repo, the hard work happened there.

ZIP generation: [fflate](https://github.com/101arrowz/fflate) by 101arrowz (MIT license).

---

## License

MIT — see [LICENSE](./LICENSE).  
Do whatever you want with this code. Just don't use it to do something that would get you or anyone else in trouble.
