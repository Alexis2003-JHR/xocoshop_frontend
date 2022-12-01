<template>
    <div class="nav">
        <div class="logo">
            <a href=""><img src="../assets/NavBar_Icons/Logo-Black.png" alt=""></a>
        </div>
        <div class="main-menu">
            <ul>
                <li><a href="#" class="Active">INICIO</a></li>
                <li><a href="#">PRODUCTOS</a></li>
                <li><a href="#">CONTACTO</a></li>
            </ul>
        </div>
        <div class="icons-nav">
            <a href=""><img src="../assets/NavBar_Icons/Shop.png" alt=""></a>
            <a href=""><img src="../assets/NavBar_Icons/User.png" alt=""></a>
        </div>
    </div>
</template>
<style scoped>
.nav{
    display: flex;
    position: absolute;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    height: 90px;
    height: 100px;
    z-index: 1;
}
.main-menu{
    display: flex;
    justify-content: space-around;
    text-align: center;
}
.main-menu li, a{
    text-decoration: none;
    display: inline-block;
    list-style: none;
    padding: 5px 5px;
    margin: 0 5px;
    color: #000000;
    font-size: 15px;
    font-weight: bold;
}
.main-menu a:hover{
    color: #B7625B;
    transition: .8s;
}
.Active{
    color: #B7625B;
    border-bottom: 2px solid #B7625B;
}
.logo, .icons-nav{
    margin: 10px 30px;
}
.icons-nav img{
    margin: 0 5px;
    width: 30px;
}
</style>