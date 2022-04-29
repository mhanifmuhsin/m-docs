---
layout: post
title:  "Mengenal Singkat Tentang TypeScript"
date:   2022-04-29 09:11:11 +0700
category: typescript
---
Dalam post pertama mengenai TypeScript ini kita akan sedikit perkenalan atau mengenali apa itu TypeScript dan kenapa kita perlu mempelajari TypeScript.

Seperti yang kita ketahui Javascript merupakan salah satu bahasa yang populer dan mempunyai perkembangan yang sangat pesat, hal itu dibukitkan dengan Javascript bisa menjadi pilihan untuk aplikasi frontend dan backend dari berbagai ukuran. 

Namun ada beberapa dilema yang sering terjadi ketika aplikasi yang kita bangun mulai besar ukurannya, tentunya dalam _development_ ataupun _production_ kita tidak ingin terjadi sesuatu yang membuat kita pusing, dan ini sering disebut dengan **_bugs_** oleh para _programmer_.

Seperti yang kita ketahui bahwasanya Javascript merupakan bahasa yang tidak menggukan tipe dalam penulisan sebuah variable nya, misalkan :
```
  let bilanganPertama = 10;
  console.log(bilanganPertama) // output 10
```

Kodingan diatas memang tidak salah dan akan berjalan dengan baik, namun mari kita coba mengetikan kodingan seperti ini :

```
if (bilanganPertama === "10")console.log("sama")
// output undifined
```

Dari output kodingan diatas mengembalikan  **undifined**, mungkin jika kodingan kita 1 baris seperti diatas, kita tidak akan terlalu pusing dan mungkin akan ketahuan bahwa **bilanganPertama** itu number bukan sebuah string makanya akan mengembalikan **undifined**, nah bagaimana jika kodingan kita sudah semakin komplek dan merupakan hasil lemparan dari sebuat parameter ? , tentu ini akan menjadi hal yang sepele namun mempunyai _effort_ yang besar untuk mengetahui apa masalahnya dan dimana masalahnya karena aplikasi masih bisa berjalan atau di _running_.

Disinalah TypeScript datang dan dicipatakan dengan tujuan untuk menjadi pemeriksa tipe statis program JavaScript - dengan kata lain, alat yang berjalan sebelum kode Anda berjalan dan memastikan bahwa jenis program sudah benar.

Untuk membuktikannya mari kita coba _refactor code_ di atas kedalam TypeScript menggunakan Playgroud TypeScript :
```
let bilanganPertama : number = 5
if(bilanganPertama === "5") console.log("sama")

muncul notif pemberitahuan kesalahan :
let bilanganPertama: number
This condition will always return 'false' since the types 'number' and 'string' have no overlap.
```

Sesuai dengan tujuannya, TypeScript mengecek bahwa kodingan tersebut bermasalah, dan TypeScript pun memberikan penjelasan apa penyebabnya, dengan demikian kita akan lebih aman dalam membuat program dan tentunya akan meminimalisir hal-hal  yang tidak kita inginkan di kemudian hari setelah aplikasi yang kita buat sudah berada di _production_.

Dengan demikian kita dapat simpulkan alasan kita mengenal dan mempelajari TypeScript, yaitu 
untuk membuat kita semakin percaya diri dengan kodingan yang kita buat dan membantu orang lain untuk mudah memahami kodingan dan me-maintenance aplikasi kita. Namun hal ini pun bukan berarti kita harus menggunakan TypeScript dalam membuat sebuah aplikasi, ini hanya pilihan agar aplikasi berjalan lebih baik.

Sekian pengenalan singkat mengenai TypeScript, semoga bermanfaat.