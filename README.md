# Quick Git Training

#### Create repository in the project

```bash
git init
```

#### View the current settings list

```bash
git config --list
```

#### Configuring the name

```bash
git config --global user.name "your name"
```

#### Viewing  the current status of the repository

```bash
git status
```

#### Adding file to stage

```bash
git add filename
```

#### Adding all of  file to stage

```bash
git add .
```

#### Adding all files with changes to file name or deleting file or moved

```bash
git add -A
```

#### committing

```bash
git commit -m "your comment"
```

#### Adding all files and commits them at a time

```bash
git commit -am "your comment"
```

#### Moving or renaming a file or folder

```bash
git mv path/filename.ext newpath/newfilename.ext
```

#### Copying file

```bash
git cp path/filename.ext newpath/filename.ext
```

#### Deleting File

```bash
git rm path/filename.ext
```

#### Copying file from stage in the project directory

> در مواقعی مورد استفاده قرار میگیره که تغییراتی در فایل پروژه دادین اما متوجه میشین دیگه این تغییرات رو نمیخواین داشته باشین و فایل داخل stage مد نظرتونه

```bash
git checkout -- filename.ext
```

#### Copy latest files from the last commit into `stage` and `working directory`.

```bash
git checkout HEAD -- filename.ext
```

# gitignore

at first create a `.gitignore` file.

#### پترن هایی که مورد استفاده قرار میگیرند

- /**/ :  دسترسی به تمامی مسیرهای زیرشاخه
- * :  با تعداد تکرار صفر تا بینهایت از هر کاراکتر تطبیق میکند
- ? : با یک کاراکتر تطبیق میکند
- [] : کلاس کاراکتری
---

# Repository
####  Configuring repository url

```bash
git remote add origin http:\\address.domain\to\repname\...
```

#### sending file to repository

```bash
git push origin master
```

#### getting the latest file changes from the server
```bash
git pull origin master
```

#### git clone (Copying repository from the server on local )

```bash
git clone https://your-repository-address.git
```


#### Changing a remote's URL
 ```bash
git remote set-url origin https://your-repository-address.git
 ```
---

