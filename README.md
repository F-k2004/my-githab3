# update_readme.py
import datetime
import random

quotes = [
    "✨ امروز بهترین روز برای شروعه!",
    "🚀 با هر قدم، به هدفت نزدیک‌تر می‌شی.",
    "🌱 هر چالش فرصتی برای رشد است.",
    "🔥 تو توانایی انجامش رو داری!"
]

now = datetime.datetime.now().strftime("%Y-%m-%d %H:%M:%S")
quote = random.choice(quotes)

content = f"""
# 👋 سلام!

این README به صورت خودکار توسط **GitHub Actions** به‌روز می‌شود.  

## 🕒 زمان آخرین به‌روزرسانی
`{now}`

## ✨ نقل‌قول الهام‌بخش امروز
> {quote}
"""

with open("README.md", "w", encoding="utf-8") as f:
    f.write(content)

print("✅ README.md با موفقیت به‌روز شد!")
