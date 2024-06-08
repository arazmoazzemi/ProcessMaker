مراحل نصب و پیکربندی تقویم فارسی Datepicker در ProcessMaker
روش اول
آدرس آموزش 
https://support.faragostar.net/Knowledgebase/Article/View/33--datepicker-tarykh-shmsy


1. ایجاد پوشه CustomJavaScript
ابتدا در مسیر زیر یک پوشه به نام CustomJavaScript ایجاد نمایید:
vbnet
Copy code
C:\Bitnami\processmaker-3.2.1-0\apps\processmaker\htdocs\workflow\public_html\lib\CustomJavaScript
2. کپی فایل‌های مورد نیاز
فولدر jquery.ui_.datepicker1.8.14-cc را به مسیر ایجاد شده کپی نمایید.
3. افزودن کنترل Textbox
کنترل Textbox را از قسمت Web Control بر روی صفحه قرار دهید و نام متغیر را وارد کنید.
4. اضافه کردن آدرس‌ها به external libs
آدرس‌های زیر را در قسمت external libs وارد نمایید. این آدرس‌ها در فایل external links.txt نیز موجود هستند:
plaintext
Copy code
/lib/CustomJavaScript/jquery.ui_.datepicker1.8.14-cc/styles/jquery.ui.datepicker1.8-all.css
/lib/CustomJavaScript/jquery.ui_.datepicker1.8.14-cc/scripts/jquery.ui.datepicker-cc.all.min.js
5. افزودن کد جاوا اسکریپت
کد زیر را در بخش جاوا اسکریپت فرم وارد کنید:
javascript
Copy code
$("input[name*='textVar001']").datepicker();
یا از کد زیر استفاده کنید:
javascript
Copy code
$('#textVar001').getControl().datepicker({
    Placement: 'bottom',
    Trigger: 'focus',
    EnableTimePicker: false,
    TargetSelector: '',
    GroupId: '',
    ToDate: false,
    FromDate: false,
});


روش دوم
6. استفاده از Datepicker فارسی
می‌توانید از Datepicker فارسی استفاده کنید.
استفاده از MdBootstrapPersianDateTimePicker
https://www.codeproject.com/Articles/858123/Bootstrap-Persian-DateTimePicker
لینک ویدئو آموزشی
مشاهده ویدئو آموزشی
افزودن فایل‌های مورد نیاز
آدرس‌های زیر را به external libs اضافه کنید:
plaintext
Copy code
/lib/MD.BootstrapPersianDateTimePicker-1.6.4/Content/MdBootstrapPersianDateTimePicker/jquery.Bootstrap-PersianDateTimePicker.css
/lib/MD.BootstrapPersianDateTimePicker-1.6.4/Scripts/MdBootstrapPersianDateTimePicker/calendar.js
/lib/MD.BootstrapPersianDateTimePicker-1.6.4/Scripts/MdBootstrapPersianDateTimePicker/jquery.Bootstrap-PersianDateTimePicker.js
افزودن کد جاوا اسکریپت برای استفاده از MdPersianDateTimePicker
کد زیر را در بخش جاوا اسکریپت فرم وارد کنید:
javascript
Copy code
$("input[name*='textVar001']").MdPersianDateTimePicker();
یا از کد زیر استفاده کنید:
javascript
Copy code
$('#textVar001').getControl().MdPersianDateTimePicker({
    Placement: 'bottom',
    Trigger: 'focus',
    EnableTimePicker: false,
    TargetSelector: '',
    GroupId: '',
    ToDate: false,
    FromDate: false,
});
نکات اضافی
•	مطمئن شوید که تمامی فایل‌های CSS و JS به درستی بارگذاری شده‌اند.
•	در صورت بروز هرگونه خطا، کنسول مرورگر خود را بررسی کنید تا خطاهای احتمالی را پیدا و رفع کنید.
•	برای سفارشی‌سازی بیشتر، مستندات مربوط به هر پلاگین را مطالعه نمایید.
این قالب به شما کمک می‌کند تا کدهای خود را به صورت منظم و خوانا در گیت‌هاب قرار دهید و از بروز مشکلات احتمالی جلوگیری کنید.

