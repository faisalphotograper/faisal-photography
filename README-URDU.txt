FPFAISAL PHOTOGRAPHY — مکمل ویب سائٹ پیکج

اس ZIP میں شامل ہے:
- index.html: عوامی ویب سائٹ
- admin.html: محفوظ ایڈمن لاگ اِن اور میڈیا اپلوڈ
- css/style.css: موبائل اور کمپیوٹر کے لیے ڈیزائن
- js/app.js: گیلری اور WhatsApp بکنگ فارم
- js/admin.js: ایڈمن اپلوڈ انٹرفیس
- netlify/functions/: سرور سائیڈ لاگ اِن، سیشن، محفوظ Cloudinary دستخط اور گیلری
- netlify.toml: Netlify کی ترتیب

اہم: یہ پیکج موجودہ گفتگو میں دستیاب HTML اور gallery.json کی معلومات کی بنیاد پر دوبارہ تیار کیا گیا ہے۔ اصل مکمل ZIP یا تمام پرانی تصاویر/CSS/JS دستیاب نہیں تھیں؛ اس لیے آپ کی نجی اصل تصاویر اس ZIP میں شامل نہیں ہیں۔ موجودہ Cloudinary اکاؤنٹ میں پہلے سے موجود fp1976 ٹیگ والی تصاویر خودکار گیلری میں آ سکتی ہیں۔

NETLIFY پر لگانے کا طریقہ:
1. ZIP extract کریں۔ اس فولڈر کے اندر موجود فائلیں/فولڈرز Netlify کے Manual deploy میں اپلوڈ کریں۔
2. Netlify Dashboard > Site configuration (یا Project configuration) > Environment variables میں درج ذیل variables شامل کریں:
   ADMIN_PASSWORD = اپنا مضبوط ایڈمن پاس ورڈ
   SESSION_SECRET = کم از کم 32 حروف کا بے ترتیب راز (مثلاً openssl rand -hex 32 سے بنائیں)
   CLOUDINARY_CLOUD_NAME = fgg10278
   CLOUDINARY_API_KEY = آپ کی Cloudinary API Key
   CLOUDINARY_API_SECRET = آپ کی Cloudinary API Secret
3. تمام variables محفوظ کرنے کے بعد Netlify پر نیا deploy کریں۔
4. اپنی سائٹ کھولیں اور /admin.html پر جائیں۔ ADMIN_PASSWORD سے لاگ اِن کریں۔
5. تصویر یا ویڈیو منتخب کرکے Upload securely to Cloudinary دبائیں۔ اپلوڈ شدہ media، fp1976 tag کے ساتھ گیلری میں خود دکھائی دے گا۔

سیکیورٹی:
- ADMIN_PASSWORD، SESSION_SECRET اور CLOUDINARY_API_SECRET صرف Netlify Environment Variables میں رکھیں۔ انہیں HTML/JS یا اس ZIP میں نہ ڈالیں اور کسی کے ساتھ شیئر نہ کریں۔
- Cloudinary API Secret چیٹ میں نہ بھیجیں۔
- Admin session آٹھ گھنٹے بعد ختم ہو جاتا ہے۔

Cloudinary اکاؤنٹ کی تفصیلات Netlify میں خود درج کرنا ہوں گی؛ اس ZIP میں کوئی پاس ورڈ یا API Secret شامل نہیں۔
