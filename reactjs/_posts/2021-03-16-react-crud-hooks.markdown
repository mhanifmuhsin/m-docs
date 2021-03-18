---
layout: post
title:  "Membuat Aplikasi CRUD menggunakan React JS tanpa Database"
date:   2021-03-16 15:49:28 +0700
category: reactjs
---

Dokumentasi ini bersumber dari : [dev.to](https://dev.to/sanderdebr/creating-a-crud-app-in-react-with-hooks-3jml) Sanderdebr

Aplikasi sederhana ini dibangun menggunakan :

1. CRA (create-react-app)

2. [Skeleton CSS boilerplate](http://getskeleton.com)

[Source code](https://github.com/mhanifmuhsin/react-crud-hook)

## Step 1

1. Install react mengunakan CRA
    ```javascript
    npx create-react-app react-crud-hooks
    ```
2. Masuk ke foder react-crud-hooks
    ```javascript
    cd react-crud-hooks
    ```
3. Jalankan App, untuk mengetahui apakah kita berhasil atau tidak
    ```javascript
    npm start
    ```
    atau
    ```javascript
    yarn start
    ```

## Step 2 

1. Masuk ke folder src (cara menggunakan terminal)
    ```javascript
    cd src
    ```
2. Buat 4 file : **AddUserForm.js**, **EditUserForm.js**, **UserTable.js**, **data.js** (cara menggunakan terminal)
    ```javascript
    touch AddUserForm.js EditUserForm.js UserTable.js data.js
    ```

    Keterangan :

    **AddUserForm.js** Component yang digunakan untuk meng-input user

    **EditUserForm.js** Component yang digunakan untuk meng-edit user

    **UserTable.js** Component yang digunakan sebagai menmapilkan data user

    **data.js** File yang digunakan untuk membuat data dummy

    *Penggunaan terminal optional , bisa menggunakan GUI juga*

## Step 3

