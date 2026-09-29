# 🧪 Wadie - Pentest Toolkit

أداة تدريبية للفحص الأمني على السيرفرات المحلية فقط (Termux).

---

## ⚠️ تحذير قانوني

هاد الأداة **للتدريب القانوني فقط**. استعمالها على أي سيرفر ماشي ديالك بلا إذن كتابي = جريمة.

| مسموح ✅ | ممنوع ❌ |
|---|---|
| 127.0.0.1 (السيرفر ديالك) | مواقع الناس |
| TryHackMe / HTB | البنوك |
| DVWA / VulnHub | الحكومة |
| سيرفراتك الخاصة | أي هدف بلا إذن |

---

## 📥 التثبيت

### 1) نصب المتطلبات

```bash
pkg update && pkg upgrade -y
pkg install python nmap curl hydra sqlmap gobuster perl git -y
pip install requests
```

### 2) نصب الأدوات المساعدة

```bash
git clone https://github.com/sullo/nikto ~/nikto
git clone https://github.com/danielmiessler/SecLists ~/SecLists
```

### 3) حمل الأداة

```bash
git clone https://github.com/wadiehadouu3-hash/Wadie.git
cd Wadie
chmod +x pentest.sh
```

---

## 🚀 الاستعمال

```bash
./pentest.sh
```

---

## 🛠️ الميزات

| # | الميزة | الأداة |
|---|---|---|
| 1 | فحص البورتات | nmap |
| 2 | فحص الويب | Nikto |
| 3 | اكتشاف المسارات | gobuster |
| 4 | SQL Injection | sqlmap |
| 5 | XSS | curl + payloads |
| 6 | Hydra SSH | hydra |
| 7 | HTTP Headers | curl |

---

## 📖 مثال عملي

### طرفية 1 — شغل السيرفر المحلي

```bash
cd ~/lab
php -S 127.0.0.1:8080
```

### طرفية 2 — شغل الأداة

```bash
cd ~/Wadie
./pentest.sh
```

من بعد فالأداة:
```
اختار: 0
دخل الهدف: 127.0.0.1
دخل البورت: 8080

اختار: 1    # فحص البورتات
اختار: 2    # Nikto
اختار: 3    # SQL Injection
اختار: 4    # XSS
```

---

## 📜 الترخيص

MIT License - شوف [LICENSE](LICENSE)

---

## ⚖️ إخلاء المسؤولية

المطور **ماشي مسؤول** عن أي استعمال غير قانوني للأداة. المستخدم هو المسؤول الوحيد.
