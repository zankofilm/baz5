# اصلاح Build نسخه 1.0.2

این نسخه برای خطای مرحله `Build debug APK` در GitHub Actions آماده شده است.

تغییرات اصلی:

- Kotlin Gradle Plugin از 2.2.20 به 2.4.21 ارتقا یافت تا با AGP 8.13.2 و Gradle 8.13 در بازه رسمی سازگاری باشد.
- Compose Compiler plugin نیز با Kotlin روی 2.4.21 هم‌نسخه شد.
- Build Tools به‌صورت صریح روی 36.0.0 تنظیم شد تا با پکیج نصب‌شده در CI یکسان باشد.
- dependency صریح `kotlinx-coroutines-android` اضافه شد.
- Workflow خروجی کامل Gradle را در `build.log` ذخیره و حتی در صورت شکست به‌عنوان Artifact با نام `BAZR-build-log` بارگذاری می‌کند.

اگر Build باز هم شکست خورد، Artifact به نام `BAZR-build-log` را از همان Run دانلود کنید؛ خطای دقیق داخل آن خواهد بود.
