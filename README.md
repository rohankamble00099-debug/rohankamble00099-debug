<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1.0">
<meta name="description" content="Free online calculators and useful tools for everyone.">
<title>ToolNest USA - Free Online Tools</title>

<style>
*{box-sizing:border-box;margin:0;padding:0}
body{
font-family:Arial,sans-serif;
background:#f5f7fb;
color:#172033;
line-height:1.5
}
header{
background:#111827;
color:white;
padding:16px 6%;
display:flex;
justify-content:space-between;
align-items:center;
position:sticky;
top:0;
z-index:10
}
.logo{font-size:24px;font-weight:800}
.logo span{color:#60a5fa}
nav a{
color:white;
text-decoration:none;
margin-left:18px;
font-size:14px
}
.hero{
background:linear-gradient(135deg,#111827,#1d4ed8);
color:white;
padding:65px 6%;
text-align:center
}
.hero h1{font-size:42px;margin-bottom:12px}
.hero p{
max-width:650px;
margin:auto;
color:#dbeafe
}
.search{
max-width:600px;
margin:25px auto 0;
display:flex
}
.search input{
flex:1;
padding:15px;
border:0;
border-radius:10px 0 0 10px;
font-size:16px;
outline:none
}
.search button{
padding:15px 22px;
border:0;
background:#60a5fa;
color:#111827;
font-weight:bold;
border-radius:0 10px 10px 0
}
.container{
max-width:1100px;
margin:auto;
padding:45px 20px
}
.title{text-align:center;margin-bottom:30px}
.title h2{font-size:30px}
.grid{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(240px,1fr));
gap:20px
}
.card{
background:white;
border:1px solid #e5e7eb;
border-radius:18px;
padding:25px;
box-shadow:0 5px 20px rgba(0,0,0,.05)
}
.icon{font-size:35px;margin-bottom:10px}
.card h3{margin-bottom:8px}
.card p{color:#667085;font-size:14px}
.tool{
margin-top:15px
}
input,textarea,select{
width:100%;
padding:12px;
border:1px solid #d1d5db;
border-radius:8px;
margin:6px 0;
font-size:15px
}
button.action{
background:#2563eb;
color:white;
border:0;
padding:11px 16px;
border-radius:8px;
cursor:pointer;
margin-top:5px
}
.result{
margin-top:12px;
padding:12px;
background:#eff6ff;
border-radius:8px;
font-weight:bold
}
.adbox{
margin:35px 0;
padding:25px;
background:#fff;
border:1px dashed #cbd5e1;
border-radius:12px;
text-align:center;
color:#64748b
}
.info{
background:#111827;
color:white;
border-radius:18px;
padding:30px;
margin-top:30px
}
.info p{color:#d1d5db;margin-top:8px}
footer{
background:#0b1120;
color:#9ca3af;
text-align:center;
padding:30px
}
.hidden{display:none}

@media(max-width:600px){
.hero h1{font-size:32px}
nav{display:none}
.search{flex-direction:column}
.search input,.search button{border-radius:8px;margin:4px 0}
}
</style>
</head>

<body>

<header>
<div class="logo">Tool<span>Nest</span> 🇺🇸</div>

<nav>
<a href="#tools">Tools</a>
<a href="#about">About</a>
</nav>
</header>

<section class="hero">

<h1>Free Online Tools</h1>

<p>
Simple, fast and free tools for calculations, text,
conversions and everyday online tasks.
</p>

<div class="search">
<input id="search" placeholder="Search a tool..."
onkeyup="searchTools()">
<button onclick="searchTools()">Search</button>
</div>

</section>

<main class="container">

<div class="title">
<h2 id="tools">Popular Free Tools</h2>
</div>

<div class="grid">

<!-- Percentage -->

<div class="card tool-card">
<div class="icon">📊</div>
<h3>Percentage Calculator</h3>
<p>Calculate percentages instantly.</p>

<input id="num1" type="number" placeholder="Enter number">
<input id="num2" type="number" placeholder="Enter percentage">

<button class="action" onclick="percentage()">Calculate</button>

<div id="percentResult" class="result">Result will appear here</div>
</div>


<!-- Salary -->

<div class="card tool-card">
<div class="icon">💵</div>
<h3>Hourly Pay Calculator</h3>
<p>Calculate weekly, monthly and yearly pay.</p>

<input id="hourly" type="number" placeholder="Hourly pay ($)">
<input id="hours" type="number" placeholder="Hours per week">

<button class="action" onclick="salary()">Calculate</button>

<div id="salaryResult" class="result">Result will appear here</div>
</div>


<!-- Word Counter -->

<div class="card tool-card">
<div class="icon">📝</div>
<h3>Word Counter</h3>
<p>Count words and characters in your text.</p>

<textarea id="text" rows="5"
placeholder="Type or paste your text..."
oninput="wordCounter()"></textarea>

<div id="wordResult" class="result">
0 words • 0 characters
</div>
</div>


<!-- Unit Converter -->

<div class="card tool-card">
<div class="icon">📏</div>
<h3>Miles → Kilometers</h3>
<p>Convert miles into kilometers.</p>

<input id="miles" type="number" placeholder="Miles">

<button class="action" onclick="convertMiles()">
Convert
</button>

<div id="mileResult" class="result">
Result will appear here
</div>
</div>


<!-- Age -->

<div class="card tool-card">
<div class="icon">🎂</div>
<h3>Age Calculator</h3>
<p>Calculate your approximate age.</p>

<input id="birth" type="date">

<button class="action" onclick="ageCalculator()">
Calculate Age
</button>

<div id="ageResult" class="result">
Result will appear here
</div>
</div>


<!-- Tip -->

<div class="card tool-card">
<div class="icon">💳</div>
<h3>Tip Calculator</h3>
<p>Calculate restaurant tips quickly.</p>

<input id="bill" type="number" placeholder="Bill amount ($)">
<input id="tip" type="number" placeholder="Tip percentage">

<button class="action" onclick="tipCalculator()">
Calculate
</button>

<div id="tipResult" class="result">
Result will appear here
</div>
</div>

</div>


<div class="adbox">
Advertisement space
<br>
<span>Monetization can be added here later after meeting an ad network's requirements.</span>
</div>


<section id="about" class="info">

<h2>About ToolNest</h2>

<p>
ToolNest provides simple free online tools designed to make
everyday calculations and tasks easier.
</p>

<p>
The website can be expanded with more calculators, useful
articles and other tools as the audience grows.
</p>

</section>

</main>


<footer>
© 2026 ToolNest • Free Online Tools
</footer>


<script>

function percentage(){

let number=parseFloat(document.getElementById("num1").value);
let percent=parseFloat(document.getElementById("num2").value);

if(isNaN(number)||isNaN(percent)){
document.getElementById("percentResult").innerText=
"Please enter both numbers.";
return;
}

let result=number*percent/100;

document.getElementById("percentResult").innerText=
percent+"% of "+number+" = "+result;
}


function salary(){

let hourly=parseFloat(document.getElementById("hourly").value);
let hours=parseFloat(document.getElementById("hours").value);

if(isNaN(hourly)||isNaN(hours)){
document.getElementById("salaryResult").innerText=
"Please enter both values.";
return;
}

let weekly=hourly*hours;
let monthly=weekly*52/12;
let yearly=weekly*52;

document.getElementById("salaryResult").innerText=
"Weekly: $"+weekly.toFixed(2)+
" | Monthly: $"+monthly.toFixed(2)+
" | Yearly: $"+yearly.toFixed(2);
}


function wordCounter(){

let text=document.getElementById("text").value.trim();

let words=text?
text.split(/\s+/).length:0;

let chars=text.length;

document.getElementById("wordResult").innerText=
words+" words • "+chars+" characters";
}


function convertMiles(){

let miles=parseFloat(document.getElementById("miles").value);

if(isNaN(miles)){
document.getElementById("mileResult").innerText=
"Please enter miles.";
return;
}

let km=miles*1.609344;

document.getElementById("mileResult").innerText=
miles+" miles = "+km.toFixed(2)+" km";
}


function ageCalculator(){

let birth=document.getElementById("birth").value;

if(!birth){
document.getElementById("ageResult").innerText=
"Please select your birth date.";
return;
}

let birthDate=new Date(birth);
let today=new Date();

let age=today.getFullYear()-birthDate.getFullYear();

let month=today.getMonth()-birthDate.getMonth();

if(
month<0 ||
(month===0 && today.getDate()<birthDate.getDate())
){
age--;
}

document.getElementById("ageResult").innerText=
"Your age is approximately "+age+" years.";
}


function tipCalculator(){

let bill=parseFloat(document.getElementById("bill").value);
let tip=parseFloat(document.getElementById("tip").value);

if(isNaN(bill)||isNaN(tip)){
document.getElementById("tipResult").innerText=
"Please enter bill and tip.";
return;
}

let tipAmount=bill*tip/100;
let total=bill+tipAmount;

document.getElementById("tipResult").innerText=
"Tip: $"+tipAmount.toFixed(2)+
" | Total: $"+total.toFixed(2);
}


function searchTools(){

let query=document.getElementById("search")
.value.toLowerCase();

let cards=document.querySelectorAll(".tool-card");

cards.forEach(card=>{

let text=card.innerText.toLowerCase();

if(text.includes(query)){
card.classList.remove("hidden");
}else{
card.classList.add("hidden");
}

});

}

</script>

</body>
</html>
<!--
**rohankamble00099-debug/rohankamble00099-debug** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
