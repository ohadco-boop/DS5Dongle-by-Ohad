# CHANGELOG

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
