---
layout: post
title:  "Contekan DOM Javascript"
date:   2021-03-19 17:47:00 +0700
category: javascript
---
Dokumentasi ini bersumber dari : [dev.to](https://dev.to/palashmon/ultimate-cheatsheet-compilation-32c9#chapter-3) Palash Mondal

```javascript
//elemen tunggal yang ditentukan oleh id
const app = document.getElementById('app')
//beberapa elemen(array) ditentukan oleh nama kelas
const hero = document.getElementByClassName('hero')
//beberapa elemen berdasarkan tag html
const h1 = document.getElementByTagName('h1')
//elemen pertama berdasarkan pemilih/selector
const hero = document.querySelector('.hero')
//beberapa elemen berdasarkan pemilih/selector
const heroes = document.querySelectorAll('.hero')
```

```javascript
//buat elemen html dari tag
let para = document.createElement('p')
//buat text node
let text = document.createTextNode('I love it')

<p>I love it</p>


//tambahkan txt node ke elemen para
para.appendChild(text)
//masukkan h2 sebelum h1
app.inserBefore(h2,h1)
```

```javascript
h1.insertAdjacentHTML('beforebegin','<span>cool</span>')

// beforebegin  => tempatkan sebelum h1 sebagai sibling
// afterbegin   => tempatkan di dalam h1 sebaga first child
// beforeend    => tempatkan di dalam h1 sebaga last child
// afterend     => tempatkan setelah h1 sebagai sibling
```

```javascript
app.classList.remove('dark') //hapus class
app.classList.add('light') //tambah class
app.classList.toggle('visible') //toggle class
app.classList.contsains('app') // benar jika app ada
app.childNodes //mengambil semua node anak
app.parentNode //mengembalikan parent node
```

```html
<div id="app" class="hero dark">
    <h1>sketchnotes by Proful</h1>
</div>
```
