# סרטונים — HyperFrames

שני פרויקטים של HyperFrames, בסגנון Coral (קורל / דיו / קרם, משטחים בקצוות חדים, קווקוו 45°, ספרות רקע ענקיות), עם Rubik לכל הטקסט (ל-Bebas Neue של הסגנון אין עברית).

| פרויקט | פורמט | משך | קובץ |
|---|---|---|---|
| `launch-video/` — סרטון ההשקה (מדים → אזרחי → גלובן ביטוחים → הרצאות וסדנאות → סיום) | 9:16, ‏1080×1920 | 48 שניות | `launch-video/renders/tomer-globen-launch.mp4` |
| `tools-reel/` — ריל "שלושת הכלים שיחסכו לכם שעות" | 9:16, ‏1080×1920 | 20 שניות | `tools-reel/renders/tools-reel.mp4` |

## עריכה ורינדור מחדש

```bash
cd videos/launch-video        # או tools-reel
npx hyperframes preview       # Studio: לחיצה על כל טקסט לעריכה, גרירת קליפים בציר הזמן
npx hyperframes check
npx hyperframes render -o renders/out.mp4
```

- הטקסטים נמצאים ב-`index.html` של כל פרויקט. הזמנים מוגדרים ב-`data-start` / `data-duration` ובסקריפט GSAP שבתחתית הקובץ.
- המוזיקה (`assets/music.mp3`) מסונתזת ונקייה מזכויות. אפשר להחליף אותה בקובץ אחר באותו שם.
- סרטון ההשקה הוא גרסה ויזואלית ללא קריינות. אחרי שתצלם את התסריט, אפשר לשים את הקול מעל ולהאריך את הסצנות לפי קצב הדיבור.
- בריל, שלושת הכלים (Claude, ‏Gamma, ‏NotebookLM) מוגדרים כטקסט בשורות `#l1`–`#l3`.
