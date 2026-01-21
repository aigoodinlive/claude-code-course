---
name: generate-lesson
description: Generate structured lesson content with objectives, examples, and exercises. Use when creating new course lessons or updating existing ones.
---

# Generate Lesson - יצירת שיעור

צור שיעור מובנה לקורס Claude Code בעברית.

## מבנה השיעור

כל שיעור חייב לכלול:

### 1. כותרת ומטא
```markdown
# שיעור X: [נושא]

**משך:** X דקות
**מטרה:** [משפט אחד]
```

### 2. מטרות השיעור
```markdown
## 🎯 מטרות השיעור

בסוף השיעור תדעו:
- מטרה 1
- מטרה 2
- מטרה 3
```

### 3. תוכן מרכזי
- הסברים בעברית פשוטה
- דוגמאות קוד עובדות
- טבלאות השוואה כשרלוונטי
- אזהרות/טיפים בתיבות

### 4. תרגיל מעשי
```markdown
## ✅ תרגיל מעשי

### משימה: [שם]
1. שלב 1
2. שלב 2
3. שלב 3
```

### 5. שאלות לבדיקה עצמית
```markdown
## 📝 שאלות לבדיקה עצמית

1. שאלה?
2. שאלה?
3. שאלה?
```

### 6. סיכום וקישור לשיעור הבא
```markdown
## ➡️ בשיעור הבא

[תיאור קצר של מה ילמדו]
```

## הנחיות כתיבה

1. **שפה פשוטה** - הימנע ממונחים טכניים ללא הסבר
2. **דוגמאות מעשיות** - כל מושג עם קוד שאפשר להריץ
3. **אורך מתאים** - בערך 500-800 מילים לשיעור
4. **פורמט עקבי** - שמור על המבנה בכל השיעורים

## שימוש

```
/generate-lesson skills intro "מבוא ל-Skills"
/generate-lesson hooks advanced "אוטומציה עם Hooks"
```

$ARGUMENTS: [tier] [level] "[title]"
- tier: intro / advanced / business
- level: מספר השיעור או נושא
- title: כותרת השיעור
