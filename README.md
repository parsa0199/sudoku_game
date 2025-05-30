# 🎮 بازی سودوکو با پایتون و Pygame

این پروژه یک بازی سودوکو با استفاده از زبان برنامه‌نویسی پایتون و کتابخانه‌ی Pygame است. شما می‌توانید این بازی را اجرا کنید، اعداد را وارد کنید، و در صورت حل صحیح، پیام برنده شدن را مشاهده کنید.

## ✅ مراحل اجرا

### 1. نصب پیش‌نیازها
ابتدا باید کتابخانه Pygame را نصب کنید:

```bash
pip install pygame
```

## 🧠 ساختار برنامه

این پروژه شامل دو کلاس اصلی است:

- **SudokuBoard**: برای منطق سودوکو (تولید جدول، بررسی حرکت‌های معتبر، حل مسئله با الگوریتم backtracking)
- **SudokuGUI**: برای نمایش گرافیکی بازی و تعامل با کاربر

## ✳️ کلاس SudokuBoard

این کلاس وظیفه مدیریت جدول سودوکو را دارد.

### متدهای اصلی:

- **`__init__`**: ساخت جدول خالی و تولید یک پازل تصادفی سودوکو
- **`is_valid_placement(row, col, num)`**: بررسی می‌کند که آیا عدد مشخص شده را می‌توان در آن خانه قرار داد یا نه
- **`find_empty_cell()`**: پیدا کردن اولین خانه خالی از جدول
- **`solve()`**: حل جدول با استفاده از الگوریتم بازگشتی backtracking
- **`generate_puzzle(difficulty=5)`**: تولید جدول اولیه و حذف تعدادی خانه بر اساس میزان سختی
- **`is_board_complete_and_valid()`**: بررسی کامل بودن جدول و معتبر بودن اعداد آن
- **`is_cell_fixed(row, col)`**: بررسی اینکه آیا خانه‌ی مشخص‌شده از ابتدا ثابت بوده یا خیر

## 💻 کلاس SudokuGUI

این کلاس رابط گرافیکی بازی را با استفاده از Pygame پیاده‌سازی می‌کند.

### ویژگی‌ها:

- **`draw_grid()`**: رسم جدول سودوکو در پنجره‌ی Pygame
- **`handle_click(pos)`**: تعیین خانه‌ای که کاربر کلیک کرده است
- **`handle_key(key)`**: مدیریت فشار کلیدهای عددی یا حذف (Backspace/Delete) برای وارد کردن عدد در جدول
- **`display_win_message()`**: نمایش پیام "You Win!" در صورت تکمیل صحیح جدول
- **`run()`**: حلقه‌ی اصلی برنامه که رویدادهای ورودی را بررسی می‌کند و جدول را بروزرسانی می‌کند

## 🏁 اجرای بازی

در انتهای فایل:

```python
if __name__ == "__main__":
    game = SudokuGUI()
    game.run()
```

با اجرای این قسمت، بازی شروع می‌شود و یک پنجره‌ی سودوکو نمایش داده می‌شود.

## 🎯 نکات مهم

- فقط می‌توانید در خانه‌هایی که از ابتدا پر نشده‌اند عدد وارد کنید
- اگر جدول را به‌درستی کامل کنید، پیام "You Win!" نمایش داده می‌شود
- از کلیدهای 1 تا 9 برای وارد کردن عدد استفاده کنید
- از Backspace برای پاک کردن یک عدد استفاده کنید

## 🙌 نتیجه‌گیری

این پروژه یک مثال عالی برای یادگیری موارد زیر است:

- ساخت بازی با Pygame
- پیاده‌سازی الگوریتم حل سودوکو
- کار با رابط گرافیکی و رویدادهای کاربر در پایتون

