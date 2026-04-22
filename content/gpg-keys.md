+++
title = "GPG Key Commands"
+++

## gpg-key commands

🔑 مدیریت کلیدهای خودت (Identity)
این بخش برای ایجاد و بررسی شناسنامه دیجیتال توست.

ساخت کلید جدید (حرفه‌ای و تعاملی):
```
gpg --expert --full-generate-key
```
مشاهده لیست کلیدهای عمومی:
```
gpg --list-keys --keyid-format SHORT
```
مشاهده لیست کلیدهای خصوصی (فوق محرمانه):
```
gpg --list-secret-keys --keyid-format SHORT
```
مشاهده اثر انگشت (Fingerprint) کلید:
```
gpg --fingerprint [Email_Or_KeyID]
```
📤 خروجی گرفتن و پشتیبان‌گیری (Export)
مهم: حتماً از کلید خصوصی خود بک‌آپ بگیرید و در جای امن (آفلاین) نگه دارید.

خروجی کلید عمومی (برای اشتراک‌گذاری):
```
gpg --armor --export [KeyID] > public_key.asc
```
خروجی کلید خصوصی (بک‌آپ حساس):
```
gpg --armor --export-secret-keys [KeyID] > private_key.asc
```
ساخت فایل ابطال (Revocation Certificate):
```
gpg --gen-revoke [KeyID] > revoke.asc
```
(اگر کلیدت گم یا هک شد، با این فایل به دنیا اعلام می‌کنی که دیگر معتبر نیست).

📨 مدیریت کلیدهای دیگران (Import & Trust)
زمانی که می‌خواهی کلید دوستانت را اضافه کنی یا با سرورهای جهانی تعامل داشته باشی.

وارد کردن کلید عمومی دیگران:
```
gpg --import friend_key.asc
```
جستجوی کلید یک نفر در اینترنت:
```
gpg --keyserver keys.openpgp.org --search-keys [Email]
```
ارسال کلید خودت به سرور جهانی:
```
gpg --keyserver keys.openpgp.org --send-keys [KeyID]
```
تازه کردن کلیدها (آپدیت انقضای کلیدهای دوستان):
```
gpg --refresh-keys
```

🔒 رمزنگاری و امضا (Files & Messages)
دستوراتی برای قفل کردن و مهر و موم کردن فایل‌ها در ترمینال.

رمزنگاری یک فایل برای گیرنده خاص:
```
gpg --encrypt --recipient [Friend_Email] secret.txt
```

رمزگشایی (Decrypt) یک فایل یا پیام:
```
gpg --decrypt secret.txt.gpg
```

فقط امضا کردن متن (Clearsign):
```
gpg --clearsign document.txt
```
(یک فایل متنی می‌سازد که محتوا خوانا است اما امضا به انتهای آن چسبیده).

تایید اصالت یک فایل امضا شده:
```
gpg --verify document.txt.asc
```

🗑️ پاک‌سازی (Delete)
حذف کلید عمومی:
```
gpg --delete-keys [KeyID]
```

حذف کلید خصوصی:
```
gpg --delete-secret-keys [KeyID]
```

💡 چند ترفند کوتاه:
رمزنگاری سریع با پسورد (بدون کلید):
```
gpg --symmetric file.txt
```
(این دستور از تو یک پسورد می‌خواهد و فایل را قفل می‌کند؛ برای باز کردنش هم فقط همان پسورد لازم است).

خروجی مستقیم به ترمینال:
اگر می‌خواهی کلید عمومی‌ات را سریع کپی کنی و در چت بفرستی:
```
gpg --armor --export [KeyID] 
```
(بدون علامت < و نام فایل).
