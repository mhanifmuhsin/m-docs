---
layout: post
title:  "Mengenal template literals sebagai fundamental Javascript bagi pengguna React"
date:   2021-04-08 06:38:38 +0700
category: reactjs
---

[Referensi](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals)

Dokumentasi ini mengenai Template literals yang mereferensi dari [MDN Web Docs](https://developer.mozilla.org/en-US/).

Template literals atau template string merupakan fitur pada Javascript (ES2015/ES6), ciri dari template literals yaitu menggunakan backtick (``), bukan tanda kutip ganda atau tunggal. Adapun beberapa fitur yang bisa kita gunakan adalah sebagai berikut :

1. Multi-line string

    Untuk memahaminya kita akan menggunakan contoh code dibawah ini

    - tanpa menggunakan template literals
    ```javascript
    console.log('string text line 1\n' +
    'string text line 2');
    // "string text line 1
    // string text line 2"
    ```
    - menggunakan template literals
    ```javascript
    console.log(`string text line 1
    string text line 2`);
    // "string text line 1
    // string text line 2"
    ```

    pengertian dari code diatas, dimana code yang pertama memerlukan tanda (\n dan +) untuk pindah ke baris baru, sedangkan pada code kedua hanya memerlukan enter, maka otomatis akan pindah ke baris baru

2. Expression interpolation

    Dengan template literals ini kita dapat mengembed ekspresi javascript dengan menggunakan tanda dollar dan kurung kurawal contohnya ${ekspresi javascript}, berikut contoh code sebagai pemahaman Expression interpolation :

    - tanpa template literals
    ```javascript
    let a = 5;
    let b = 10;
    console.log('Fifteen is ' + (a + b) + ' and\nnot ' + (2 * a + b) + '.');
    // "Fifteen is 15 and
    // not 20."
    ```
    - menggunakan template literals
    ```javascript
    let a = 5;
    let b = 10;
    console.log(`Fifteen is ${a + b} and
    not ${2 * a + b}.`);
    // "Fifteen is 15 and
    // not 20."
    ```
    - template literals sebagai String Concatenation
    ```javascript
    let name = 'Muhamad Hanif Muhsin';
    let age = 23;
    console.log(`${name} ${age} years old`);
    //Muhamad Hanif Muhsin 23 years old
    ```

    Melihat code diatas sudah tentu template literal lebih mudah untuk digunakan dan dibaca.

3. Nesting templates

    Pengguanaan ini biasanya pada kasus pengkondisian, untuk lebih jelasnya kita lihat kode dibawah ini :

    - tanpa menggunakan template literals dan nesting
    ```javascript
    let classes = 'header';
    classes += (isLargeScreen() ?
    '' : item.isCollapsed ?
        ' icon-expander' : ' icon-collapser');
    ```
    - menggunakan template literals tanpa nesting
    ```javascript
    const classes = `header ${ isLargeScreen() ? '' :
        (item.isCollapsed ? 'icon-expander' : 'icon-collapser') }`;
    ```

    - menggunakan template literals dan nesting
    ```javascript
    const classes = `header ${ isLargeScreen() ? '' :
        `icon-${item.isCollapsed ? 'expander' : 'collapser'}` }`;
    ```

    Kode terakhir mungkin pilihan kita semua, karena terlihat simpel dan mudah dibaca.

Sekian dokumentasi yang dapat saya catat, semoga bermanfaat . Terima kasih.




