# النوتة الروحية

برنامج الأطفال (ابتدائي): الصلاة، الإنجيل، القداس، الصوم (الأربع والجمعة)، والاعتراف مرة في الشهر.
ملف واحد `index.html` + `manifest.json`، على نفس مشروع Firebase بتاع STMina.

## قبل التشغيل
1. في `index.html` املا `apiKey` و`appId` و`messagingSenderId` (من Firebase Console > Project settings).
2. فعّل **Anonymous** في Firebase Authentication.
3. ادمج `firestore.rules.txt` في `firestore.rules` بتاع STMina **قبل** القاعدة الأخيرة (`match /{document=**}`) وانشرها.
4. لو App Check مفعّل: حط `RECAPTCHA_SITE_KEY` (نفس مفتاح STMina).

## الداتا
- `kid_codes/{الكود}` = `{ childId, name }` (الخادم هيعملها من STMina لاحقًا).
- `kid_devices/{uid}` = `{ code, childId }` (بيتكتب لما الولد يدخل الكود).
- `spiritualNotes/{childId}/days/{yyyy-mm-dd}` و`spiritualNotes/{childId}/months/{yyyy-mm}`.
