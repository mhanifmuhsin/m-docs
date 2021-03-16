---
layout: post
title:  "Contekan Kode Status HTTP"
date:   2021-03-16 09:40:28 +0700
category: other
---

Dokumentasi ini bersumber dari : [dev.to](https://dev.to/palashmon/ultimate-cheatsheet-compilation-32c9#chapter-3) Palash Mondal

|<span style="color:salmon">1xx</span>|<span style="color:salmon">Informational</span>|
|100 - Continue| Menunjukkan sejauh ini semuanya baik-baik saja |
|102 - Processing| Server sedang memproses permintaan tetapi tidak ada respons yang tersedia |
|<span style="color:green">2xx</span>|<span style="color:green">Success</span>|
|200 - Ok|Permintaan berhasil|
|201 - Created|Biasanya tanggapan dikirim setelah permintaan posting|
|<span style="color:orange">3xx</span>|<span style="color:orange">Redirection</span>|
|301 - Moved Permanently|URL sumber daya yang diminta telah diubah secara permanen. URL baru diberikan sebagai tanggapan|
|304 - Not Modified|Respons belum diubah, versi cache dapat digunakan|
|<span style="color:DeepPink">4xx</span>|<span style="color:DeepPink">Client Error</span>|
|400 - Bad Request|Server tidak dapat memahami permintaan karena sintaks yang tidak valid|
|401 - Unauthorized|Pengguna tidak diautentikasi|
|400 - Forbidden|Klien diautentikasi tetapi tidak memiliki akses|
|400 - Not Found|Server tidak dapat menemukan sumber daya yang diminta|
|<span style="color:red">5xx</span>|<span style="color:red">Server Error</span>|
|500 - Internal Server Error|Server mengalami situasi yang tidak diketahui bagaimana menanganinya|
|502 - Bad Gateway|Gateway server mendapat respons tidak valid|
|500 - Gateway Timeout|Gateway server tidak bisa mendapat tanggapan tepat waktu|

