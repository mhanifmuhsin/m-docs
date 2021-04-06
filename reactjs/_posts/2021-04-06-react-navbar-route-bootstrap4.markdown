---
layout: post
title:  "Membuat route pada Navbar dengan react-router-dom"
date:   2021-04-06 07:02:38 +0700
category: reactjs
---

[Github Source](https://github.com/mhanifmuhsin/yt-navbar-react/tree/react-router)

Dokumentasi ini merupakan kelanjutan dari post dengan judul [**Membuat Navbar menggunakan Bootstrap 4 dan React JS**](http://mhanifmuhsin.com/reactjs/2021/04/05/react-navbar-bootstrap4.html), lebih baik teman-teman baca dulu dan pelajari, karena saya akan menggunakan source codenya kembali.

Baiklah kali ini kita akan mencoba membuat route sederhana menggunakan *react-router-dom* , Adapun tahapannya sebagai berikut : 

1. **Buka source code yt-navbar-react**

2. **Modifikasi Navbar**

    Ubah code :

    ```html
    <li className="nav-item">
        <Link className="nav-link" href="#">Link</Link>
    </li>
    ```

    menjadi :

     ```html
    <li className="nav-item">
        <Link className="nav-link" href="#">Profile</Link>
    </li>
    ```
    
    Ubah code :

    ```html
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
    ```

    menjadi :

    ```html
    <li className="nav-item dropdown">
        <Link className="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
            Students
       </Link>
        <div className="dropdown-menu" aria-labelledby="navbarDropdown">
                <Link className="dropdown-item" href="#">Junior High School</Link>
                <Link className="dropdown-item" href="#">Senior High School</Link>
                <div className="dropdown-divider"></div>
                <Link className="dropdown-item" href="#">Elementary School</Link>
        </div>
    </li>
    ```

3. **Tambahkan script berikut pada index.js untuk menambahkan javascript pada bootstrap :**
    
    ```javascript
    import 'bootstrap';
    ```

4. **Jalankan aplikasi, dan hasilnya akan seperti ini :**

    <img src="/assets/images/rc-route.png" alt="photo" width="400"/>


5. **Buat 3 component pada folder src, dengan nama file Home.js, Profile.js dan JuniorStudent.js**

    <img src="/assets/images/rc-route-1.png" alt="photo" width="100"/>

6. **Ketikan script dibawah ini di dalam file Home.js**

    ```html
    import React from 'react';

     const Home = ()=>{
         return <h1>Profile</h1>
     }

    export default Home
    ```

7. **Ketikan script dibawah ini di dalam file Profile.js**

    ```html
    import React from 'react';

     const Profile = ()=>{
         return <h1>Profile</h1>
     }

    export default Profile
    ```

8. **Ketikan script dibawah ini di dalam file JuniorStudent.js**

    ```html
    import React from 'react';

     const JuniorStudent = ()=>{
         return <h1>Profile</h1>
     }

    export default JuniorStudent
    ```

8. **Buat file route.js di folder src, dan ketikan script berikut :**

    ```javascript
    import React from 'react';
    const JuniorStudent = React.lazy(() => import('./JuniorStudent'))
    const Profile = React.lazy(() => import('./Profile'))
    const Home = React.lazy(() => import('./Home'))

    const routes = [
    
        { path: '/students/juniorStudent', Component: JuniorStudent },
        { path: '/profile', Component: Profile },
        { path: '/', Component: Home },
    ]
    export default routes
    ```

9. **Buka file Navbar.js, dan update code seperti ini :**

    Import routes yang telah kita buat, kemudian update import react-router-dom dengan menambahkan Switch dan Route
    ```javascript
    import routes from './routes'
    import { Link, Switch, Route } from "react-router-dom";
    ```

    Tambahkan script berikut sesudah tag nav > div 
    ```javascript
    <Switch>
        {routes.map((route, i) => {
            const {
                    path,
                    omponent
                  } = route
            return <Route key={i} path={path}>
                    <Component />
                    </Route>
                    })}
    </Switch>
    ```

    Kemudian tambahkan juga script berikut di level paling atasnya, sehingga menjadi pembungkus dari return :

    ```javascript
    <React.Suspense fallback={<div>Loading...</div>}>
     //code lainnya
    </React.Suspense>
    ```
    
    Berikut code lengkapnya :

    ```html
    import React from 'react';
    import routes from './routes'
    import { Link, Switch, Route } from "react-router-dom";

    const Navbar = () => {
        return (
            <React.Suspense fallback={<div>Loading...</div>}>
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
                                <Link className="nav-link" href="#">Profile</Link>
                            </li>
                            <li className="nav-item dropdown">
                                <Link className="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                                    Students
                                </Link>
                                <div className="dropdown-menu" aria-labelledby="navbarDropdown">
                                    <Link className="dropdown-item" href="#">Junior High School</Link>
                                    <Link className="dropdown-item" href="#">Senior High School</Link>
                                    <div className="dropdown-divider"></div>
                                    <Link className="dropdown-item" href="#">Elementary School</Link>
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
                <div>
                    <Switch>
                        {routes.map((route, i) => {
                            const {
                                path,
                                Component
                            } = route
                            return <Route key={i} path={path}>
                                <Component />
                            </Route>
                        })}
                    </Switch>
                </div>
            </div>
            </React.Suspense>
        )
    }

    export default Navbar
    ```

10. **Update kembali code Navbar**

    Ubah code :

    ```html
    <Link className="nav-link" href="#">Home <span className="sr-only">(current)</span></Link>
    ```

    menjadi :

    ```html
    <Link to="/" className="nav-link" >Home <span className="sr-only">(current)</span></Link>
    ```
    
    Ubah code :

    ```html
    <Link className="nav-link" href="#">Profile</Link>
    ```

    menjadi :

    ```html
    <Link to="/profile"className="nav-link">Profile</Link>
    ```
    
    Ubah code :

    ```html
    <Link className="dropdown-item" href="#">Junior High School</Link>
    ```

    menjadi :

    ```html
    <Link to="/students/JuniorStudent" className="dropdown-item">Junior High School</Link>
    ```

11. **Silahkan jalankan kembali aplikasinya, dan seharusnya route sudah berjalan ketika kita klik menu Home, Profile dan Junior High School, berikut hasilnya :**

    <img src="/assets/images/rc-route-2.png" alt="photo" width="400"/>

    <img src="/assets/images/rc-route-3.png" alt="photo" width="400"/>

    <img src="/assets/images/rc-route-4.png" alt="photo" width="400"/>



Sekian dokumentasi yang dapat saya catat, semoga bermanfaat . Terima kasih.




