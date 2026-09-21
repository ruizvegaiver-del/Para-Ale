<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>Para Ale 🌻</title>

<style>
body{
margin:0;
display:flex;
justify-content:center;
align-items:center;
height:100vh;
background:linear-gradient(#ffd54f,#ffecb3);
overflow:hidden;
font-family:Arial,sans-serif;
}

.flower{
position:fixed;
top:-40px;
font-size:28px;
animation:fall linear infinite;
}

@keyframes fall{
to{
transform:translateY(110vh) rotate(360deg);
}
}

.envelope{
position:relative;
width:300px;
height:200px;
cursor:pointer;
}

.back{
position:absolute;
width:100%;
height:100%;
background:#f6c445;
border-radius:8px;
}

.front{
position:absolute;
bottom:0;
width:100%;
height:100px;
background:#dca72b;
clip-path:polygon(0 0,100% 0,50% 100%);
z-index:3;
}

.flap{
position:absolute;
width:100%;
height:100px;
background:#ffd54f;
clip-path:polygon(0 100%,50% 0,100% 100%);
transform-origin:top;
transition:1s;
z-index:4;
}

.letter{
position:absolute;
left:15px;
top:20px;
width:270px;
height:320px;
background:#fff;
border-radius:12px;
padding:18px;
box-sizing:border-box;
overflow:auto;
transform:translateY(80px);
transition:1s;
z-index:2;
}

.open .flap{
transform:rotateX(180deg);
}

.open .front{
opacity:0;
}

.open .letter{
transform:translateY(-220px);
z-index:10;
}

h2{
text-align:center;
color:#d4a000;
}

p{
color:#333;
line-height:1.6;
}
</style>

</head>
<body>

<div class="envelope" id="sobre">

<div class="back"></div>

<div class="letter">

<h2>🌻 Para Ale 🌻</h2>

<p>
Estas flores amarillas son para recordarte lo especial que eres.
</p>

<p>
Gracias por cada sonrisa, cada momento y por ser una persona tan increíble.
</p>

<p>
<b>Gracias por tu amistad, pendeja. 💛</b>
</p>

<p>
Espero que esta pequeña sorpresa te saque una sonrisa.
</p>

<p>
😂🚿 <b>Y ya pues... ¡anda báñate!</b>
</p>

<p style="text-align:center;">
❤️ Con mucho cariño ❤️
</p>

</div>

<div class="front"></div>
<div class="flap"></div>

</div>

<script>

document.getElementById("sobre").onclick=function(){
this.classList.toggle("open");
}

for(let i=0;i<40;i++){
let f=document.createElement("div");
f.className="flower";
f.innerHTML="🌻";
f.style.left=Math.random()*100+"vw";
f.style.animationDuration=(5+Math.random()*5)+"s";
f.style.animationDelay=Math.random()*5+"s";
document.body.appendChild(f);
}

</script>

</body>
</html>
