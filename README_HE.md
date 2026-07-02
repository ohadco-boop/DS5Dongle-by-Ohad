# DS5Dongle by Ohad v1.0.5


## שפה

- [English](README.md)
- [עברית](README_HE.md)

Firmware מותאם ל-Raspberry Pi Pico 2 W עם מסך Waveshare Pico-OLED-1.3, שמאפשר שימוש בשלט DualSense דרך Bluetooth מול מחשב, עם תצוגת OLED, הגדרות, Audio, Remap, Diagnostics וניהול סלוטים.

![Boot](assets/oled/oled_sc00_boot.jpg)


## תיקון Audio Route ב-1.0.5

החבילה הזו כוללת תיקון התאוששות אוטומטית לאודיו אחרי שימוש באתרי בדיקה כמו DualSense Tester. אם האתר פותח את הזרמת האודיו ואז נסגר או מפסיק לשלוח packets, הקושחה מחזירה את מסלול האודיו לבד בלי צורך לחבר/לנתק אוזניות.

## קבצים חשובים
- `DS5Dongle-by-Ohad-1.0.5.uf2` - נוצר ב-GitHub Actions לאחר build.
- `USER_MANUAL.pdf` - מדריך שימוש מלא.
- `PRODUCT_SPECIFICATION.pdf` - מפרט מוצר.
- `CHANGELOG.md` - היסטוריית גרסאות.

## יכולות מרכזיות
- DualSense Bluetooth bridge.
- USB HID מול המחשב.
- USB Audio ב-48 kHz.
- תמיכה במיקרופון BT של השלט.
- AudioKeep: השלט לא נכבה בגלל Idle בזמן שיש אודיו פעיל.
- OLED 128x64 עם מסכי Status, Slots, Lightbar, Trigger Test, Gyro, Touchpad, Diagnostics, CPU, BT Signal, VU, Settings ו-Remap.
- Remap ל-19 כפתורים כולל Off ו-PicoMic.
- PowerCombo: PS + Options לניתוק/כיבוי בטוח.
- Multi-slot pairing עד 4 סלוטים.
- עדכון Firmware דרך UF2.

## Build ב-GitHub
הגרסה נשלטת בקובץ:

```yaml
.github/workflows/build.yml
FIRMWARE_VERSION: 1.0.5
```

ה-artifact שייצא מה-build יהיה:

```text
DS5Dongle-by-Ohad-1.0.5.uf2
```

## שימוש מהיר
1. הורד את ה-UF2 מה-Artifact של GitHub Actions.
2. הכנס את הפיקו ל-BOOTSEL.
3. גרור את ה-UF2 לכונן RPI-RP2.
4. חבר את השלט דרך Bluetooth.
5. השתמש ב-KEY0/KEY1 כדי לנווט במסכי OLED.

## ניווט OLED
- KEY0: מסך הבא.
- KEY1: מסך קודם.
- KEY1 ארוך: שינוי בהירות.
- KEY0 + KEY1: reboot לפיקו.
- Options + D-Pad ימינה/שמאלה בשלט: מעבר בין מסכים.

## מסמכים
קרא את `USER_MANUAL.pdf` לשימוש רגיל ואת `PRODUCT_SPECIFICATION.pdf` למפרט טכני.


## גרסה 1.0.5

נוסף ממשק OLED בעברית כאופציה. ברירת המחדל נשארת אנגלית. משנים דרך `Settings -> Language` ושומרים עם משולש.
