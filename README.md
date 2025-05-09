# Sodacan360-

#html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="./style.css">
    <title>Document</title>
</head>
<body>

    <div class="banner">
        <div class="product">
            <div class="soda"
            style="--url:url(./bg\ 1.png)">
            </div>
            <div class="soda"
            style="--url:url(./bg\ 2.png)">
            </div>
        </div>

        <div class="rock">
            <img src="./rock1.png" alt="">
            <img src="./rock2.png" alt="">
            <img src="./rock3.png" alt="">
        </div>
    </div>
    
</body>
</html>

#css
body{
    background-color: grey;
   background-image: url(./bg.jpg);
   position: relative;
}
.banner{
    height: 100vh;
    overflow: hidden;
    position: relative;
}
.banner .product{
     /* background-color: red; */
     position: absolute;
     width: 500px;
     height: 500px;
     bottom: 170px;
     left: 50%;
     transform: translateX(-50%);
     z-index: 1;
     transition: 0.7s;
     --left: 0px;
     display: flex;
}
.banner .product .soda{
    background: 
    var(--url) var(--left),0,
    url(./freepik__background__10441.png);
    background-size: auto 100%;
    width: 400px;
    aspect-ratio: 2/3;
    background-blend-mode: multiply;
    mask-image: url(./freepik__background__10441.png);
    mask-size: auto 100%;
    transition: 0.7s;
    position: absolute;
    left: 50%;
    transform: translateX(-50%);
}
.banner .product:hover{
    --left: 1000px;
    transform: translateX(-50%) translateY(-120px);
}
.banner .rock{
    position: absolute;
    inset: 0 0 0 0;
    pointer-events: none;
}
.banner .rock img{
position: absolute;
transition: 0.7s;
}
.banner .rock img:nth-child(1){
    height: 170px;
    left: 54%;
    transform: translateX(-50%);
    bottom: -30px;
}
.banner:has(.product:hover) .rock img:nth-child(1){
    transform: translateX(-50%)translateY(50px);
}
.banner .rock img:nth-child(2){
height: 50%;
left: 0%;
bottom: 0;
}
.banner:has(.product:hover) .rock img:nth-child(2){
    transform: translateX(-50%)translateY(100px);
}
.banner .rock img:nth-child(3){
    height: 100%;
    right: 0;
    bottom: -100px;
    rotate: -25deg;
}
.banner:has(.product:hover) .rock img:nth-child(3){
    transform: translateX(100px) translateY(100px);
}
.banner .product .soda:nth-child(2){
    opacity: 0;
}
.banner .product:hover .soda:nth-child(2){
    opacity: 1;
}
