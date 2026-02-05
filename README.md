<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>For Sufiyan ❤️</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
body{
    margin:0;
    height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    background:linear-gradient(135deg,#ffb6c1,#ffd1dc);
    font-family:'Segoe UI',sans-serif;
    overflow:hidden;
}

.card{
    background:white;
    padding:30px 22px;
    border-radius:28px;
    width:90%;
    max-width:380px;
    text-align:center;
    box-shadow:0 30px 60px rgba(0,0,0,0.25);
    animation:fadeIn 0.8s ease;
}

@keyframes fadeIn{
    from{opacity:0;transform:scale(0.75)}
    to{opacity:1;transform:scale(1)}
}

h1{
    color:#ff3f6c;
}

p{
    font-size:17px;
    color:#444;
    line-height:1.6;
}

button{
    padding:12px 26px;
    font-size:16px;
    border:none;
    border-radius:30px;
    cursor:pointer;
    margin:8px;
}

.yes{
    background:#ff3f6c;
    color:white;
}

.no{
    background:#eee;
    position:absolute;
}

.continue{
    background:#ff85a1;
    color:white;
}

.glow{
    animation:glow 1.5s infinite alternate;
}

@keyframes glow{
    from{text-shadow:0 0 6px #ff3f6c}
    to{text-shadow:0 0 25px #ff3f6c}
}

.hearts, .loveFX{
    position:fixed;
    inset:0;
    pointer-events:none;
}

.float{
    position:absolute;
    font-size:26px;
    animation:floatUp 4s linear infinite;
}

@keyframes floatUp{
    from{transform:translateY(100vh) scale(0.8);opacity:1}
    to{transform:translateY(-10vh) scale(1.3);opacity:0}
}
</style>
</head>

<body>

<audio id="bgm" autoplay loop>
<source src="https://cdn.pixabay.com/audio/2023/03/13/audio_6c59c6c84f.mp3">
</audio>

<div class="card" id="card">
    <h1 class="glow">💘 Sufiyan 💘</h1>
    <p>
        Will you be my Valentine?<br><br>
        Not just for today,<br>
        but for all the little tomorrows ❤️
    </p>
    <p>🌹🌹🌹</p>

    <button class="yes" onclick="stepTwo()">Yes 💖</button>
    <button class="no" onmouseover="moveNo()">No 🙈</button>
</div>

<div class="hearts" id="hearts"></div>
<div class="loveFX" id="loveFX"></div>

<script>
const music=document.getElementById("bgm");
document.body.addEventListener("click",()=>music.play());

function moveNo(){
    const btn=document.querySelector(".no");
    btn.style.left=Math.random()*80+"vw";
    btn.style.top=Math.random()*80+"vh";
}

/* STEP 2 */
function stepTwo(){
    document.getElementById("card").innerHTML=`
    <h1 class="glow">Sufiyan ❤️</h1>
    <p>
       Somewhere between your long nights of studying and quiet exhaustion,<br>
my heart chose you with patience and certainty.<br><br>

As you learn to heal lives with steady hands and courage,<br>
I dream of building a life where we heal each other too.<br><br>

Your journey toward becoming a doctor inspires me,<br>
because it shows me the kind of strength I want beside me forever.<br><br>

When the world calls you in white coats and responsibilities,<br>
I hope to be the home you return to, always waiting with love.<br><br>

Not just a love for today,<br>
but a future, a partnership, a lifetime — with you. ❤️

    </p>
    <button class="yes" onclick="stepThree()">Yes 💕</button>
    <button class="no" onmouseover="moveNo()">No 😳</button>
    `;
}

/* STEP 3 */
function stepThree(){
    document.getElementById("card").innerHTML=`
    <h1 class="glow">Just One More Step 💌</h1>
    <p>
        My heart has one last thing to say…
    </p>
    <button class="continue" onclick="finalStep()">Continue ➜</button>
    `;
}

/* FINAL STEP */
function finalStep(){
    document.getElementById("card").innerHTML=`
    <h1 class="glow">I Love You ❤️</h1>
    <p>
        🌙 Shayari 🌙<br><br>
        Tumhari ek muskurahat se hi,<br>
        mera din roshan ho jaata hai.<br>
        Tumhara saath mil jaaye agar,<br>
        toh har dard bhi pyaar ban jaata hai.
        <br><br>
        Happy Valentine’s Day, Sufiyan 💖<br>
        <b>— From Shahima ❤️</b>
    </p>
    `;
    startHearts();
    startLoveFX();
}

function startHearts(){
    const c=document.getElementById("hearts");
    setInterval(()=>{
        const h=document.createElement("div");
        h.className="float";
        h.innerHTML=["❤️","💖","💘","🌹"][Math.floor(Math.random()*4)];
        h.style.left=Math.random()*100+"vw";
        h.style.fontSize=Math.random()*22+18+"px";
        c.appendChild(h);
        setTimeout(()=>h.remove(),4000);
    },160);
}

function startLoveFX(){
    const fx=document.getElementById("loveFX");
    setInterval(()=>{
        const e=document.createElement("div");
        e.className="float";
        e.innerHTML=["💋","🤗","💞"][Math.floor(Math.random()*3)];
        e.style.left=Math.random()*100+"vw";
        e.style.fontSize=Math.random()*24+22+"px";
        fx.appendChild(e);
        setTimeout(()=>e.remove(),4000);
    },220);
}
</script>

</body>
</html>
