# ThinkpadX1C3-SequoiaEFI
ThinkpadX1C3-SequoiaEFI

# ThinkPad T450s / T450 / X1C3 OpenCore EFI

A fully functional OpenCore EFI for running macOS Sequoia on the Lenovo ThinkPad T450s, T450, and X1 Carbon Gen 3 (X1C3). 

This EFI was natively designed for the T450s. However, due to the similarity in hardware specifications, it has been verified to work perfectly on the standard T450 and X1C3. Note that this means the EFI includes a few extra kernel extensions (`.kext`) that may not be strictly required for your specific model, but they do not impact system performance or stability.

---

## Technical Specifications
* **OpenCore Version:** 1.0.4
* **Target macOS Version:** macOS Sequoia 15.x

---

## What Works & What Doesn't

### Working ✅
* **Graphics:** Fully accelerated graphics (Intel HD 5500) — *Requires OpenCore Legacy Patcher (OCLP) post-install*
* **Audio & Display Brightness:** Fully functional
* **Power Management:** Sleep and wake modes work properly
* **Input Devices:** Keyboard backlight, Function (Fn) keys, TrackPad, and the TrackPoint (the red nub)
* **Connectivity:** Bluetooth
* **Ports:** HDMI video and audio output
* **Apple Ecosystem:** Siri and most integrated iCloud/Apple ecosystem features

### Untested ⚠️
* **DisplayPort (DP):** Video output via mini-DP is currently untested.

### Not Working / Limitations ❌
* **Native Wi-Fi:** Native macOS Wi-Fi is not supported. You must use the **HeliPort** application for Wi-Fi connectivity.
* **AirDrop:** Unavaliable due to the Wi-Fi limitation.

---

## Important Post-Download Steps

> ⚠️ **CRITICAL STEP:** You must generate your own unique SMBIOS data before using this EFI on your machine. 

Using the same serials as other users can lead to Apple ID bans or broken services. Use [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) to generate and inject the following values into your `config.plist`:
* `SerialNumber`
* `ROM`
* `MLB`
* `SystemUUID`
