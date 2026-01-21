# Claude Code in Action - סיכום קורס מקיף

## מטרת הקורס
קורס מקיף על שימוש ב-Claude Code למשימות פיתוח תוכנה, המכסה מארכיטקטורה בסיסית ועד אינטגרציה מתקדמת.

---

## 📋 מבנה הקורס (21 שיעורים)

### חלק 1: What is Claude Code? (3 שיעורים)
1. **Introduction** (וידאו)
2. **What is a coding assistant?** (וידאו)
3. **Claude Code in action** (וידאו)

### חלק 2: Getting hands on (9 שיעורים)
4. **Claude Code setup** (טקסט)
   - הדרכות התקנה מלאות
   - MacOS (Homebrew): `brew install cask claude-code`
   - MacOS, Linux, WSL: `curl -fsSL https://claude.ai/install.sh | bash`
   - Windows CMD: `curl -fsSL https://claude.ai/install.cmd -o install.cmd && install.cmd && del install.cmd`
   - אימות: הרצת `claude` בטרמינל
   - הגדרות נוספות ל-AWS Bedrock או Google Cloud Vertex

5. **Project setup** (טקסט)
6. **Adding context** (וידאו)
7. **Making changes** (וידאו)
8. **Course satisfaction survey** (שאלון)
9. **Controlling context** (וידאו)
10. **Custom commands** (וידאו)
11. **MCP servers with Claude Code** (וידאו)
12. **Github integration** (וידאו)

### חלק 3: Hooks and the SDK (7 שיעורים)
13. **Introducing hooks** (וידאו)
14. **Defining hooks** (וידאו)
15. **Implementing a hook** (וידאו)
16. **Gotchas around hooks** (טקסט)
17. **Useful hooks!** (וידאו)
18. **Another useful hook** (טקסט)
19. **The Claude Code SDK** (וידאו)

### חלק 4: Wrapping up (2 שיעורים)
20. **Quiz on Claude Code** (מבחן)
21. **Summary and next steps** (וידאו)

---

## 🎯 מה תלמד בקורס

### 1. **Understand coding assistant architecture**
הבנה כיצד AI assistants מתקשרים עם codebases דרך אינטגרציה של כלים והבסיס הטכני.

### 2. **Explore Claude Code's tool use system**
גילוי כיצד למנף מספר כלים בשילוב לטיפול במשימות תכנות מורכבות ורב-שלביות.

### 3. **Master context management techniques**
אסטרטגיות לשמירה על context רלוונטי לאורך שיחות והפניה יעילה לתיעוד ופרויקטים.

### 4. **Implement visual communication workflows**
שימוש ב-visual inputs לתקשורת שינויים בממשק וניצול מצבי תכנון מתקדמים.

### 5. **Create custom automation**
בניית פקודות מותאמות אישית ואוטומציות הניתנות לשימוש חוזר שמייעלות משימות פיתוח חוזרות.

### 6. **Extend functionality with MCP servers**
למידה לשלב כלים וservices חיצוניים ליכולות משופרות כמו אוטומציה של דפדפן וניהול מסדי נתונים.

### 7. **Integrate with GitHub workflows**
הבנה כיצד להגדיר תהליכי code review אוטומטיים ושילוב סיוע AI בזרימות העבודה הקיימות שלך ב-GitHub.

### 8. **Apply thinking and planning modes**
למידה מתי וכיצד להשתמש בגישות חשיבה שונות לרמות מורכבות שונות של משימות תכנות.

---

## 📚 דרישות מקדימות (Prerequisites)

1. **היכרות עם command-line interfaces ופעולות טרמינל**
2. **הבנה בסיסית של version control עם Git**

---

## 👥 למי הקורס מיועד

1. **מפתחי תוכנה** המעוניינים לשלב סיוע AI בזרימות עבודת הקוד שלהם
2. **צוותים** המבקשים ליישם אינטגרציית GitHub מבוססת AI עבור זרימות עבודה מרובות

---

## 🔑 נושאים מרכזיים בקורס

### Setup & Installation
- התקנה בסביבות שונות (MacOS, Linux, Windows, WSL)
- אינטגרציה עם AWS Bedrock
- אינטגרציה עם Google Cloud Vertex
- קישורים לתיעוד:
  - https://code.claude.com/docs/en/quickstart
  - https://code.claude.com/docs/en/amazon-bedrock
  - https://code.claude.com/docs/en/google-vertex-ai

### Context Management
- הוספת context לשיחות
- שליטה ב-context לאורך פרויקטים
- הפניה לתיעוד ופרויקטים

### Custom Commands
- יצירת פקודות מותאמות אישית
- אוטומציה של משימות חוזרות
- בניית workflows ניתנים לשימוש חוזר

### MCP Servers
- שילוב כלים חיצוניים
- הרחבת יכולות Claude Code
- אוטומציה של דפדפן וניהול מסדי נתונים

### GitHub Integration
- אוטומציה של code review
- שילוב ב-existing workflows
- ניהול pull requests

### Hooks & SDK
- הבנת Hooks ב-Claude Code
- יישום Hooks מותאמים אישית
- שימוש ב-Claude Code SDK
- Gotchas ו-best practices

---

## 💡 תובנות למפתחי קורסים

### רעיונות לקורסים שלך
1. **קורס למתחילים**: התמקדות ב-setup, basic usage, ו-context management
2. **קורס מתקדם**: Hooks, SDK, אינטגרציות מורכבות
3. **קורס עסקי**: GitHub integration, team workflows, automation
4. **קורס התמחותי**: MCP servers, custom tools, advanced customization

### נושאים שכדאי להוסיף
- דוגמאות קוד מעשיות לכל נושא
- תרגילים hands-on
- מקרי בוחן אמיתיים
- Best practices וtips & tricks
- Troubleshooting נפוצים
- השוואה לכלים אחרים (GitHub Copilot, etc.)

### פורמטים מומלצים לחומר
- **מסמכי טקסט**: להדרכות התקנה ו-setup
- **וידאו**: לדמו של features ו-workflows
- **מצגות**: לסקירה כללית וקונספטים
- **Markdown**: לתיעוד טכני ו-reference
- **תרגילים אינטראקטיביים**: לתרגול מעשי

---

## 🎨 עיצוב וברנדינג

### רעיונות לשילוב הברנד שלך
- צבעי זהב, סגול, שחור בכל החומרים
- מוטיב Circuit board לגרפיקה
- לוגו "G" זהב עם traces
- טקסטים בעברית עם מונחים טכניים באנגלית

### סוגי חומרים אפשריים
1. **Workbooks** בעיצוב Digital Alchemy
2. **Video thumbnails** עם הברנדינג שלך
3. **Cheat sheets** למהירות התייחסות
4. **Interactive demos** באתר goodin.live
5. **Certificate of completion** מעוצב

---

## 📖 משאבים נוספים

### קישורים רשmiים
- מדריך התחלה מהירה: https://code.claude.com/docs/en/quickstart
- Amazon Bedrock integration: https://code.claude.com/docs/en/amazon-bedrock
- Google Vertex AI integration: https://code.claude.com/docs/en/google-vertex-ai

### רעיונות למשאבים משלימים
- FAQ section
- Community forum
- Example projects gallery
- Video tutorials library
- Blog posts with use cases

---

## 🚀 צעדים הבאים

1. **חקור את הקורס המלא** - עבור על כל 21 השיעורים
2. **תעד insights** - רשום תובנות ודוגמאות מעניינות
3. **בנה curriculum** - צור מבנה קורס משלך
4. **פתח תוכן** - כתוב חומרים בסגנון שלך
5. **תבדוק את השוק** - ראה מה חסר בקורסים קיימים
6. **תשווק** - הכן landing page ו-marketing materials

---

*מסמך זה נוצר על בסיס הקורס הרשמי של Anthropic Academy*
*לשימוש פנימי לצורך תכנון קורסים והטמעות*
