<!DOCTYPE html>

<html>
<head>
<meta charset="UTF-8">
<title>Happy Birthday Providencia</title>

<link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Poppins:wght@300;500&display=swap" rel="stylesheet">

<style>

body{
margin:0;
height:100vh;
display:flex;
justify-content:center;
align-items:center;
background:linear-gradient(135deg,#ffd6e0,#ffeaf2,#ffd1dc);
overflow:hidden;
font-family:'Poppins',sans-serif;
}

/* CARD */

.card{
width:520px;
height:420px;
background:#ffc7d1;
border-radius:30px;
display:flex;
flex-direction:column;
align-items:center;
justify-content:center;
box-shadow:0 20px 60px rgba(0,0,0,0.2);
position:relative;
z-index:2;
}

/* TITLE */

.title{
font-family:'Pacifico',cursive;
font-size:42px;
color:#c2185b;
margin-top:25px;
opacity:0;
animation:textShow 2s 4s forwards;
text-align:center;
}

@keyframes textShow{
from{opacity:0; transform:translateY(30px);}
to{opacity:1; transform:translateY(0);}
}

/* CAKE */

.cake{
position:relative;
width:160px;
height:140px;
display:flex;
justify-content:center;
align-items:flex-end;
}

.plate{
width:180px;
height:14px;
background:white;
border-radius:10px;
position:absolute;
bottom:0;
}

/* CAKE LAYERS */

.layer{
position:absolute;
width:160px;
height:34px;
background:#8d6e63;
border-radius:10px;
opacity:0;
}

.layer1{
bottom:14px;
animation:layer 0.8s 0.5s forwards;
}

.layer2{
bottom:48px;
animation:layer 0.8s 1.2s forwards;
}

.layer3{
bottom:82px;
animation:layer 0.8s 1.9s forwards;
}

@keyframes layer{
from{
transform:translateY(40px);
opacity:0;
}
to{
transform:translateY(0);
opacity:1;
}
}

/* CREAM */

.cream{
position:absolute;
width:160px;
height:22px;
background:white;
border-radius:12px;
top:18px;
opacity:0;
animation:creamDrop 1s 2.6s forwards;
}

@keyframes creamDrop{
from{
transform:translateY(-20px);
opacity:0;
}
to{
transform:translateY(0);
opacity:1;
}
}

/* CANDLE (MUNCUL TERAKHIR) */

.candle{
width:12px;
height:35px;
background:#ff8fa3;
position:absolute;
top:-15px;
border-radius:3px;
opacity:0;
animation:candleShow 1s 3.4s forwards;
}

@keyframes candleShow{
from{
opacity:0;
transform:translateY(-20px);
}
to{
opacity:1;
transform:translateY(0);
}
}

.flame{
width:10px;
height:15px;
background:orange;
border-radius:50%;
position:absolute;
top:-15px;
left:1px;
animation:flicker 1s infinite alternate;
}

@keyframes flicker{
from{transform:scale(1);}
to{transform:scale(1.2);}
}

/* HEARTS */

.heart{
position:absolute;
width:14px;
height:14px;
background:#ff6b81;
transform:rotate(45deg);
animation:fall linear infinite;
}

.heart:before,
.heart:after{
content:"";
position:absolute;
width:14px;
height:14px;
background:#ff6b81;
border-radius:50%;
}

.heart:before{top:-7px;}
.heart:after{left:-7px;}

@keyframes fall{
0%{transform:translateY(-100vh) rotate(45deg);}
100%{transform:translateY(100vh) rotate(45deg);}
}

/* BALLOON */

.balloon{
position:absolute;
width:40px;
height:50px;
background:#ff8fa3;
border-radius:50%;
animation:float 6s infinite ease-in-out;
}

.balloon:after{
content:"";
position:absolute;
width:2px;
height:40px;
background:#999;
left:19px;
top:50px;
}

@keyframes float{
0%{transform:translateY(0);}
50%{transform:translateY(-20px);}
100%{transform:translateY(0);}
}

/* SPARKLES */

.sparkle{
position:absolute;
width:6px;
height:6px;
background:white;
border-radius:50%;
animation:twinkle 2s infinite;
}

@keyframes twinkle{
0%{opacity:0;}
50%{opacity:1;}
100%{opacity:0;}
}

</style>

</head>

<body>

<div class="card">

<div class="cake">

<div class="plate"></div>

<div class="layer layer1"></div>
<div class="layer layer2"></div>
<div class="layer layer3"></div>

<div class="cream"></div>

<div class="candle">
<div class="flame"></div>
</div>

</div>

<div class="title">Happy Birthday Providencia</div>

</div>

<script>

/* hearts */

for(let i=0;i<35;i++){
let h=document.createElement("div");
h.className="heart";
h.style.left=Math.random()*100+"vw";
h.style.animationDuration=(Math.random()*3+3)+"s";
document.body.appendChild(h);
}

/* balloons kiri */

for(let i=0;i<5;i++){
let b=document.createElement("div");
b.className="balloon";
b.style.left=(3 + i*6)+"vw";
b.style.top=(20 + Math.random()*50)+"vh";
document.body.appendChild(b);
}

/* balloons kanan */

for(let i=0;i<5;i++){
let b=document.createElement("div");
b.className="balloon";
b.style.left=(97 - i*6)+"vw";
b.style.top=(20 + Math.random()*50)+"vh";
document.body.appendChild(b);
}

/* sparkles */

for(let i=0;i<40;i++){
let s=document.createElement("div");
s.className="sparkle";
s.style.left=Math.random()*100+"vw";
s.style.top=Math.random()*100+"vh";
document.body.appendChild(s);
}

</script>

</body>
</html>

