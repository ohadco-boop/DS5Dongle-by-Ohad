# CHANGELOG

## 1.0.5 - Hebrew OLED UI

- Added optional Hebrew OLED UI language.
- Added `Settings -> Language` with English/Hebrew toggle.
- Added a compact Hebrew bitmap font for the 128x64 OLED.
- Localized main OLED screen titles, Settings labels, Remap title/footer, pairing hints and save/status messages.
- Refined Hebrew pairing instructions: `Create + PS` is kept readable in English while the surrounding instructions are Hebrew.
- Fixed Hebrew Lightbar header overlap between `[BATT]` and `תאורה`, and changed the footer hint to `שינוי מצב עם R1`.
- Default language remains English for existing users.
- Based on 1.0.4 Stable + AudioRouteFix + PoweroffTouchpadWdtFix.


## 1.0.4 - Poweroff Touchpad Watchdog Fix

- Fixed a case where touching the DualSense touchpad during controller power-off could keep high-rate HID interrupt reports flowing and trip the Pico watchdog.
- The safe power-off guard now remains active until the real HCI DISCONNECTION_COMPLETE event, instead of ending immediately after sending the disconnect command.
- Late controller interrupt reports are dropped during intentional power-off to keep Bluetooth/USB teardown quiet.
- The original AudioRouteFix is preserved. Fix2/Fix3 and Tester TTL behavior are not included.


### 1.0.4 PoweroffWatchdogFix
- Prevented false Pico watchdog resets during intentional controller power-off after long audio/game sessions.
- Kept the watchdog enabled, but extended the timeout from 1 s to 3 s and feeds it during the safe BT teardown path.
- No changes to AudioRouteFix behavior, Tester route behavior, or USB audio descriptors.


## v1.0.4 - Audio Route Fix
- Added automatic USB Audio route recovery when a browser or tester page stops the audio stream without a headset plug/unplug event.
- Fixes cases where DualSense Tester could leave audio stuck until reconnecting headphones.
- Clears stale host audio route state after the stream stops or the USB Audio interface returns to idle.
- AudioKeep and deferred Flash save now use recent effective audio activity instead of stale USB audio state.
- Output reports are no longer treated as missing speaker audio packets after a stale browser/tester stream.

## v1.0.4 - Stable AudioFix
- Fixed the AudioKeep + save + poweroff sequence.
- The firmware now sends an audio-safe mute/off state to the controller before any forced Flash write.
- Added a short delay before saving/disconnecting to prevent broken audio on the next connection.
- Cleans cached host audio route after local disconnect so the next connection starts clean.

## v1.0.4 - Stable
- Updated the firmware version to `1.0.4` across the build system and OLED fallback text.
- GitHub Actions UF2 artifact name: `DS5Dongle-by-Ohad-1.0.4.uf2`.
- Added official Boot Screen: `DS5Dongle / by Ohad / v1.0.4`.
- Status screen displays `DS5Dongle 1.0.4`.
- AudioKeep is included as an official feature: when ON, active audio prevents Idle shutdown.
- PowerCombo and Idle shutdown use a safe poweroff path and return to the Status screen before disconnecting.
- Fixed Settings item indexing after adding AudioKeep, so Reset Defaults and Wipe Slots no longer collide with AudioKeep.
- Added new OLED asset: `assets/oled/oled_sc00_boot.jpg`.
- Updated Status OLED asset for v1.0.4: `assets/oled/oled_sc01.jpg`.
- Added user manual: `USER_MANUAL.pdf` and `docs/USER_MANUAL.md`.
- Added product specification: `PRODUCT_SPECIFICATION.pdf` and `docs/PRODUCT_SPECIFICATION.md`.

## v1.0.1
- Added AudioKeep on/off: prevents Idle shutdown while audio is active.
- Added the REMAP OLED asset under `assets/oled`.

## v1.0.0
- Initial stable DS5Dongle by Ohad baseline with OLED UI, Settings, REMAP, PowerCombo, Audio, Diagnostics, and pairing slots.