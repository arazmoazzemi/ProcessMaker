# قوانین طراحی فرآیند در پراسس میکر

## آریو پروژه گستر

### دستورالعمل نصب پراسس میکر

### دستورالعمل نصب سیستم فراگستر

## اطلاعات اضافی

### نیازمندی‌ها جهت توسعه فرآیند در نسخه 3.2.1 پراسس میکر
- آشنایی به چرخه فرآیند طراحی فرم و BPMS
- آشنایی به دیتابیس‌های SQL و MySQL
- آشنایی به PHP، JavaScript، CSS، HTML

### توضیحات اضافی
مدل پیاده‌سازی از نسخه 4 پراسس میکر تغییر و بهبود یافته است.

## ایجاد تقویم کاری و شیفت کاری

## ایجاد گروه‌های فرآیند

## ایجاد چارت سازمانی

## ایجاد کاربران
نکته: این قسمت در فراگستر طراحی و ایجاد می‌گردد و اطلاعات پس از همگام‌سازی دیتابیس در پراسس میکر قابل استفاده خواهد بود.

---

# تنظبمات مستقیم در پراسس میکر

## مراحل نصب و پیکربندی تقویم فارسی Datepicker در ProcessMaker

### روش اول
آدرس آموزش: [پشتیبانی فراگستر](https://support.faragostar.net/Knowledgebase/Article/View/33--datepicker-tarykh-shmsy)

1. **ایجاد پوشه CustomJavaScript**  
ابتدا در مسیر زیر یک پوشه به نام CustomJavaScript ایجاد نمایید:
   ```vbnet
   C:\Bitnami\processmaker-3.2.1-0\apps\processmaker\htdocs\workflow\public_html\lib\CustomJavaScript
```

کپی فایل‌های مورد نیاز
فولدر jquery.ui_.datepicker1.8.14-cc را به مسیر ایجاد شده کپی نمایید.

افزودن کنترل Textbox
کنترل Textbox را از قسمت Web Control بر روی صفحه قرار دهید و نام متغیر را وارد کنید.

اضافه کردن آدرس‌ها به external libs
آدرس‌های زیر را در قسمت external libs وارد نمایید. این آدرس‌ها در فایل external links.txt نیز موجود هستند:
```
/lib/CustomJavaScript/jquery.ui_.datepicker1.8.14-cc/styles/jquery.ui.datepicker1.8-all.css
/lib/CustomJavaScript/jquery.ui_.datepicker1.8.14-cc/scripts/jquery.ui.datepicker-cc.all.min.js
```


افزودن کد جاوا اسکریپت
کد زیر را در بخش جاوا اسکریپت فرم وارد کنید:

```
$("input[name*='textVar001']").datepicker();
```
یا از کد زیر استفاده کنید:
```
$('#textVar001').getControl().datepicker({
    Placement: 'bottom',
    Trigger: 'focus',
    EnableTimePicker: false,
    TargetSelector: '',
    GroupId: '',
    ToDate: false,
    FromDate: false,
});
```

روش دوم
استفاده از Datepicker فارسی
می‌توانید از Datepicker فارسی استفاده کنید.
استفاده از MdBootstrapPersianDateTimePicker
آدرس آموزش: CodeProject

لینک ویدئو آموزشی: مشاهده ویدئو آموزشی

افزودن فایل‌های مورد نیاز
آدرس‌های زیر را به external libs اضافه کنید:
```
/lib/MD.BootstrapPersianDateTimePicker-1.6.4/Content/MdBootstrapPersianDateTimePicker/jquery.Bootstrap-PersianDateTimePicker.css
/lib/MD.BootstrapPersianDateTimePicker-1.6.4/Scripts/MdBootstrapPersianDateTimePicker/calendar.js
/lib/MD.BootstrapPersianDateTimePicker-1.6.4/Scripts/MdBootstrapPersianDateTimePicker/jquery.Bootstrap-PersianDateTimePicker.js
```

افزودن کد جاوا اسکریپت برای استفاده از MdPersianDateTimePicker
کد زیر را در بخش جاوا اسکریپت فرم وارد کنید:

```
$("input[name*='textVar001']").MdPersianDateTimePicker();
```

یا از کد زیر استفاده کنید:
```
$('#textVar001').getControl().MdPersianDateTimePicker({
    Placement: 'bottom',
    Trigger: 'focus',
    EnableTimePicker: false,
    TargetSelector: '',
    GroupId: '',
    ToDate: false,
    FromDate: false,
});
```

نکات اضافی
مطمئن شوید که تمامی فایل‌های CSS و JS به درستی بارگذاری شده‌اند.
در صورت بروز هرگونه خطا، کنسول مرورگر خود را بررسی کنید تا خطاهای احتمالی را پیدا و رفع کنید.
برای سفارشی‌سازی بیشتر، مستندات مربوط به هر پلاگین را مطالعه نمایید.
این قالب به شما کمک می‌کند تا کدهای خود را به صورت منظم و خوانا در گیت‌هاب قرار دهید و از بروز مشکلات احتمالی جلوگیری کنید.
----

قراردادهای نام‌گذاری در طراحی هر فرم
هر فرم در زیر فرم ساخته شده در گروه‌های فرآیند ساخته می‌شود و این فرم باید عضو یکی از گروه‌های فرآیند باشد.

هر فرم بر اساس کد مدرک ایجاد شده توسط فرم ایزو ساخته می‌شود و درصورت تغییر کد مدرک، فرم جدید با ساختار جدید ایجاد می‌گردد و اطلاعات فرم قدیم در فرآیند غیر فعال می‌گردد.




































