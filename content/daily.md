+++
title = "Daily"
+++

## 19/4/2026 - intro
سلام. تا جایی که یادمه همیشه دوست داشتم یه مکان برای نوشتن فکرا و دیدگاهام داشته باشم. حقیقتا تلگرام گزینه مناسبی بود ولی خب نوشتن وبلاگ رو یه دامین شخصی یه حس دیگه ای داشت هه هه هه.  
بهرحال اینجا چیزای روزمره رو نمینویسم. بیشتر نظراتم یا شاید حتی اخبار جدید درمورد تکنولوژی و اپن سورس و بیت کوین و این چیزارو بنویسم. و اینکه اگه واستون سواله چرا اینجا انقدر سادست چون دلم میخواست فضای نوستالژی اینترنت حفظ بشه. از جینگولی بازی دیگه خوشم نمیاد. 
و در آخرم اینکه کلی چیز هست باید یاد بگیرم. امیدوارم اونی که اینجارو چک میکنه واسش جالب باشه این چیزا.  

## 20/4/2026 
درواقع سوال اصلیی که باید از خودمون به عنوان یک شهروند عادی بپرسیم اینه که چه چیزی باارزش تر از امنیت هست ؟  
و چرا چیزهایی مثل نظارت مستقیم دولت ها به روی سرمایه و پیام های ما انقدر ساده پذیرفته شده؟  
آیا واقعا بر اساس منطق تصمیم گرفتیم یا یکسری پروتکل های نظارتی بهمون دیکته شده؟  
بنظرم نیازی به اعتماد به بانک ها نیست. سرمایه من **سرمایه من** است:)


## 21/4/2026
1>  
بنظرم این بهترین ویدیو برای درک دقیق بلاکچینه.  
https://youtu.be/_160oMzblY8?is=SBdOvSY5YsshNrqG

2>  
We must defend our own privacy if we expect to have any. We must come together and create systems which allow anonymous transactions to take place. People have been defending their own privacy for centuries with whispers, darkness, envelopes, closed doors, secret handshakes, and couriers. The technologies of the past did not allow for strong privacy, but electronic technologies do.

We the Cypherpunks are dedicated to building anonymous systems. We are defending our privacy with cryptography, with anonymous mail forwarding systems, with digital signatures, and with electronic money.

Cypherpunks write code. We know that someone has to write software to defend privacy, and since we can't get privacy unless we all do, we're going to write it. We publish our code so that our fellow Cypherpunks may practice and play with it. Our code is free for all to use, worldwide. We don't much care if you don't approve of the software we write. We know that software can't be destroyed and that a widely dispersed system can't be shut down.  
https://www.activism.net/cypherpunk/manifesto.html

## 22/4/2026
بنظرتون میشه یه ایمیل رمزنگاری شده با Terminal User Interface درست کرد ؟ :)  
آپدیت ۲ : اتفاتات جالبی افتاد با gpg key آشنا شدم که درواقع یه کریپتوگرافی نامتقارنه با الگوریتمای مختلف ساخته میشه به اسم خودت و ایمیلت.  
یه تویی به اسم Neomutt وجود داره که درواقع میتونی با وارد کردن اپ پسورد جیمیل (پسوورد معمولی نیست از تنظیمات جیمیل بدست میاد و ۱۶ حرفه) داخل فایل های کانفیگش لاگین بشی تو جیمیلت از طریق ترمینالت.  
در ادامه یه آیدی کوتاه از gpg public key درست میکنی و اونم تو فایل کانفیگ ها اضافه میکنی.(صرفا برای امضا کردن پیام. هر تغییر کوچیکی از طرف هکر ها یا سرور باعث ازبین رفتن اتصال بین نامه و امضا میشه و گیرنده متوجه تغییر تو ساختار نامه میشه)    
در ادامه وقتی میخوای ایمیلتو واسه شخصی بفرستی میتونی تنظیم بکنی که فقط امضا بشه (از طریق کلید عمومی خودت برای اینکه ثابت بشه نامه قطعا از طریق شما ارسال شده و هیچ تغییری نکرده - نامه تکست خالصه و قابل خوندنه اما **قابل تغییر نیست** ) یا رمزنگاریش کنی ( یا فایل هش شده تحویل میده که **قابل خوندن نیست** ) یا جفتش!  
توجه باید داشت که برای ارسال پیام رمزنگاری شده باید پابلیک آیدی طرف مقابل و داشته باشید تا بر اساس آیدی اون شخص ، ایمیل رمزنگاری بشه اینطوری خودتونم نمیتونید چیزی که رمزنگاری کردید و باز کنید و فقط خود شخص مقابل با کلید پرایوتش میتونه باز بکنه!!! ( خیلی باحالهههه) نمیدونم چیزی و جا انداختم یا نه. اگه چیزی باز به ذهنم رسید یا متوجه شدم جایی و شاتباه کردم اصلاح میکنم.

این زیر هم کانفیگ نئومات و قرار میدم  
هم کامندای مورد نیاز gpg 
## neomutt config
```
#-----NEOMUTT CONFIG----------

set realname = "YOUR NAME"
set from = "YOUR E-MAIL"  # ایمیل خودت را اینجا بزن
set use_from = yes


set imap_user = "YOUR E-MAIL"
set imap_pass = "GOOGLE APP PASSWORD"  # همان رمز ۱۶ رقمی گوگل
set folder = "imaps://imap.gmail.com:993"
set spoolfile = "+INBOX"
set postponed = "+[Gmail]/Drafts"
set record = "+[Gmail]/Sent Mail"
set trash = "+[Gmail]/Trash"

set smtp_url = "smtps://YOUR-EMAIL@gmail.com:GOOGLE-APP-PASSWORD@smtp.gmail.com:465/"

set crypt_autosign = yes
set crypt_replysign = yes
set crypt_use_gpgme = yes
set pgp_sign_as = "PUBLIK KEY 'ID' "

set mail_check = 60
set timeout = 10
set sort = reverse-threads
```
## gpg-key commands

🔑 مدیریت کلیدهای خودت (Identity)
این بخش برای ایجاد و بررسی شناسنامه دیجیتال توست.

ساخت کلید جدید (حرفه‌ای و تعاملی):
gpg --expert --full-generate-key

مشاهده لیست کلیدهای عمومی:
gpg --list-keys --keyid-format SHORT

مشاهده لیست کلیدهای خصوصی (فوق محرمانه):
gpg --list-secret-keys --keyid-format SHORT

مشاهده اثر انگشت (Fingerprint) کلید:
gpg --fingerprint [Email_Or_KeyID]

📤 خروجی گرفتن و پشتیبان‌گیری (Export)
مهم: حتماً از کلید خصوصی خود بک‌آپ بگیرید و در جای امن (آفلاین) نگه دارید.

خروجی کلید عمومی (برای اشتراک‌گذاری):
gpg --armor --export [KeyID] > public_key.asc

خروجی کلید خصوصی (بک‌آپ حساس):
gpg --armor --export-secret-keys [KeyID] > private_key.asc

ساخت فایل ابطال (Revocation Certificate):
gpg --gen-revoke [KeyID] > revoke.asc
(اگر کلیدت گم یا هک شد، با این فایل به دنیا اعلام می‌کنی که دیگر معتبر نیست).

📨 مدیریت کلیدهای دیگران (Import & Trust)
زمانی که می‌خواهی کلید دوستانت را اضافه کنی یا با سرورهای جهانی تعامل داشته باشی.

وارد کردن کلید عمومی دیگران:
gpg --import friend_key.asc

جستجوی کلید یک نفر در اینترنت:
gpg --keyserver keys.openpgp.org --search-keys [Email]

ارسال کلید خودت به سرور جهانی:
gpg --keyserver keys.openpgp.org --send-keys [KeyID]

تازه کردن کلیدها (آپدیت انقضای کلیدهای دوستان):
gpg --refresh-keys

🔒 رمزنگاری و امضا (Files & Messages)
دستوراتی برای قفل کردن و مهر و موم کردن فایل‌ها در ترمینال.

رمزنگاری یک فایل برای گیرنده خاص:
gpg --encrypt --recipient [Friend_Email] secret.txt

رمزگشایی (Decrypt) یک فایل یا پیام:
gpg --decrypt secret.txt.gpg

فقط امضا کردن متن (Clearsign):
gpg --clearsign document.txt
(یک فایل متنی می‌سازد که محتوا خوانا است اما امضا به انتهای آن چسبیده).

تایید اصالت یک فایل امضا شده:
gpg --verify document.txt.asc

🗑️ پاک‌سازی (Delete)
حذف کلید عمومی:
gpg --delete-keys [KeyID]

حذف کلید خصوصی:
gpg --delete-secret-keys [KeyID]

💡 چند ترفند کوتاه:
رمزنگاری سریع با پسورد (بدون کلید):
gpg --symmetric file.txt
(این دستور از تو یک پسورد می‌خواهد و فایل را قفل می‌کند؛ برای باز کردنش هم فقط همان پسورد لازم است).

خروجی مستقیم به ترمینال:
اگر می‌خواهی کلید عمومی‌ات را سریع کپی کنی و در چت بفرستی:
gpg --armor --export [KeyID] (بدون علامت < و نام فایل).
