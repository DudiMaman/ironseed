# IRONSEED — ironseed.pages.dev

אתר סטטי המתפרסם אוטומטית ל-Cloudflare Pages.

**כתובת האתר:** https://ironseed.pages.dev

## איך זה עובד

כל push לענף `main` מפעיל GitHub Action שמפרסם את תיקיית `public/` לפרויקט
ה-Pages בשם `ironseed`. תוך כדקה השינוי באוויר — באותה כתובת.

## עדכון האתר

עורכים את `public/index.html` (בכל דרך — Claude, עריכה ישירה ב-GitHub, או
מקומית) ודוחפים ל-`main`. זהו.

## הגדרה חד-פעמית (Secret)

ה-Action דורש Secret בשם `CLOUDFLARE_API_TOKEN`:

1. בדשבורד של Cloudflare: My Profile ← API Tokens ← Create Token ← Custom Token.
2. הרשאה: **Account → Cloudflare Pages → Edit** (על החשבון שלך).
3. בריפו ב-GitHub: Settings ← Secrets and variables ← Actions ← New repository
   secret, בשם `CLOUDFLARE_API_TOKEN`, ומדביקים את הטוקן.
