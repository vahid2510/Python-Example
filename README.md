# Python-Example
# 🐍 200 Weird & Creative Python Snippets

**۲۰۰ قطعه کد خلاقانه، عجیب و جالب پایتون**

---

## 🎯 About the Project / دربارهٔ پروژه

This repository contains **200 short Python snippets (each up to 15 lines)** designed to showcase creativity, unexpected logic combinations, and surprising outputs. Every piece of code demonstrates how flexible and playful Python can be when used inventively.
این مخزن شامل **۲۰۰ قطعه کد کوتاه پایتون (حداکثر ۱۵ خط)** است که برای نمایش خلاقیت، ترکیب‌های غیرمنتظرهٔ مفاهیم و خروجی‌های جالب یا عجیب نوشته شده‌اند. هر کد نشان می‌دهد پایتون چقدر می‌تواند انعطاف‌پذیر و بازیگوش باشد.

Each snippet:

* Is entirely original and imaginative
* Uses unconventional or funny logic
* Relies only on Python’s standard library
* Produces interesting, strange, or aesthetic output
* Combines concepts like `lambda`, `itertools`, `contextlib`, `decorators`, and `__magic_methods__`

هر کد:

* کاملاً جدید و ابداعی است
* از منطق‌های غیرمعمول و خلاقانه استفاده می‌کند
* فقط از کتابخانه‌های استاندارد پایتون بهره می‌برد
* خروجی‌های منحصربه‌فرد و جالب تولید می‌کند
* ترکیبی از مفاهیم `lambda`، `itertools`، `contextlib`، `decorator` و متدهای جادویی دارد

---

## ⚗️ Repository Structure / ساختار مخزن

| File                              | توضیح                             |
| --------------------------------- | --------------------------------- |
| `200_weird_python_snippets.ipynb` | شامل ۲۰۰ قطعه کد با توضیحات فارسی |
| `README.md`                       | فایل توضیحات اصلی (همین فایل)     |


---

## 🧠 Concepts Used / مفاهیم استفاده‌شده

This project creatively mixes many core Python ideas, including:
در این پروژه، مفاهیم بنیادی پایتون به‌صورت خلاقانه ترکیب شده‌اند:

* **Nested loops / حلقه‌های تو در تو** برای ایجاد الگوهای تکرارشونده
* **List comprehensions / لیست‌کامپرهنشن‌های چندسطحی** برای فشرده‌سازی منطق در یک خط
* **Nested dictionaries / دیکشنری‌های تو در تو** برای داده‌های پویا
* **Lambda functions / توابع λ** برای تعریف سریع رفتارها
* **Generator expressions / ژنراتورها** برای تولید دادهٔ lazy
* **Context managers / مدیریت‌گرهای زمینه** مثل وارونه‌کنندهٔ چاپ
* **Decorators / دکوریتورها** برای تغییر رفتار توابع
* **Magic methods / متدهای جادویی** برای رفتارهای غیرمنتظره (مثل `@`, `~`, `[]`)
* **itertools و functools** برای ترکیب و تکرار داده‌ها

---

## 🚀 How to Use / نحوهٔ استفاده

1. Download the main file / فایل اصلی را دانلود کنید:

   ```bash
   200_weird_python_snippets.ipynb
   ```
2. Copy and run any snippet / یکی از کدها را در پایتون اجرا کنید:

   ```python
   # Example: Code #17 / مثال: کد ۱۷
   class Flip:
       def __init__(self,v): self.v=v
       def __invert__(self): return Flip(str(self.v)[::-1])
       def __repr__(self): return f"Flip({self.v})"
   print(~Flip(2025))
   ```
3. Observe the output / خروجی را ببینید و لذت ببرید.

---

## 🧩 Sample Snippets / نمونه‌کدها

### 🔹 Code 7 / کد ۷: وارونه‌کنندهٔ چاپ

```python
import contextlib, sys
@contextlib.contextmanager
def reversed_print():
    class W:
        def write(self, s): sys.__stdout__.write(s[::-1])
    old = sys.stdout; sys.stdout = W()
    try: yield
    finally: sys.stdout = old

with reversed_print():
    print("Hello 7")
```

**Explanation / توضیح:** Prints everything backward. هر چیزی که چاپ می‌کنی را برعکس نمایش می‌دهد.

---

### 🔹 Code 18 / کد ۱۸: ماشین جمعی زنجیره‌ای

```python
class S:
    def __init__(self): self.t=0
    def __call__(self,*xs): self.t+=sum(xs); return self
    def __repr__(self): return f"Σ={self.t}"

print(S()(1,3,2)(4)(-2))
```

**Explanation / توضیح:** A callable class that accumulates sums. کلاسی که جمع را در هر فراخوانی حفظ می‌کند.

---

## 💡 Purpose / هدف پروژه

This project is meant for:

* Practicing creative coding
* Learning Python’s hidden features through fun examples
* Inspiring mini-projects and experiments

هدف این پروژه:

* تمرین خلاقیت در برنامه‌نویسی
* یادگیری ویژگی‌های پنهان پایتون با مثال‌های سرگرم‌کننده
* الهام‌گیری برای پروژه‌ها و ایده‌های کوچک

---

## 🧭 Inspiration / الهام

Inspired by the beauty of concise, poetic code.
الهام‌گرفته از زیبایی کدهای فشرده و شاعرانه.

> Programming isn’t always science — sometimes it’s poetry written in logic.
> برنامه‌نویسی همیشه علم نیست — گاهی شعری است که با منطق نوشته می‌شود.

---

## 🧾 License / مجوز

Released under the **MIT License**. Feel free to use and share with credit.
منتشرشده تحت مجوز **MIT**؛ استفاده و بازنشر آزاد است با ذکر منبع.

---

## ❤️ Support / پشتیبانی

If you enjoy this project:
⭐️ **Star** the repo and share your weird Python ideas!
اگر از پروژه لذت بردی، **ستاره بده** و ایده‌های عجیب خودت را به اشتراک بگذار.

