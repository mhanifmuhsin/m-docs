---
layout: post
title:  "Contekan Array Javascript"
date:   2021-03-18 07:15:25 +0700
category: javascript
---
Dokumentasi ini bersumber dari : [dev.to](https://dev.to/palashmon/ultimate-cheatsheet-compilation-32c9#chapter-3) Palash Mondal

```javascript
['a','b'].concat(['c']) //['a',b','c']
['a','b'].join('~') //'a~b'
['a','b','c'].slice(1) //['b','c']
['a','b','c'].indexOf('b') //1
['a','b','c'].lastIndexOf('b) //2
```

```javascript
['a','b','c'].forEach(x => console.log (x))

[1,2,3].every(x => x < 10) //true
[1,2,3].some(x => x < 2) // true
[1,2,3].filter(x => x < 2) //[1]
```

```javascript
[1,2,3].map(x => x * 2) //[2,3,6]
[1,2,3].reduce((x,y) => x * y) //6
[2,15,3].sort() // [2,3,15]
[1,2,3].reverse() //[3,2,1]
[1,2,3].length //3
```

```javascript
const arr = [1,2,3]
const x=arr.shift() //arr=[2,3],x=1
const x=arr.unshift(9) //arr=[9,1,2,3],x=4
const x=arr.pop() //arr=[1,2],x=3
const x=arr.push(5) //arr=[1,2,3,5],x=4
```

```javascript
const arr=['a','b','c','d'];
const mod = arr.splice(1,2,'z'); //arr=['a','z','d'],mod=['b','c']
```
