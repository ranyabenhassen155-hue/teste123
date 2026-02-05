<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>For Ranim ❤️</title>

<style>
body{
    text-align:center;
    font-family:Arial;
    background:#ffe6f0;
    padding-top:80px;
    overflow:hidden;
}

h1{
    font-size:35px;
}

button{
    padding:12px 25px;
    font-size:18px;
    margin:10px;
    cursor:pointer;
    border:none;
    border-radius:8px;
}

.yes{
    background:#ff4d88;
    color:white;
}

.no{
    background:white;
}

/* hearts */
.heart{
    position:fixed;
    color:red;
    font-size:25px;
    animation: float 4s linear infinite;
}

@keyframes float{
    0%{ transform:translateY(0); opacity:1;}
    100%{ transform:translateY(-800px); opacity:0;}
}
</style>
</head>

<body>

<h1>Ranim, will you be my Valentine? ❤️</h1>

<button class="yes" onclick="yesClick()">YES</button>
<button class="no" id="noBtn">NO</button>

<script>

function yesClick(){

    document.body.innerHTML += `
    <h1>YAYYYY 💖</h1>
    <p>I love you Ranim ❤️</p>
    <img src="https://media.giphy.com/media/MDJ9IbxxvDUQM/giphy.gif" width="280">
    `;

    setInterval(createHeart, 300);
}

function createHeart(){
    let heart = document.createElement("div");
    heart.className = "heart";
    heart.innerHTML = "❤️";

    heart.style.left = Math.random()*100 + "vw";
    heart.style.bottom = "0px";

    document.body.appendChild(heart);

    setTimeout(()=> heart.remove(),4000);
}

let noBtn = document.getElementById("noBtn");

noBtn.addEventListener("mouseover", function(){
    let x = Math.random() * (window.innerWidth - 100);
    let y = Math.random() * (window.innerHeight - 50);

    noBtn.style.position = "absolute";
    noBtn.style.left = x + "px";
    noBtn.style.top = y + "px";
});

</script>

</body>
</html>
