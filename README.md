<div align="center">

# 💰 ميزانيتي | AzizBudget

### راتبك ومصاريفك والمتبقي… كلّها قدامك، بدون تعقيد 🐧

**برنامج ميزانية شخصي مجاني لأجهزة Linux، بواجهة عربية بسيطة ومريحة.**

**الإصدار:** `v1.2` · **النظام المستهدف:** Ubuntu / Linux Mint · **التقنيات:** Python 3 + PySide6 (Qt)

</div>

---

## ✨ وش هو «ميزانيتي»؟

**ميزانيتي (AzizBudget)** تطبيق سطح مكتب يساعدك ترتّب ميزانيتك الشهرية بسهولة: تدخل راتبك ودخلك الإضافي، وتسجّل مصاريفك، وتشوف مباشرة كم صرفت وكم باقي لك من الشهر.

فكرته بدأت من جدول Excel شخصي، وتحوّلت إلى برنامج مستقل تقدر تفتحه من قائمة التطبيقات وتستخدمه يوميًا. **في التثبيت الجديد تبدأ الميزانية من الصفر** وتضيف دخلك ومصاريفك بنفسك؛ أما التحديث فلا يُصفّر البيانات المحفوظة.

## 🚀 المميزات

| الميزة | الوصف |
|---|---|
| 💵 متابعة الدخل | تسجيل الراتب الشهري والدخل الإضافي. |
| 🧾 إدارة المصاريف | إضافة المصروفات وتعديلها وحذفها مع ملاحظة اختيارية. |
| 🗂️ تصنيف المصاريف | فواتير، قروض، مقاضي، أسرة، مواصلات، ادخار، ترفيه، وأخرى. |
| 🧮 حساب تلقائي | عرض إجمالي الدخل والمصاريف والمبلغ المتبقي. |
| 📅 ميزانية أسبوعية | تقسيم المبلغ المتبقي على 1 إلى 5 أسابيع تختارها بنفسك. |
| 📊 نسبة الصرف | مؤشر يوضح نسبة المصروفات من الدخل. |
| 🗓️ متابعة شهرية | التنقل بين الشهور، ولكل شهر بياناته المستقلة. |
| 🔎 تكبير الخط | تصغير وتكبير عناصر الواجهة من 80% إلى 160%، مع حفظ اختيارك. |
| 🌙 واجهة داكنة | تصميم بسيط يدعم اتجاه الكتابة العربية من اليمين لليسار. |
| 📄 تصدير CSV | حفظ كشف الميزانية في ملف يمكن فتحه ببرامج الجداول. |
| 💾 حفظ محلي | تُحفظ بيانات الميزانية على جهازك دون حساب أو مزامنة سحابية. |

## 🐧 تحميل وتثبيت ميزانيتي على Linux

**التثبيت الحالي بملف Bash ذاتي الاستخراج، وليس بحزمة Snap أو RPM أو DEB.** لا تحتاج Snap، ولا تستخدم أوامر تثبيت التطبيقات الأخرى مع هذا الملف.

فُحص محتوى مثبّت v1.2 بتاريخ **17 نوفمبر 2026** لتوثيق مساراته وخطواته. هذه مراجعة للمثبّت، وليست اختبار تشغيل على كل توزيعة.

| النظام | الحالة |
|---|---|
| Ubuntu / Linux Mint | الأنظمة المستهدفة بالمثبّت الحالي |
| Fedora المكتبي التقليدي | خطوات تجهيز Python أدناه؛ تشغيل التطبيق عليه لم يتأكد بعد |
| Debian | خطوات تجهيز المتطلبات أدناه؛ لم يُوثق اختبار التطبيق هنا |
| بقية التوزيعات والمعماريات | تتطلب Python وvenv ومكتبات PySide6 متوافقة؛ لا يوجد ضمان شامل |
| Fedora Silverblue / Kinoite | خطوات dnf أدناه ليست تعليمات مؤكدة لهذه الأنظمة |

المثبّت لا ينفّذ apt أو dnf بنفسه؛ جهّز المتطلبات حسب توزيعتك، ثم شغّل نفس ملف المثبّت. توفر حزمة PySide6 الجاهزة يعتمد على إصدار Python والمعمارية والنظام.

### 1. حمّل الملف الصحيح

افتح [إصدار v1.2](https://github.com/mraziz2005-hue/AzizBudget/releases/tag/v1.2)، ثم **Assets**، وحمّل:

[AzizBudget-1.2-Install-Public.sh](https://github.com/mraziz2005-hue/AzizBudget/releases/download/v1.2/AzizBudget-1.2-Install-Public.sh)

**لا تستخدم `Source code (zip)` أو `Code → Download ZIP` بدل ملف المثبّت.** المستودع يحتوي README فقط حاليًا؛ ملف `.sh` المرفق يحتوي ملفات التطبيق بداخله.

### 2. جهّز المتطلبات — حسب توزيعتك

#### Ubuntu / Linux Mint / Debian

```bash
sudo apt update
sudo apt install python3 python3-venv python3-pip coreutils tar gzip
```

#### Fedora Workstation / KDE التقليدي

```bash
sudo dnf install python3 python3-pip coreutils tar gzip
```

Fedora يستخدم `dnf` بدل `apt`. رسالة المثبّت التي تقترح `python3-venv` تخص Ubuntu / Mint؛ لا تنسخ أمر apt إلى Fedora.

#### توزيعات أخرى

ثبّت Python 3 مع دعم venv وpip، وأدوات Bash وcoreutils وtar وgzip، باستخدام مدير حزم توزيعتك.

تحقق من البيئة:

```bash
python3 --version
python3 -m venv --help
uname -m
```

هذه أوامر فحص؛ لا تعني بمفردها أن مكتبات Qt الرسومية تعمل على الجهاز. قد تحتاج مكتبات نظام إضافية حسب رسالة الخطأ.

### 3. شغّل المثبّت بحسابك العادي

افتح الطرفية داخل مجلد التنزيلات:

```bash
cd ~/Downloads
ls -lh AzizBudget-1.2-Install-Public.sh
bash AzizBudget-1.2-Install-Public.sh
```

إذا كان مجلد التنزيلات باسم مختلف، افتحه في مدير الملفات واختر **فتح الطرفية هنا** بدل أمر `cd ~/Downloads`.

**لا تستخدم `sudo bash` لتثبيت البرنامج.** المثبّت يثبت التطبيق والاختصار داخل حساب المستخدم الحالي. لا تحتاج `chmod +x` عند تشغيل الملف بواسطة `bash`.

التثبيت الأول قد يستغرق وقتًا لتنزيل PySide6. انتظر رسالة نجاح التثبيت.

### ماذا يفعل المثبّت؟

بحسب السكربت المرفق فعلًا:

1. يفك ملفات التطبيق المؤرشفة بعد فحص سلامتها.
2. يتحقق من وجود Python 3.
3. ينشئ بيئة `.venv` داخل مجلد التطبيق باستخدام `--system-site-packages`.
4. يتحقق من توفر PySide6، ويثبّت `PySide6>=6.8,<7` من حزم جاهزة إذا احتاج ذلك.
5. يجري فحصًا لـ Qt وحقول النص العربية دون فتح نافذة.
6. ينسخ ملفات التطبيق ويضيف اختصارًا إلى قائمة التطبيقات.
7. يحتفظ بنسخة من ملف الواجهة السابق عند وجوده؛ هذه ليست نسخة كاملة من الميزانية.

مجلد بيانات الميزانية منفصل عن ملفات التطبيق، والمثبّت لا يحذفه أو يصفره. فحص Qt أثناء التثبيت لا يغني عن تجربة النافذة والحفظ على توزيعتك.

### 4. افتح البرنامج

ابحث في قائمة التطبيقات عن:

- **ميزانيتي** في الواجهة العربية.
- **Aziz Budget** في الواجهة الإنجليزية، مع مسافة بين الكلمتين.

قد يظهر بأيقونة آلة حاسبة؛ هذا هو الاختصار الذي ينشئه المثبّت.

للتشغيل المباشر من الطرفية:

```bash
"$HOME/.local/share/aziz-budget-app/.venv/bin/python" "$HOME/.local/share/aziz-budget-app/aziz_budget.py"
```

هذا هو نفس المسار الذي يستخدمه اختصار التطبيق. لا تحتاج تفعيل البيئة يدويًا، ولا تستخدم `sudo` للتشغيل.

بعد نجاح التثبيت يمكنك حذف ملف التنزيل `.sh`؛ التطبيق المثبّت لا يعتمد على بقائه.

### 5. إذا لم يظهر في قائمة التطبيقات

جرّب البحث بالاسمين **ميزانيتي** و**Aziz Budget** أولًا، ثم أغلق القائمة وافتحها. إذا لم تتحدث، سجّل خروجًا وادخل مجددًا.

افحص ملف الاختصار:

```bash
ls -l "$HOME/.local/share/applications/aziz-budget.desktop"
```

إذا كان موجودًا، افحص الاسم وأمر التشغيل:

```bash
cat "$HOME/.local/share/applications/aziz-budget.desktop"
```

ثم جرّب أمر التشغيل المباشر في الخطوة 4.

إذا كان الاختصار مفقودًا، أغلق البرنامج وأعد تشغيل المثبّت **بحسابك العادي** لإعادة إنشائه. لا تستخدم روابط اختصارات Snap؛ ميزانيتي ليس مثبتًا بواسطة Snap.

إذا ظهر التطبيق في القائمة لكنه لا يفتح، شغّله من الطرفية للحصول على رسالة الخطأ؛ إعادة إنشاء الاختصار وحدها لا تصلح مشكلة مكتبات Python أو Qt.

### 🔄 تحديث البرنامج

أغلق التطبيق واحتفظ بنسخة احتياطية من بياناتك، ثم حمّل مثبّت الإصدار الجديد من [Releases](https://github.com/mraziz2005-hue/AzizBudget/releases) واتبع تعليماته.

تحديثات GitHub ليست تلقائية. مثبّت v1.2 يحافظ على مجلد البيانات المنفصل. لا تنقل بيئة `.venv` بين الأجهزة أو التوزيعات؛ أعد التثبيت على الجهاز الجديد وانقل البيانات فقط عند الحاجة.


## 🧭 طريقة الاستخدام

1. اكتب **الراتب الشهري** وأي **دخل إضافي**، ثم احفظ الدخل.
2. أضف كل مصروف باسمه ومبلغه وتصنيفه، ويمكنك كتابة ملاحظة.
3. راقب **إجمالي المصاريف** و**المبلغ المتبقي** في أعلى الشاشة.
4. اختر عدد الأسابيع لمعرفة **المتاح لكل أسبوع**.
5. عدّل أو احذف المصروفات من السجل عند الحاجة، أو صدّر الميزانية إلى CSV.

يمكنك استخدام زري **+** و**−** أعلى الواجهة لتغيير حجم الخط.

## 🔒 الخصوصية وحفظ البيانات

البرنامج يعمل **محليًا**، ولا يرسل بيانات الراتب أو المصروفات إلى خادم. الإنترنت مطلوب لتنزيل اعتماديات التثبيت، وليس لعمليات الميزانية اليومية.

ملفاتك الشخصية تُحفظ في:

```text
~/.local/share/aziz-budget/
├── data.json            # بيانات الميزانيات الشهرية
├── data.backup.json     # نسخة احتياطية محلية
└── preferences.json     # إعداد حجم الخط
```

يُثبَّت البرنامج نفسه في مجلد منفصل:

```text
~/.local/share/aziz-budget-app/
```

**تنبيه:** تنزيل التطبيق على جهاز آخر لا ينقل الميزانية تلقائيًا؛ لكل جهاز بياناته المحلية.

## 💾 النسخ الاحتياطي ونقل الميزانية

أغلق التطبيق ثم انسخ المجلد التالي كاملًا إلى مكان تختاره:

```text
~/.local/share/aziz-budget/
```

يمكنك فتحه من مدير الملفات بإظهار الملفات المخفية أو لصق المسار. ملف `data.backup.json` نسخة محلية سابقة، وليس سجل نسخ احتياطية غير محدود.

للنقل إلى جهاز آخر:

1. ثبّت البرنامج على الجهاز الجديد.
2. أغلق البرنامج على الجهازين.
3. احتفظ بنسخة من بيانات الجهاز الجديد إذا كانت موجودة.
4. انسخ محتويات مجلد البيانات القديم إلى نفس مسار البيانات في حساب الجهاز الجديد.
5. افتح البرنامج وتحقق من الشهور والدخل والمصاريف.

النقل اليدوي **يستبدل** الملفات المطابقة ولا يدمج ميزانيتين تلقائيًا. ملفات JSON محلية، ولا يعني ذلك أنها مشفرة؛ احفظ النسخ الاحتياطية في مكان خاص.

المسارات الموثقة هي الافتراضية. الكود يتيح تغيير مجلد البيانات بواسطة المتغير `AZIZ_BUDGET_DATA_DIR`؛ إذا ضبطته يدويًا، انسخ مجلدك الفعلي بدل الافتراضي.

## 🛠️ حل المشكلات الشائعة

| المشكلة | الخطوة المناسبة |
|---|---|
| `No such file or directory` للمثبّت | تأكد من اسم الملف ومجلد التنزيل باستخدام `pwd` و`ls` |
| Python غير موجود | ثبّت المتطلبات المناسبة لتوزيعتك |
| تعذر إنشاء venv على Ubuntu / Mint / Debian | ثبّت python3-venv ثم أعد المثبّت |
| `apt: command not found` على Fedora | استخدم dnf؛ رسالة apt داخل المثبّت موجهة لـ Ubuntu / Mint |
| تعذر تنزيل PySide6 | راجع الإنترنت ورسالة pip وإصدار Python والمعمارية |
| `No matching distribution found` | قد لا تتوفر حزمة PySide6 جاهزة لبيئتك؛ أرفق إصدار Python والمعمارية والخطأ |
| `ModuleNotFoundError: PySide6` عند التشغيل | استخدم أمر التشغيل الكامل لبيئة التطبيق، ثم أعد المثبّت إن استمرت المشكلة |
| خطأ Qt أو xcb أو Wayland | شغّل من الطرفية وأرفق الرسالة لتحديد مكتبة النظام الناقصة؛ لا تبدّل الإعدادات عشوائيًا |
| التطبيق غير ظاهر بالقائمة | ابحث عن «ميزانيتي» و«Aziz Budget»، واتبع خطوة فحص الاختصار |
| البيانات غير موجودة على جهاز آخر | لا توجد مزامنة تلقائية؛ اتبع قسم نقل الميزانية |

للتشخيص:

```bash
cat /etc/os-release
python3 --version
uname -m
"$HOME/.local/share/aziz-budget-app/.venv/bin/python" "$HOME/.local/share/aziz-budget-app/aziz_budget.py"
```

أرسل الخطأ واسم التوزيعة في [Issues](https://github.com/mraziz2005-hue/AzizBudget/issues)، دون نشر ملفات ميزانيتك أو راتبك ومصاريفك.

## 🗑️ إزالة البرنامج مع الاحتفاظ بالبيانات

أغلق التطبيق أولًا. من مدير الملفات احذف **ملفات التطبيق والاختصار فقط**:

```text
~/.local/share/aziz-budget-app/
~/.local/share/applications/aziz-budget.desktop
```

**اترك مجلد `~/.local/share/aziz-budget/` كما هو إذا تريد الاحتفاظ بميزانيتك.** حذف التطبيق لا يتطلب حذف Python أو مكتبات النظام.

## 📚 مراجع البيئة

رُوجع ملف المثبّت الفعلي وتعليمات التثبيت بتاريخ **17 نوفمبر 2026**.

- [Python على Fedora](https://developer.fedoraproject.org/tech/languages/python/python-installation.html)
- [pip والبيئات الافتراضية على Fedora](https://developer.fedoraproject.org/tech/languages/python/pypi-installation.html)

## 📌 حالة المشروع

**الإصدار الحالي: v1.2**

- يدعم الكتابة العربية داخل حقول الإدخال باستخدام Qt / PySide6.
- يوفّر حفظ الميزانيات محليًا، وتكبير الخط، وتصدير CSV.
- ليس تطبيقًا سحابيًا، ولا يزامن البيانات بين الأجهزة.
- لم يُنشر على Snap Store حتى الآن، والتثبيت الحالي متاح عبر ملف GitHub Release.

## 🌍 English — Quick overview

**AzizBudget (ميزانيتي)** is a lightweight, Arabic-first personal budgeting desktop app for Linux.

Track your salary, additional income, and categorized expenses; view your remaining balance, spending percentage, and a weekly spending allowance. It also includes monthly budgets, CSV export, adjustable text scaling (80–160%), and local data storage.

**Target platforms:** Ubuntu / Linux Mint; Fedora setup is documented but app execution there is not yet confirmed.  
**Technology:** Python 3 + PySide6 (Qt)  
**Prepare dependencies:**

Ubuntu / Linux Mint / Debian:

```bash
sudo apt update
sudo apt install python3 python3-venv python3-pip coreutils tar gzip
```

Traditional Fedora:

```bash
sudo dnf install python3 python3-pip coreutils tar gzip
```

**Install:** Download `AzizBudget-1.2-Install-Public.sh` from **Releases**, open a terminal in the download folder, and run:

```bash
bash AzizBudget-1.2-Install-Public.sh
```

Run the installer as your normal user, **without sudo**. This is a self-extracting Bash installer, not a Snap. The automatically generated repository ZIP is not a substitute.

Search the application menu for **ميزانيتي** or **Aziz Budget**, or launch directly:

```bash
"$HOME/.local/share/aziz-budget-app/.venv/bin/python" "$HOME/.local/share/aziz-budget-app/aziz_budget.py"
```

The desktop shortcut is `~/.local/share/applications/aziz-budget.desktop`. Budget data lives separately in `~/.local/share/aziz-budget/`; back up that folder before migrating or updating.

The installer may download PySide6 on the first run. The app then works offline. User data stays on each device; cloud sync and automatic updates are not included.

---

<div align="center">

**صُنع ببساطة… لأن ميزانيتك ما تحتاج جدولًا معقدًا.** 💰

Made with 🐧 for Linux users.

</div>
