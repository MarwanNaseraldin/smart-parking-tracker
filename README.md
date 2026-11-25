# 🛡️ Smart VIP Parking Tracker (Track 1 - Lite)

מערכת מיקרו-סרביסים לניהול כניסת רכבים לחניון VIP חכם, מבוססת Docker, Docker Compose ו-GitHub Actions.

## 🏗️ ארכיטקטורת המערכת
* **Web Dashboard (`parking-web`)**: שרת Nginx המנגיש את ממשק השומר בפורט `8080`. כולל שליטה על שער החניון, מצב יום/לילה והתראת תפוסה מלאה.
* **Storage Server (`parking-storage`)**: שרת Apache (`httpd`) בפורט `8081` המשמש לאחסון והנגשת תמונות לוחיות הרישוי.
* **Data Persistence**: שימוש ב-Named Volume (`parking_images`) הממופה לתיקיית התמונות ב-Apache, כך שהתמונות נשמרות גם לאחר הסרת הקונטיינרים (`docker compose down`).

## 🚀 הוראות הרצה
1. שכפול המאגר:
   ```bash
   git clone <YOUR-REPO-URL>
   cd smart-parking-tracker