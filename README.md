# Team Radar – GitHub Pages

صفحة رادار للفريق. ارفع هذا المجلد على GitHub وفعّل GitHub Pages، ثم شارك الرابط مع صديقك مع رابط ngrok.

---

## الخطوات على GitHub

### 1) إنشاء مستودع جديد (New repository)

1. ادخل إلى [github.com](https://github.com) وسجّل الدخول.
2. اضغط **New** (أو **+** → **New repository**).
3. **Repository name:** مثلاً `team-radar` (أي اسم).
4. اختر **Public**.
5. **لا** تختر "Add a README" (هذا المجلد فيه الملفات مسبقاً).
6. اضغط **Create repository**.

---

### 2) رفع الملفات

**طريقة أ: من المتصفح (الأبسط)**

1. داخل المستودع الجديد اضغط **Add file** → **Upload files**.
2. اسحب مجلد `github-pages-radar` كامل، أو افتحه واسحب الملفين:
   - `index.html`
   - `README.md`
3. اكتب تحت **Commit changes** رسالة مثل: `Add radar page`.
4. اضغط **Commit changes**.

**طريقة ب: من سطر الأوامر (إن كان عندك Git)**

```bash
cd github-pages-radar
git init
git add index.html README.md
git commit -m "Add radar page"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/team-radar.git
git push -u origin main
```

(غيّر `YOUR_USERNAME` و `team-radar` حسب اسم حسابك والمستودع.)

---

### 3) تفعيل GitHub Pages

1. داخل المستودع اضغط **Settings**.
2. من القائمة اليسرى اختر **Pages** (تحت "Code and automation").
3. تحت **Build and deployment**:
   - **Source:** اختر **Deploy from a branch**.
   - **Branch:** اختر `main` (أو `master`) والمجلد **/ (root)**.
4. اضغط **Save**.

انتظر دقيقة أو دقيقتين، ثم ادخل مرة ثانية إلى **Settings → Pages**: راح يظهر لك الرابط، غالباً بهذا الشكل:

```
https://YOUR_USERNAME.github.io/team-radar/
```

هذا هو رابط الصفحة.

---

## كيف يستخدمها صديقك (من دولة ثانية)

**من جهازك (أنت اللي تلعب):**

1. شغّل البرنامج وافتح **Web Radar** (البورت 8765).
2. شغّل ngrok:  
   `ngrok http 8765`  
   وانسخ رابط ngrok، مثلاً:  
   `https://abc123.ngrok-free.app`

**الرابط اللي تعطيه لصديقك:**

```
https://YOUR_USERNAME.github.io/team-radar/?api=https://abc123.ngrok-free.app
```

- غيّر `YOUR_USERNAME` و `team-radar` حسب مستودعك.
- غيّر `https://abc123.ngrok-free.app` برابط ngrok اللي يظهر عندك كل مرة تشغّل فيها ngrok.

صديقك يفتح الرابط من أي دولة، يختار اسمه من **I am:** ويشوف الرادار.

---

## ملاحظات

- كل مرة تشغّل فيها ngrok راح يتغير الرابط، فحدّث الرابط اللي ترسله لصديقك (أو يكتبه في خانة **Server URL** في الصفحة ويضغط **Apply**).
- الصفحة تعمل أيضاً بدون استضافة: لو فتحها من جهازك على `http://localhost:8765` ما تحتاج تكتب Server URL.
