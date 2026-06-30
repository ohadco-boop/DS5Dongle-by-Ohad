# CHANGELOG

## v1.0.4 - Stable
- עודכן מספר הגרסה ל-1.0.4 בכל מקומות הבנייה וה-OLED fallback.
- שם ה-UF2 דרך GitHub Actions: `DS5Dongle-by-Ohad-1.0.4.uf2`.
- נוסף Boot Screen רשמי: `DS5Dongle / by Ohad / v1.0.4`.
- Status מציג `DS5Dongle 1.0.4`.
- AudioKeep נשאר כחלק רשמי מהגרסה: כשהוא ON, אודיו פעיל מונע כיבוי Idle.
- PowerCombo ו-Idle משתמשים במסלול כיבוי בטוח וחוזרים למסך Status לפני ניתוק.
- תוקן מיקום פריטי Settings לאחר הוספת AudioKeep: Reset defaults ו-Wipe slots לא מתנגשים עם AudioKeep.
- נוסף asset חדש: `assets/oled/oled_sc00_boot.jpg`.
- עודכן asset סטטוס ל-v1.0.4: `assets/oled/oled_sc01.jpg`.
- נוסף מדריך שימוש: `USER_MANUAL.pdf` ו-`docs/USER_MANUAL.md`.
- נוסף מפרט מוצר: `PRODUCT_SPECIFICATION.pdf` ו-`docs/PRODUCT_SPECIFICATION.md`.

## v1.0.1
- AudioKeep on/off: מונע כיבוי Idle בזמן שיש אודיו פעיל.
- נוספה תמונת REMAP ב-`assets/oled`.

## v1.0.0
- גרסת בסיס יציבה של DS5Dongle by Ohad עם OLED, Settings, REMAP, PowerCombo, Audio, Diagnostics וסלוטים.
