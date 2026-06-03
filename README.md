<div align="center">

### 🌍 IP Geolocation Tracker
### أداة تتبع المواقع الجغرافية لعناوين IP

꧁ঔৣ☬ Muhannad Daher ☬ঔৣ꧂

أداة احترافية لتحديد الموقع الجغرافي لأي عنوان IP مع دعم Tor وواجهة عربية بالكامل

---

![Version](https://img.shields.io/badge/2.8-%EF%BA%8D%EF%BB%B9%EF%BA%BB%EF%BA%AA%EF%BA%8D%EF%BA%AE-blue?style=for-the-badge)<br>
![Platform](https://img.shields.io/badge/%EF%BB%9B%EF%BA%8E%EF%BB%9F%EF%BB%B2%20%EF%BB%9F%EF%BB%B4%EF%BB%A8%EF%BB%9C%EF%BA%B2-%EF%BA%8D%EF%BB%9F%EF%BA%92%EF%BB%B4%EF%BA%8C%EF%BA%94-green?style=for-the-badge&logo=kalilinux)<br>
![Platform](https://img.shields.io/badge/%EF%BA%84%EF%BB%A7%EF%BA%AA%EF%BA%AE%EF%BB%AE%EF%BB%B3%EF%BA%AA-%EF%BA%8D%EF%BB%9F%EF%BA%92%EF%BB%B4%EF%BA%8C%EF%BA%94-green?style=for-the-badge&logo=android)<br>
![Python](https://img.shields.io/badge/3.x-%EF%BA%91%EF%BA%8E%EF%BB%B3%EF%BA%9C%EF%BB%AE%EF%BB%A6-blue?style=for-the-badge&logo=python)<br>
![License](https://img.shields.io/badge/MIT-%EF%BA%8D%EF%BB%9F%EF%BA%98%EF%BA%AE%EF%BA%A7%EF%BB%B4%EF%BA%BA-red?style=for-the-badge)<br>
![Status](https://img.shields.io/badge/%EF%BB%A7%EF%BA%B8%EF%BB%82-%EF%BA%8D%EF%BB%9F%EF%BA%A4%EF%BA%8E%EF%BB%9F%EF%BA%94-blue?style=for-the-badge)

---

**المحتويات:**

</div>

- [المميزات](#-المميزات)
- [طريقة التثبيت والتشغيل](#-طريقة-التثبيت-والتشغيل)
  - [تطبيق 🤖 Termux (Android)](#-android--termux)
  - [نظام 🐉 Kali Linux](#-kali-linux)
- [طريقة الاستخدام](#-طريقة-الاستخدام)
- [إعدادات Tor](#-إعدادات-tor)
- [اختصارات مهمة](#-اختصارات-مهمة)
- [حفظ النتائج](#-حفظ-النتائج)
- [إنشاء اختصار التشغيل](#-إنشاء-اختصار-التشغيل)
- [المطور](#-المطور)
- [الرخصة](#-الرخصة)

---

<div align="center">

## ✨ المميزات

</div>

- 🌍 **تتبع أي عنوان IP** (IPv4 فقط)
- 📍 **تحديد موقعك الحالي** تلقائياً
- 🔒 **دعم Tor** لتغيير عنوان IP والموقع
- 🎨 **واجهة عربية بالكامل** مع ألوان احترافية
- 💾 **حفظ النتائج** كملف JSON
- 🔄 **ثلاثة APIs بديلة** لضمان العمل
- 🖥️ **يعمل على Termux و Kali Linux**

---

<div align="center">

## 🚀 طريقة التثبيت والتشغيل

---

## 📱 Android — Termux

</div>

**الخطوة 1 — تثبيت المتطلبات (مرة واحدة فقط)**
```bash
pkg update && pkg upgrade -y
pkg install python tor curl -y
pip install requests pysocks
```

الخطوة 2 — تثبيت مكتبات العربية (مرة واحدة فقط)

```bash
pip install arabic-reshaper python-bidi
```

الخطوة 3 — تثبيت الخط العربي (مرة واحدة فقط)

```bash
curl -L "https://fonts.gstatic.com/s/notonaskharabic/v33/RrQ5bpV-9Dd1b1OAGA6M9PkyDuVBePeKNaxcsss0Y7bwvc-VaA.ttf" -o ~/.termux/font.ttf
termux-reload-settings
```

⚠️ أغلق Termux تماماً وافتحه من جديد بعد تثبيت الخط

الخطوة 4 — تنزيل الأداة وتشغيلها

```bash
curl -o $PREFIX/bin/mud_ig.py https://raw.githubusercontent.com/mmuhacker/mud-ig/main/mud_ig.py
chmod +x $PREFIX/bin/mud_ig.py
```

الخطوة 5 — إنشاء اختصار التشغيل

```bash
ln -sf $PREFIX/bin/mud_ig.py $PREFIX/bin/ig
```

⚡ أو كل شيء في أمر واحد

```bash
pkg update && pkg upgrade -y && pkg install python tor curl -y && pip install requests pysocks arabic-reshaper python-bidi && curl -L "https://fonts.gstatic.com/s/notonaskharabic/v33/RrQ5bpV-9Dd1b1OAGA6M9PkyDuVBePeKNaxcsss0Y7bwvc-VaA.ttf" -o ~/.termux/font.ttf && termux-reload-settings && curl -o $PREFIX/bin/mud_ig.py https://raw.githubusercontent.com/mmuhacker/mud-ig/main/mud_ig.py && chmod +x $PREFIX/bin/mud_ig.py && ln -sf $PREFIX/bin/mud_ig.py $PREFIX/bin/ig && echo "تم التثبيت بنجاح! يمكنك الآن تشغيل الأداة بكتابة: ig"
```

● أمر التشغيل

```bash
ig
```

---

<div align="center">

🐉 Kali Linux

</div>

الخطوة 1 — تثبيت المتطلبات (مرة واحدة فقط)

```bash
sudo apt update && sudo apt upgrade -y
sudo apt install python3 tor curl -y
pip3 install requests pysocks arabic-reshaper python-bidi
```

الخطوة 2 — تنزيل الأداة

```bash
sudo curl -o /usr/local/bin/mud_ig.py https://raw.githubusercontent.com/mmuhacker/mud-ig/main/mud_ig.py
sudo chmod +x /usr/local/bin/mud_ig.py
```

الخطوة 3 — إنشاء اختصار التشغيل

```bash
sudo ln -sf /usr/local/bin/mud_ig.py /usr/local/bin/ig
```

الخطوة 4 — تشغيل Tor (اختياري)

```bash
sudo service tor start
```

● أمر التشغيل

```bash
ig
```

⚡ أو كل شيء في أمر واحد

```bash
sudo apt update && sudo apt upgrade -y && sudo apt install python3 tor curl -y && pip3 install requests pysocks arabic-reshaper python-bidi && sudo curl -o /usr/local/bin/mud_ig.py https://raw.githubusercontent.com/mmuhacker/mud-ig/main/mud_ig.py && sudo chmod +x /usr/local/bin/mud_ig.py && sudo ln -sf /usr/local/bin/mud_ig.py /usr/local/bin/ig && echo "تم التثبيت بنجاح! يمكنك الآن تشغيل الأداة بكتابة: ig"
```

---

<div align="center">

📖 طريقة الاستخدام

</div>

الخيار الوظيفة
[1] تتبع موقع IP معين (أدخل الIP يدوياً)
[2] تتبع موقعك الحالي تلقائياً
[3] عرض تعليمات الاستخدام
[4] إعدادات Tor
[0] خروج

---

<div align="center">

🔒 إعدادات Tor

</div>

الأداة تكشف Tor تلقائياً عند التشغيل. من قائمة إعدادات Tor يمكنك:

الخيار الوظيفة
[1] عرض حالة Tor
[2] تفعيل Tor
[3] تعطيل Tor
[4] استخدام Tor للطلبات (نعم/لا)
[8] رجوع

<div align="center">

الحالة المعنى
🟢 مفعّل الطلبات تمر عبر Tor (يظهر موقع عقدة Tor)
🔴 معطّل الاتصال المباشر (يظهر موقعك الحقيقي)

---

⌨️ اختصارات مهمة

الاختصار الوظيفة
Ctrl+C إيقاف الأداة فوراً
0 خروج من القائمة الرئيسية
8 رجوع من القوائم الفرعية

---

📂 حفظ النتائج

</div>

عند تتبع أي IP، يتم حفظ النتيجة تلقائياً كملف JSON بالصيغة:

```
ip_94.249.81.43_info.json
```

محتوى الملف:

```json
{
  "ip": "94.249.81.43",
  "الدولة": "Hashemite Kingdom of Jordan",
  "رمز الدولة": "JO",
  "المنطقة": "Amman",
  "المدينة": "Amman",
  "خط العرض": 31.9772088,
  "خط الطول": 35.8373789,
  "مزود الخدمة": "Orange Jordan (ألياف ضوئية)",
  "المصدر": "ipwhois.app"
}
```

---

<div align="center">

🔧 إنشاء اختصار التشغيل

</div>

يتم عمله لمرة واحدة فقط أثناء التثبيت

Termux:

```bash
ln -sf $PREFIX/bin/mud_ig.py $PREFIX/bin/ig
```

Kali Linux:

```bash
sudo ln -sf /usr/local/bin/mud_ig.py /usr/local/bin/ig
```

للتشغيل: اكتب ig واضغط Enter

---

<div align="center">

⚠️ ملاحظات مهمة

</div>

· الأداة تدعم عناوين IPv4 فقط (لضمان حفظ الملفات بشكل صحيح)
· الموقع الجغرافي المعروض تقريبي ويعتمد على سجلات مزود الخدمة
· قد يظهر موقع مركز بيانات المزود وليس موقعك الفعلي بدقة 100%
· عند تفعيل Tor، ستظهر مواقع عقد Tor وليس موقعك الحقيقي

---

<div align="center">

👨‍💻 المطور

Muhannad Daher

https://img.shields.io/badge/GitHub-mmuhacker-black?style=for-the-badge&logo=github

---

📄 الرخصة

MIT License — حر الاستخدام مع ذكر المصدر

---

· أداة تتبع المواقع الجغرافية لعناوين IP
· البيئة: Termux (Android) / Kali Linux
· الإصدار: v2.8

---

Madarik Tools — صُنع بالعربية

⭐ إذا أعجبتك الأداة، لا تنسَ النجمة! ⭐

</div>
```

---
