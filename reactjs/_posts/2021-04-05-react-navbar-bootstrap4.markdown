---
layout: post
title:  "Membuat Navbar menggunakan Bootstrap 4 dan React JS"
date:   2021-04-05 09:25:28 +0700
category: reactjs
---

[YouTube](https://youtu.be/e-DFne8Dhgk)

[Github Source](https://github.com/mhanifmuhsin/yt-navbar-react)

Dalam dokumentasi ini, kita akan belajar menggunakan Bootstrap 4 dengan React JS dengan cara membuat sebuah *Component* Navbar sederhana yang sudah ada di Bootstrap 4. Adapun tahapannya sebagai berikut :

1. **Membuat aplikasi react menggunakan CRA(*Create React App*)**

    Buka terminal dan jalankan perintah berikut :

    ```javascript
    npx create-react-app yt-navbar-react
    ```

2. **Kita coba jalankan terlebih dahulu aplikasi yang sudah dibuat**

    Masuk ke dalam folder aplikasi react dengan cara :

    ```javascript
    cd yt-navbar-react
    ```
    Setelah itu jalankan perintah dibawah ini untuk running server react
    ```javascript
    yarn start
    atau
    npm start
    ```

    Jika berhasil akan tampil seperti ini :

    <img src="/assets/images/rc-react-start.png" alt="photo" width="400"/>

3. **Install Bootstrap 4**
    
    Masuk ke terminal lagi, dan pastikan ada di folder *yt-navbar-react*, kemudian jalankan perintah berikut :

    ```javascript
    npm install bootstrap
    atau
    yarn add bootstrap
    ```

    ```javascript
    npm install --save jquery popper.js
    atau
    yarn add jquery popper.js
    ```

4. **Import Bootstrap ke index.js atau app.js**

    ```javascript
    import 'bootstrap/dist/css/bootstrap.min.css';
    ```

    <img src="/assets/images/rc-imp-b4.png" alt="photo" width="400"/>

5. **Install react-router-dom**

    ```base
    npm install --save react-router-dom
    atau
    yarn add react-router-dom
    ```

6. **Buat Component dengan nama Navbar.js didalam folder src, dan copy kan script berikut :**

    ```html
    import React from 'react';
    import { Link } from "react-router-dom";

    const Navbar = () => {
        return (
            <div>
                <nav className="navbar navbar-expand-lg navbar-dark bg-dark">
                    <Link className="navbar-brand" href="#">Navbar</Link>
                    <button className="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                        <span className="navbar-toggler-icon"></span>
                    </button>

                    <div className="collapse navbar-collapse" id="navbarSupportedContent">
                        <ul className="navbar-nav mr-auto">
                            <li className="nav-item active">
                                <Link className="nav-link" href="#">Home <span className="sr-only">(current)</span></Link>
                            </li>
                            <li className="nav-item">
                                <Link className="nav-link" href="#">Link</Link>
                            </li>
                            <li className="nav-item dropdown">
                                <Link className="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                                    Dropdown
                                </Link>
                                <div className="dropdown-menu" aria-labelledby="navbarDropdown">
                                    <Link className="dropdown-item" href="#">Action</Link>
                                    <Link className="dropdown-item" href="#">Another action</Link>
                                    <div className="dropdown-divider"></div>
                                    <Link className="dropdown-item" href="#">Something else here</Link>
                                </div>
                            </li>
                            <li className="nav-item">
                                <Link className="nav-link disabled" href="#" tabindex="-1" aria-disabled="true">Disabled</Link>
                            </li>
                        </ul>
                        <form className="form-inline my-2 my-lg-0">
                            <input className="form-control mr-sm-2" type="search" placeholder="Search" aria-label="Search" />
                            <button className="btn btn-outline-success my-2 my-sm-0" type="submit">Search</button>
                        </form>
                    </div>
                </nav>
            </div>
        )
    }

    export default Navbar
    ```

7. **Tambahkan script berikut di index.js :**

    ```javascript
    import { BrowserRouter } from "react-router-dom";
    ```

    ```html
    <BrowserRouter>
    </BrowserRouter>
    ```
    <img src="/assets/images/rc-imp-b4-1.png" alt="photo" width="400"/>

8. **Update file *App.js***

    ```javascript
    import './App.css';
    import Navbar from './Navbar';

    function App() {
    return (
        <Navbar />
    );
    }

    export default App;
    ```

9. **Jalankan ulang**

    ```javascript
    npm start
    atau 
    yarn start
    ```
    <img src="/assets/images/rc-imp-b4-2.png" alt="photo" width="400"/>

Sekian dokumentasi yang dapat saya catat, semoga bermanfaat . Terima kasih.




