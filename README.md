# olympeNitsu.github.io
<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>HouseQuest</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">

<style>
*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Poppins;
}

body{
background:#0B1020;
color:white;
overflow-x:hidden;
}

/* ===== BACKGROUND ===== */
.glow{
position:fixed;
width:600px;
height:600px;
background:radial-gradient(circle, rgba(139,92,246,0.35), transparent 70%);
filter:blur(90px);
z-index:-2;
animation:float 8s ease-in-out infinite;
}

.glow.two{
right:-150px;
bottom:-150px;
background:radial-gradient(circle, rgba(59,130,246,0.35), transparent 70%);
}

.glow.one{
left:-150px;
top:-150px;
}

@keyframes float{
0%,100%{transform:translateY(0);}
50%{transform:translateY(30px);}
}

/* ===== FLOATING COINS ===== */
.coin{
position:fixed;
font-size:20px;
opacity:0.2;
animation:fall 10s linear infinite;
}

@keyframes fall{
0%{transform:translateY(-100px) rotate(0);}
100%{transform:translateY(110vh) rotate(360deg);}
}

/* ===== NAV ===== */
nav{
display:flex;
justify-content:space-between;
align-items:center;
padding:20px 50px;
}

nav h1{
letter-spacing:3px;
}

nav a{
color:white;
margin-left:20px;
opacity:0.6;
text-decoration:none;
transition:0.3s;
}

nav a:hover{
opacity:1;
}

/* ===== HERO ===== */
.hero{
text-align:center;
padding:120px 20px;
}

.hero h2{
font-size:54px;
}

.hero p{
max-width:800px;
margin:15px auto;
opacity:0.75;
}

.btn{
padding:12px 22px;
margin:10px;
border:none;
border-radius:12px;
cursor:pointer;
font-weight:bold;
background:linear-gradient(90deg,#8B5CF6,#3B82F6);
color:white;
transition:0.3s;
}

.btn:hover{
transform:scale(1.05);
}

.btn:active{
transform:scale(0.95);
}

/* ===== SECTIONS ===== */
section{
padding:80px 20px;
max-width:1000px;
margin:auto;
}

h3{
font-size:26px;
margin-bottom:15px;
}

.card{
background:rgba(255,255,255,0.05);
border:1px solid rgba(255,255,255,0.1);
padding:20px;
border-radius:15px;
margin-top:15px;
backdrop-filter:blur(10px);
line-height:1.7;
transition:0.3s;
}

.card:hover{
transform:translateY(-5px);
}

/* ===== IMAGES ===== */
.mockup{
margin-top:15px;
height:220px;
border-radius:15px;
border:2px dashed rgba(255,255,255,0.3);
display:flex;
align-items:center;
justify-content:center;
opacity:0.7;
transition:0.3s;
}

.mockup:hover{
opacity:1;
transform:scale(1.02);
}

/* ===== QUESTY ===== */
#questyBtn{
position:fixed;
bottom:20px;
right:20px;
width:70px;
height:70px;
border-radius:50%;
background:#1c2140;
display:flex;
align-items:center;
justify-content:center;
cursor:pointer;
box-shadow:0 0 25px rgba(139,92,246,0.6);
animation:bounce 2s infinite;
}

#questyBtn img{
width:45px;
}

@keyframes bounce{
0%,100%{transform:translateY(0);}
50%{transform:translateY(-10px);}
}

/* ===== CHAT ===== */
#chat{
position:fixed;
bottom:100px;
right:20px;
width:300px;
height:380px;
background:rgba(0,0,0,0.75);
backdrop-filter:blur(10px);
border:1px solid rgba(255,255,255,0.1);
border-radius:15px;
display:none;
flex-direction:column;
overflow:hidden;
}

#chatHeader{
background:#8B5CF6;
padding:10px;
font-weight:bold;
}

#messages{
flex:1;
padding:10px;
font-size:13px;
overflow:auto;
}

#inputBox{
display:flex;
}

#inputBox input{
flex:1;
padding:8px;
border:none;
outline:none;
}

#inputBox button{
background:#3B82F6;
border:none;
color:white;
padding:8px;
cursor:pointer;
}

/* ===== MUSIC ===== */
#musicBtn{
position:fixed;
left:20px;
bottom:20px;
padding:10px 15px;
border-radius:10px;
background:rgba(255,255,255,0.1);
cursor:pointer;
}

</style>
</head>

<body>

<audio controls loop>
    <source src="musique.mp3" type="audio/mpeg">
</audio>

<div class="glow one"></div>
<div class="glow two"></div>

<!-- COINS DECOR -->
<div class="coin" style="left:10%;">🪙</div>
<div class="coin" style="left:30%; animation-delay:2s;">🪙</div>
<div class="coin" style="left:70%; animation-delay:4s;">🪙</div>

<!-- NAV -->
<nav>
<h1>HOUSEQUEST</h1>
<div>
<a href="#projet">Projet</a>
<a href="#probleme">Problème</a>
<a href="#solution">Solution</a>
<a href="#vision">Vision</a>
</div>
</nav>

<!-- HERO -->
<div class="hero">
<h2>Transforme ton ménage en aventure</h2>
<p>
HouseQuest est une application qui transforme les tâches du quotidien en missions interactives.
Grâce à la gamification, chaque action devient une progression, chaque effort devient une récompense.
</p>

<button class="btn" onclick="scrollToSection('projet')">Découvrir le projet</button>
<button class="btn" onclick="toggleMusic()">Activer ambiance 🎧</button>
</div>

<!-- PROJET -->
<section id="projet">
<h3>📌 Qu’est-ce que HouseQuest ?</h3>
<div class="card">
HouseQuest est une application mobile innovante qui transforme les tâches ménagères en expérience de jeu.
Chaque action du quotidien devient une mission : nettoyer, ranger, organiser.

L’utilisateur gagne des pièces, de l’expérience et progresse dans un système de niveaux.
Une mascotte intelligente, Questy (un chat bleu), accompagne l’utilisateur dans toute son aventure.
</div>
</section>

<!-- PROBLEME -->
<section id="probleme">
<h3>❌ Problématique</h3>
<div class="card">
Aujourd’hui, les tâches ménagères sont perçues comme répétitives, sans motivation et sans récompense.

Cela entraîne :
- procrastination
- manque d’intérêt
- accumulation des tâches

HouseQuest répond à ce problème en transformant ces actions en expérience motivante et interactive.
</div>
</section>

<!-- SOLUTION -->
<section id="solution">
<h3>💡 Solution</h3>
<div class="card">
HouseQuest transforme le quotidien en jeu :

✔ Missions
✔ XP et niveaux
✔ Pièces virtuelles
✔ Récompenses
✔ Assistant IA Questy
</div>

<div class="mockup">
🖼️ IMAGE 1 : Interface de l’application
</div>
</section>

<!-- VISION -->
<section id="vision">
<h3>🚀 Vision & Ambition</h3>
<div class="card">
HouseQuest vise à créer une nouvelle génération d’applications où la vie réelle devient interactive.

À long terme :
- réalité augmentée
- intelligence artificielle avancée
- récompenses réelles
- extension vers études et sport

Objectif : transformer le quotidien en progression constante.
</div>

<div class="mockup">
🖼️ IMAGE 2 : Concept futur / casque / UI
</div>

<div class="mockup">
🖼️ IMAGE 3 : Questy + progression utilisateur
</div>
</section>

<!-- CTA -->
<section>
<h3>🎯 Rejoindre HouseQuest</h3>
<div class="card">
HouseQuest n’est pas juste une application.
C’est une nouvelle manière de vivre le quotidien.

<button class="btn" onclick="alert('Projet en cours 🚀')">OK</button>
</div>
</section>

<!-- QUESTY BUTTON -->
<div id="questyBtn" onclick="toggleChat()">
<img src="https://cdn-icons-png.flaticon.com/512/616/616408.png">
</div>

<!-- CHAT -->
<div id="chat">
<div id="chatHeader">🐱 Questy</div>

<div id="messages">
Questy : Salut 👋 Je suis ton assistant HouseQuest !
</div>

<div id="inputBox">
<input id="userInput" placeholder="Pose une question...">
<button onclick="send()">OK</button>
</div>
</div>

<!-- MUSIC -->
<div id="musicBtn" onclick="toggleMusic()">🎧 Musique</div>

<audio id="audio" loop>
<source src="https://cdn.pixabay.com/audio/2022/03/15/audio_2b5c9b7f3d.mp3" type="audio/mp3">
</audio>

<script>

function scrollToSection(id){
document.getElementById(id).scrollIntoView({behavior:"smooth"});
}

function toggleChat(){
let chat = document.getElementById("chat");
chat.style.display = chat.style.display === "flex" ? "none" : "flex";
}

function send(){
let input = document.getElementById("userInput");
let msg = input.value;
if(!msg) return;

let box = document.getElementById("messages");

box.innerHTML += "<br><b>Toi :</b> " + msg;

let response = "";

if(msg.includes("mission")){
response = "Les missions te permettent de gagner des pièces 🪙 et de l'XP ⭐";
}
else if(msg.includes("pièce")){
response = "Les pièces servent à débloquer des récompenses 🎁";
}
else if(msg.includes("questy")){
response = "Je suis Questy 🐱 ton assistant HouseQuest !";
}
else{
response = "Hmm intéressant 🤔 continue ton aventure HouseQuest !";
}

box.innerHTML += "<br><b>Questy :</b> " + response;

input.value = "";
box.scrollTop = box.scrollHeight;
}

function toggleMusic(){
let audio = document.getElementById("audio");
if(audio.paused){
audio.play();
}else{
audio.pause();
}
}

</script>

</body>
</html>
