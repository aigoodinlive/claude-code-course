---
name: create-exercise
description: Create a student exercise with template, hints, validation, and solution. Use when building practice materials for the course.
---

# Create Exercise - יצירת תרגיל

צור תרגיל מובנה עם רמזים ופתרון.

## מבנה התרגיל

### 1. כותרת ורמת קושי
```markdown
# תרגיל: [שם]

**רמה:** קל / בינוני / מאתגר
**זמן משוער:** X דקות
**נושא:** [Skills / Agents / Hooks / כללי]
```

### 2. תיאור המשימה
```markdown
## 📋 המשימה

[תיאור ברור של מה צריך לעשות]

### דרישות:
- [ ] דרישה 1
- [ ] דרישה 2
- [ ] דרישה 3
```

### 3. קבצי התחלה (אם צריך)
```markdown
## 📁 קבצי התחלה

צור את הקבצים הבאים:

**config.json:**
```json
{
  "name": "example"
}
```
```

### 4. רמזים מדורגים
```markdown
## 💡 רמזים

<details>
<summary>רמז 1 (קל)</summary>
התחל מ...
</details>

<details>
<summary>רמז 2 (בינוני)</summary>
שים לב ש...
</details>

<details>
<summary>רמז 3 (חשיפת כיוון)</summary>
הפקודה שאתה צריך היא...
</details>
```

### 5. בדיקה עצמית
```markdown
## ✅ בדיקה עצמית

הרץ את הפקודות הבאות לבדוק שהכל עובד:

```bash
# בדיקה 1
command --check

# בדיקה 2
test -f file.txt && echo "קיים"
```
```

### 6. פתרון מלא
```markdown
## 🔑 פתרון

<details>
<summary>לחץ לצפייה בפתרון</summary>

### שלב 1: [תיאור]
```bash
command here
```

### שלב 2: [תיאור]
```bash
another command
```

### הסבר:
[הסבר מפורט למה זה עובד]

</details>
```

### 7. אתגר נוסף (בונוס)
```markdown
## 🚀 אתגר בונוס

לחזקים: [משימה מורחבת]
```

## רמות קושי

| רמה | מאפיינים |
|-----|----------|
| קל | שלב אחד, פקודה בודדת |
| בינוני | מספר שלבים, שילוב מושגים |
| מאתגר | פתרון יצירתי, מחקר עצמאי |

## שימוש

```
/create-exercise "ארגון קבצים" easy intro
/create-exercise "יצירת skill" medium advanced
/create-exercise "אוטומציה מלאה" hard business
```

$ARGUMENTS: "[title]" [difficulty] [tier]
- title: שם התרגיל
- difficulty: easy / medium / hard
- tier: intro / advanced / business
