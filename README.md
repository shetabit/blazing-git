# آموزش سریع گیت

#### ایجاد رپازیتوری در پروژه

```bash
git init
```

#### دیدن لیست تنظیمات کنونی

```bash
git config --list
```

#### تنظیم کردن نام

```bash
git config --global user.name "your name"
```

#### مشاهده وضعیت کنونی رپازیتوری

```bash
git status
```

#### افزودن فایل به stage

```bash
git add filename
```

#### افزودن همه ی فایل ها به stage

```bash
git add .
```

#### افزودن همه ی فایل ها به همراه تغییرات در نام فایل و یا حذف شدن فایل یا جابه جا شدن

```bash
git add -A
```

#### کامیت کردن

```bash
git commit -m "your comment"
```

#### افزودن همه فایل ها و کامیت کردن انها به صورت همزمان

```bash
git commit -am "your comment"
```

#### جابه جا کردن یا تغییر نام فایل یا فولدر

```bash
git mv path/filename.ext newpath/newfilename.ext
```

#### کپی فایل

```bash
git cp path/filename.ext newpath/filename.ext
```

#### حذف فایل

```bash
git rm path/filename.ext
```

#### کپی کردن فایل از stage در دایرکتوری پروژه

> در مواقعی مورد استفاده قرار میگیره که تغییراتی در فایل پروژه دادین اما متوجه میشین دیگه این تغییرات رو نمیخواین داشته باشین و فایل داخل stage مد نظرتونه

```bash
git checkout -- filename.ext
```

#### کپی کردن فایل از head (اخرین کامیت) در stage و پوشه پروژه

```bash
git checkout HEAD -- filename.ext
```

#### تنظیم کردن ادرس رپازیتوری سرور

```bash
git remote add origin http:\\address.domain\to\repname\...
```

#### ارسال فایل به رپازیتوری بر روی سرور

```bash
git push origin master
```

#### دریافت اخرین تغییرات و فایل ها از سرور

```bash
git pull origin master
```

#### کلون کردن کل پروژه (کپی رپازیتوری از سرور روی کامپیوتر)

```bash
git clone https://your-repository-address.git
```

---

# gitignore

ابتدا یک فایل با پسوند gitignore ایجاد میکنیم