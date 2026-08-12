# CLAUDE.md — ריפו `pages` (הוראות חובה)

הריפו הזה (github.com/ilana-ai/pages) מתפרסם ב-GitHub Pages בכתובת
`https://ilana-ai.github.io/pages/` — אתר-פרויקט תחת **תת-נתיב** `/pages/`, לא שורש דומיין.

## פרוטוקול favicon — חובה בכל עמוד

בכל עמוד שאני יוצר או עורך בריפו הזה — **תמיד** לוודא שיש favicon של "החיים הטובים".
אין לפרסם עמוד בלי favicon.

**איך מיישמים — מתחילים כל עמוד חדש מהעתקת תיקיית `_template/`:**
היא כוללת `index.html` עם בלוק ה-favicon כבר ב-`<head>`, וכל קבצי האייקונים
(`favicon.ico`, `favicon-16x16.png`, `favicon-32x32.png`, `apple-icon-180x180.png`,
ששת `android-icon-*.png`) + `manifest.json`.

**כללי ברזל:**
- כל תיקיית עמוד היא **עצמאית** — עותק משלה של קבצי ה-favicon. (בגלל תת-הנתיב, אין מקור אחד משותף בשורש.)
- הקישורים תמיד **יחסיים** (`favicon.ico`), אף פעם לא אבסולוטיים (`/favicon.ico`).
- תיקיות שמתחילות ב-`_` (כמו `_template`) לא מתפרסמות ב-GitHub Pages — כך התבנית נשארת פרטית.

**בלוק ה-`<head>` שחייב להופיע בכל עמוד:**
```html
<link rel="icon" type="image/x-icon" href="favicon.ico" />
<link rel="icon" type="image/png" sizes="32x32" href="favicon-32x32.png" />
<link rel="icon" type="image/png" sizes="16x16" href="favicon-16x16.png" />
<link rel="apple-touch-icon" sizes="180x180" href="apple-icon-180x180.png" />
<link rel="manifest" href="manifest.json" />
```

חבילת ה-favicon המקורית (favicon.io מלא) יושבת מחוץ לריפו ב:
`C:\Users\אילנוש\Documents\ilana-agents\pages\logo\מוקטן במשקל\favicon`

## תזכורת פרסום

שינויים נכנסים לאוויר רק אחרי `git commit` + `git push`. עד אז שום רענון בדפדפן לא יעזור.
