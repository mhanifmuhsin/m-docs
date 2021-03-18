---
layout: post
title:  "Contekan String Javascript"
date:   2021-03-16 07:20:25 +0700
category: javascript
---
Dokumentasi ini bersumber dari : [dev.to](https://dev.to/palashmon/ultimate-cheatsheet-compilation-32c9#chapter-3) Palash Mondal

```javascript
String declaration

const name = "Proful";
const city = 'Jeypore';
const msg = `${name} is from ${city}`;
```

```javascript
String functions

msg.indexOf(city); // 15
msg.lastIndexOf(name); // 0
city.chartAt(2); // 'y'
city[3]; // 'y'
city.replace("J","P");
city.toUpperCase();
name.toLowerCase();
name.concat("is good");
name.slice(3,6); // 'ful'
city.split("y"); // ['Je','pore']
name.length; // 6
```
