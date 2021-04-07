---
layout: post
title:  "10 Pertanyaan interview React secara umum versi edureka"
date:   2021-04-07 09:28:38 +0700
category: reactjs
---

[Referensi](https://www.edureka.co/blog/interview-questions/react-interview-questions/#Difference-Real-Virtual)

Dokumentasi ini merupakan 10 Pertanyaan yang mungkin akan muncul ketika teman-teman melakukan interview, berikut 10 pertanyaan versi edureka :

1. **Apa perbedaan Real DOM dan Virtual DOM ?**

    |Real DOM|Virtual DOM|
    |Update Lambat|Update Lebih Cepat|
    |Bisa langsung update HTML|Tidak dapat memperbarui HTML secara langsung|
    |Membuat DOM baru jika elemen diperbarui|Memperbarui JSX jika elemen diperbarui|
    |Manipulasi DOM sangat susah|Manipulasi DOM sangat mudah|
    |Terlalu banyak pemborosan memori|Tidak ada pemborosan memori|

2. **Apa itu React ?**

    React merupakan Library JavaScript front-end yang dikembangkan oleh facebook pada tahun 2011 dan menjadi open soure pada tahun 2015, saat ini komunitas react merupakan salah satu komunitas terbesar.

    React dapat digunakan untuk pembuatan Web dengan skala kecil maupun besar, kompleks dan interaktif, komponen merupakan basis dari react untuk membangun UI sehingga dapat dengan mudah untuk digunakan kembali.

3. **Apa saja fitur yang dimiliki React ?**

    Fitur utama dari React yaitu :

    - Menggunakna virtual DOM, bukan asli

    - Menggunakan rendering sisi server

    - Mengikuti aliran satu arah (*uni-directional data flow*) atau *data binding*

4. **Sebutkan beberapa keuntungan utama dari React**

    - Meningkatkan kinerja aplikasi

    - Dapat dengan mudah digunakan di sisi *client* dan juga *server*

    - Karena JSX, keterbacaan kode meningkat

    - React mudah diintegrasikan dengan framework lain seperti Meteor, Angular , dll

    - Menggunakan React, menulis UI test case menjadi lebih mudah

5. **Apa batasan dari React ?**

    - React hanyalah *library*, bukan *framework*

    - Merupakan library yang besar sehingga membutuhkan waktu untuk memahaminya

    - Mungkin agak sulit untuk dipahami bagi pemogram pemula

    - Pengkodean menajdi kompleks karena menggunakan template *inline* dan *JSX*

6. **Apa itu JSX ?**

    JSX adalah singkatan dari **JavaScript XML**, ini merupakan jenis file yang digunakan oleh React yang memanfaatkan ekspresi JavaScript bersama dengan HTML seperti sintaks template. Dengan demikian file HTML sangant mudah untuk dipahami, berikut contoh file JSX pada React: 

    ```html
    render(){
        return(
            <div>
                <h1>Hello World from Edureka!!</h1>
            </div>
        );
    }
    ```

7. **Apa yang anda pahami tentang Virtual DOM ? Jelaskan cara kerjanya.**

    Virtual DOM adalah objek Javascript yang aslinya hanya salinan DOM asli. ini adalah node tree yang mencantumkan elemen, atribut dan isinya sebagai objek dan propertinya. Fungsi render React membuat node tree dari komponen React. kemudian memperbarui tree ini sebagai respon terhadap mutasi dalam model data yang disebabkan oleh berbagai tindakan yang dilakukan oleh pengguna atau oleh sistem. Virtual DOM ini bekerja dalam tiga langkah sederhana.

    1. Setiap kali ada data pokok yang berubah, seluruh UI dirender ulang dalam representasi Virtual DOM

        <img src="/assets/images/rc-q-1.png" alt="photo" width="400"/>

    2. Kemudian selisih antara representasi DOM sebelumnya dan yang baru dihitung

        <img src="/assets/images/rc-q-2.png" alt="photo" width="400"/>

    3. Setelah kalkulasi selesai, DOM asli akan diperbarui hanya dengan hal-hal yang benar-benar berubah.

        <img src="/assets/images/rc-q-3.png" alt="photo" width="300"/>

8. **Mengapa browser tidak bisa membaca JSX ?**

    Browser hanya dapat membaca objek JavaScript tetapi JSX bukan objek JavaScript biasa. Jadi untuk mengaktifkan browser untuk membaca JSX, pertama, kita perlu mengubah file JSX menjadi objek JavaScript menggunakan transformer JSX seperti Babel dan kemudian meneruskannya ke browser.

9. **Seberapa berbeda sintaks ES6 React jika dibandingkan dengan ES5 ?**

   - require vs import

     ```javascript
        //ES5
        var React = require('react');

        //ES6
        import React from 'react';
     ```

   - export vs exports

     ```javascript
        //ES5
        module.exports = Component;

        //ES6
        export default Component;
     ```

   - component vs function

     ```html
        //ES5
        var MyComponent = React.createClass({
            render: function(){
                return <h3>Hello Edureka!</h3>
            }
        });

        //ES6
        class MyComponent extends React.Component{
            render(){
                return <h3>Hello Edureka!</h3>
            }
        }
     ```

   - props

     ```html
        //ES5
        var App = React.createClass({
            propTypes: { name: React.PropTypes.string },
                render: function() {
                return <h3>Hello, {this.props.name}!</h3>
            }
        });

        //ES6
        class App extends React.Component {
            render() {
            return <h3>Hello, {this.props.name}!</h3>
            }
        }
     ```

   - state

     ```html
        //ES5
        var App = React.createClass({
            getInitialState: function() {
                return { name: 'world' };
            },
            render: function() {
                return <h3>Hello, {this.state.name}!</h3>
            }
        });

        //ES6
        class App extends React.Component {
            constructor() {
                super();
                this.state = { name: 'world' };
            }
            render() {
                return <h3>Hello, {this.state.name}!</h3>
            }
        }
     ```
     
10. **Apa perbedaan React dari Angular ?**

    |Topic|React|Angular|
    |ARCHITECTURE|Hanya Tampilan MVC|MVC lengkap|
    |RENDERING|Rendering sisi server|Perenderan sisi klien|
    |DOM|Menggunakan virtual DOM|Menggunakan DOM asli|
    |DATA BINDING|Pengikatan data satu arah|Pengikatan data dua arah|
    |DEBUGGING|Kompilasi waktu debugging|Proses debug waktu proses|
    |AUTHOR|Facebook|Google|

Sekian dokumentasi yang dapat saya catat, semoga bermanfaat . Terima kasih.




