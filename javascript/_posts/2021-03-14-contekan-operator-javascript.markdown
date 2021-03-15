---
layout: post
title:  "Contekan Operator Javascript"
date:   2021-03-15 20:57:25 +0700
category: javascript
---
Dokumentasi ini bersumber dari : [dev.to](https://dev.to/palashmon/ultimate-cheatsheet-compilation-32c9#chapter-3) Palash Mondal

```javascript
5 == 5     // true
5 == '5'   // true
5 === 5    // true
5 === '5'  // fasle
```

```javascript
5 != 5     // fasle
5 != '5'   // fasle
5 !== 5    // fasle
5 !== '5'  // true
```

```javascript
2 + 2  // 4
4 - 2  // 2
2 * 3  // 6
4 / 2  // 2
```

```javascript
let a = 10; log(++a ,a); // 11  11
let b = 10; log(b++ ,b); // 10  11
let c = 10; log(--c ,c); // 9  9
let d = 10; log(d-- ,d); // 10  9
```

```javascript
let a = 20; a += 5; // a = 25
let b = 20; b -= 5; // b = 15
let c = 20; c *= 5; // c = 100
let d = 20; d /= 5; // d = 4
let e = 20; e %= 5; // e = 0
```

```javascript
(5 === 5) ? 'a' : 'b' // a

3 > 2 && 1 < 2 // true
3 > 2 || 5 < 2 // true
!true          // false
```

```javascript
3 > 3   // false
3 < 3   // false
3 >= 3  // true
3 <= 3  // true
5 % 3   // 1
```
