- 👋 Hi, I’m @Mirror-Scribbles
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
Mirror-Scribbles/Mirror-Scribbles is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
css como crear un nav bar ------


@import url('https://fonts.googleapis.com/css2?family=Patua+One&display=swap');

*{
    box-sizing: border-box;
    margin: 0;
    padding: 0;
    font-family: sans-serif;
}

body{
    
    /* background-color: black; */
    background: url( software-developer-6521720_1280.jpg);
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    min-height: 100vh;
    width: 100%;
    font-family: 'Patua One', cursive;
}


.nav{
    height: 100px;
    color: aliceblue;
    background: transparent;
    border-radius: 10px;
    box-shadow: 0 0 30px rgba(2, 50, 73, 0.3);
    backdrop-filter: blur(8px);
    box-shadow: 0 0 30px  rgba(2, 23, 68, 0.5);
    width: 100%;
    padding: 40px;
    border: 1px solid rgba(2, 23, 68, 0.5);

}
.nav__container{
    display:flex;
    height: 100%;
    width: 100%;
    margin: 0 auto;
    justify-content: space-between;
    align-items: center;
    
}
.button__logo{
    font-size: 30px;
    font-weight: 600;
    background-color: transparent;
    border: none;
    color: #ff3c78;
    cursor: pointer;
    transition: 0.5s;
}
.button__logo:hover{
    color: #265a08;
    border: yellowgreen transparent;
}

.nav__menu{
display: grid;
grid-auto-flow: column;
gap: 3em;
}
.nav__item{
    position: relative;
    color: aliceblue;
    text-decoration: none;
    font-size: 16px;
    letter-spacing: 0.8px;
    padding: 0 10px;
    transition: 0.5s;
    cursor: pointer;
}
.nav__item::after{
    content: "";
    position: absolute;
    background-color: #ff3c78;
    height: 2px;
    width: 0;
    left: 0;
    bottom: -10px;
    transition: 0.3s;
}
.nav__item:hover{
color: #43a30c;
}
.nav__item:hover::after{
width: 100%;
}

.nav__input:checked + .nav__menu{

}

.nav__lable, .nav__input{
    display: none;
}

@media (max-width : 700px) {

    .nav__lable{
        display: block;
        cursor: pointer;
    }
    .nav__menu{
        transition: 0.5s;
        display: none;
    }

    .nav__input:checked + .nav__menu{
        display: block;
        position: fixed;
        top: 100px;
        bottom: 0;
        width: 100%;
        height: 500px;
        left: 0;
        display: flex;
        justify-content: space-evenly;
        flex-direction: column;
        align-items: center;
        padding-top: 20px;
        
    }

    
    
};



HTML ---------


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
   <link rel="stylesheet" href="style.css">
</head>
<body>
   <nav class="nav">
    <div class="nav__container">
        <h1 class="nav__logo"><button class= "button__logo">Mirror</button></h1>
        <label for="menu" class="nav__lable">
            <img src="menu.svg" alt="">
        </label>
        <input type="checkbox" id="menu" class="nav__input">
        <div class="nav__menu">
            <a href="#" class="nav__item">Home</a>
            <a href="#" class="nav__item">Sign up</a>
            <a href="#" class="nav__item">About me</a>
            <a href="#" class="nav__item">Contact</a>
        </div>
    </div>
   </nav> 
</body>
</html> 


















log in basico  --- numero 2 



HTML ------- 

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="log.css">
    <title>Sign up</title>
</head>
<body>
    
    <header>
<h2 class="logo">Logo</h2>
<nav class="navegation">
    <a href="#">Home</a>
    <a href="#">About</a>
    <a href="#">Services</a>
    <a href="#">Contact</a>
    <button class="btnLoging-popup">Login</button>
</nav>
    </header>
    
<div class="container">
    <span class="icone-close"><box-icon name='x-circle' animation='tada' color='#9bc8eb' ></box-icon></span>

    <div class="form-box  login">
        <h2>Login</h2>
        <form action="#">
            <div class="input-box">
                <span class="icon"><box-icon name='envelope' animation='burst' color='#9bc8eb' ></box-icon></span>
                <input type="email" required>
                <label>Email</label>
            </div>
            <div class="input-box">
                <span class="icon"><box-icon name='lock' type='solid' animation='burst' color='#9bc8eb' ></box-icon></span>
                <input type="password" required>
                <label>Password</label>
            </div>
            <div class="remeber-forgot">
                <label><input type="checkbox">Remeber me</label>
                <a href="#">Forgot password?</a>
            </div>
            <button type="submit" class="btn">Login</button>
            <div class="login-register">
                <p>Don't have an account yet? <a href="signup.html" class="register-link"> Register</a> </p>
            </div>
        </form>
    </div>

    
</div>


<script src="https://unpkg.com/boxicons@2.1.4/dist/boxicons.js"></script>
<script src="log.css"></script>
</body>
</html>





HTML 2 ------------------------ 


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="log.css">
    <title>Document</title>
</head>
<body>

    <div class="container">
    
        <div class="form-box  login">
            <h2>Register</h2>
            <form action="#">

                <div class="input-box">
                    <span class="icon"><box-icon name='user-circle' color='#9bc8eb' type='solid' animation='burst' ></box-icon></span>
                    <input type="text" required>
                    <label>Username</label>
                </div>
                <div class="input-box">
                    <span class="icon"><box-icon name='envelope' animation='burst' color='#9bc8eb' ></box-icon></span>
                    <input type="email" required>
                    <label>Email</label>
                </div>
                <div class="input-box">
                    <span class="icon"><box-icon name='lock' type='solid' animation='burst' color='#9bc8eb' ></box-icon></span>
                    <input type="password" required>
                    <label>Password</label>
                    <div class="input-box">
                        <span class="icon"><box-icon name='lock' type='solid' animation='burst' color='#9bc8eb' ></box-icon></span>
                        <input type="password" required>
                        <label>Confirm password</label>
                    </div>
                </div>
                <div class="remeber-forgot">
                    <label><input type="checkbox">Agree to terms and conditions.</label>
                </div>
                <button type="submit" class="btn">Login</button>
                <div class="login-register">
                    <p>Already have an account? <a href="loging.html" class="register-link"> Login</a> </p>
                </div>
            </form>
        </div>
    
        
    </div>
    
</body>
</html>





CSS---------------

*{
    box-sizing: border-box;
    margin: 0;
    padding: 0;
    font-family: Arial, Helvetica, sans-serif;
}

body{
    background: url(cyberpunk.jpg);
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    min-height: 100vh;
    width: 100%;
}
.container{
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
}
p{
    display: flex;
    justify-content: center;
}

.form-box{
border: 2px solid rgba(255,255,2550.5);
position: relative;
width: 400px;
height: 550px;
border-radius: 20px;
backdrop-filter: blur(5px);
display: flex;
justify-content: center;
align-items: center;
}

.form-box h2{
    color: #fff;
    text-align: center;
    font-size: 32px;
}

.form-box .input-box{
position: relative;
margin: 30px;
width: 310px;
border-bottom: 1px solid #eff;
}


.form-box .input-box input{
width: 100%;
height: 45px;
background: transparent;
border: none;
outline: none;
padding: 0 20px 0 5px;
color: #fff;
font-size: 14px;
}

i{
    position: absolute;
    color:rgb(255, 255, 255);
    top: 13px;
    right: 0;
}

input::placeholder{
    color: #fff;
}

.btn{
    color: #fff;
    background: rgb(196, 32, 32);
    width: 100%;
    height: 50px;
    border-radius: 6px;
    outline: none;
    border: none;
    font-size: 17px;
    cursor: pointer;
    box-shadow: 3px 0 10px rgb(116, 38, 38);
}

.group{
display: flex;
justify-content: space-between;
}

.group span a {
    color: #eff;
    position: relative;
    top: 10px;
    position: relative;
    text-decoration: none;
    font-weight: 500;
}

.group a:focus{
    text-decoration: underline;
}

#result{
color: rgb(255, 6, 6);
font-weight: 600;
position: relative;
top: 25px;
}





.popup{
    width: 400px; 
    background-color: rgb(255, 255, 255);
    border-radius: 6px;
     position: absolute;
    top: 0;
    left: 50%;
     transform: translate(-50, 50%) scale(0);
     transition: transform .4s , top .4s;
     visibility: hidden;
    text-align: center;
    padding: 0 30px 30px;
    height: 330px;
    color: rgb(11, 155, 83);
    border: 1px green solid;
    border: solid 1px rgb(190, 189, 189);
    
}

.popup ion-icon {
  color: hsl(120, 100%, 50%);  
  font-size: 45px;
}

.popup button{
    width: 100%;
background-color: #d11818a9;
padding: 10px 0;
margin-top: 50px;
border: none;
outline: none;
font-size: 18px;
color: #fff;
border-radius: 4px;
cursor: pointer;
box-shadow: 0 0 2px rgba(0,0,0.1)
}

.popup a{
    color: #fff;
    text-decoration: none;
    font-weight: 600;
    letter-spacing: 2px;
}

.open-slide{
top: 50%;
transform: translate(-50%, -50%) scale(1);
visibility: visible;
}


