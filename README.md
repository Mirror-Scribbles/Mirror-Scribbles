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



