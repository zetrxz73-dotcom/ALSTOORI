السطوري ALSTOORI — مشروع Android APK
=====================================

مهم: هذا مشروع Android أصلي (Java + WebView) جاهز للفتح في Android Studio.
لم أرفق APK جاهزاً لأن بيئة إنشاء الملفات الحالية لا تحتوي على Android SDK أو Gradle،
ولذلك لا يمكنني تنفيذ عملية التجميع والتحقق من APK هنا. لا أريد أن أرسل لك ملفاً
بامتداد APK وهو ليس تطبيقاً صالحاً.

كيفية إنشاء APK على الكمبيوتر:
1. ثبّت Android Studio من الموقع الرسمي:
   https://developer.android.com/studio
2. فك ضغط ALSTOORI_Android_Project.zip.
3. افتح Android Studio ثم اختر Open وحدد مجلد ALSTOORI_Android_Project.
4. وافق على تثبيت Android SDK Platform 35 وAndroid Gradle Plugin/Gradle عند الطلب.
5. انتظر انتهاء Gradle Sync.
6. من القائمة اختر Build > Build Bundle(s) / APK(s) > Build APK(s).
7. بعد نجاح البناء ستجد الملف غالباً في:
   app/build/outputs/apk/debug/app-debug.apk
8. انقل APK إلى هاتف Android وثبّته. قد تحتاج السماح بالتثبيت من هذا المصدر.

ما الذي يفعله مشروع Android:
- يفتح واجهة السطوري داخل تطبيق Android.
- يحفظ الأوامر المخصصة والمفضلة واللغة محلياً.
- يدعم العربية والإنجليزية والصينية المبسطة واليابانية.
- يتيح اختيار ملفات JSON للاستيراد.
- يحفظ ملفات JSON وmcpack التي ينشئها المحرر في Downloads/ALSTOORI.
- زر فتح Minecraft يحاول تشغيل تطبيق Minecraft Bedrock المثبت على الهاتف.

تنبيهات:
- قفل كلمة المرور داخل النسخة الحالية قفل محلي بسيط، وليس تشفيراً أمنياً للبيانات.
- لا يتحكم التطبيق مباشرة بعالم Minecraft ولا يحقن الأوامر فيه؛ انسخ الأمر والصقه في دردشة اللعبة.
- محرر الإضافات ينشئ هيكل حزمة أولياً، وليس محرراً كاملاً للنماذج ثلاثية الأبعاد أو الخامات أو السكربتات.
- توافق أوامر Bedrock يعتمد على إصدار اللعبة والصلاحيات والتجارب المفعلة.
- التطبيق مستقل وغير تابع لـ Mojang أو Microsoft.

المتطلبات:
- Android Studio حديث
- Android SDK Platform 35
- JDK 17 (يوفره Android Studio عادة)
- هاتف Android 10 أو أحدث للتطبيق الحالي


طريقة بناء APK عبر GitHub Actions (بدون تثبيت Android Studio على هاتفك):
1. أنشئ مستودعاً جديداً في GitHub من المتصفح.
2. ارفع ملفات المشروع ومجلداته بعد فك الضغط (يجب أن يبقى مجلد .github موجوداً).
3. افتح تبويب Actions في المستودع.
4. اختر "Build ALSTOORI APK" ثم Run workflow.
5. بعد نجاح المهمة، افتح صفحة التشغيل المكتمل ونزّل Artifact باسم ALSTOORI-debug-apk.
6. فك ضغط artifact لتحصل على app-debug.apk.

هذه الطريقة تحتاج حساب GitHub واتصال إنترنت. لا ترفع مفاتيح أو بيانات شخصية إلى المستودع.
