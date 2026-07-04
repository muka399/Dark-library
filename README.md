# Dark-library
FREE PREMIUM 
<h3>📚 Library Status</h3>

<p>Premium Member ⭐</p>

</div>

<div class="info">

<h3>📖 Books Opened</h3>

<p>0 Books</p>

</div>

<div class="info">

<h3>🎥 Courses Watched</h3>

<p>0 Videos</p>

</div>

<button
class="btn"
onclick="window.open('https://t.me/l6x2bot')">

🤖 Open Bot

</button>

<button
class="btn btn2"
onclick="window.open('https://t.me/+sWfgnxDvWBVhOGI9')">

📢 Join Channel

</button>

</div>

<nav class="bottom">

<a href="index.html">

🏠

<span>Home</span>

</a>

<a href="library.html">

📚

<span>Library</span>

</a>

<a href="search.html">

🔍

<span>Search</span>

</a>

<a href="profile.html">

👤

<span>Profile</span>

</a>

<a href="settings.html">

⚙️

<span>Settings</span>

</a>

</nav>

<script>

const tg = Telegram.WebApp;

tg.ready();

tg.expand();

if(tg.initDataUnsafe.user){

const u = tg.initDataUnsafe.user;

document.getElementById("name").innerHTML =

u.first_name + " " + (u.last_name || "");

document.getElementById("username").innerHTML =

u.username ? "@"+u.username : "Telegram User";

if(u.photo_url){

document.getElementById("avatar").src=u.photo_url;

}

}

</script>

</body>

</html>
<!DOCTYPE html>
<html lang="en">
<head>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Settings</title>

<link rel="stylesheet" href="style.css">
<script src="https://telegram.org/js/telegram-web-app.js"></script>

<style>

.settings{
padding:90px 15px;
}

.box{
background:#161b22;
border-radius:18px;
padding:18px;
margin-bottom:15px;
display:flex;
justify-content:space-between;
align-items:center;
}

.box h3{
font-size:17px;
}

.box p{
font-size:13px;
color:#999;
margin-top:4px;
}

.switch{
position:relative;
display:inline-block;
width:50px;
height:28px;
}

.switch input{
display:none;
}

.slider{
position:absolute;
cursor:pointer;
top:0;
left:0;
right:0;
bottom:0;
background:#555;
border-radius:30px;
transition:.3s;
}

.slider:before{
content:"";
position:absolute;
height:22px;
width:22px;
left:3px;
top:3px;
background:white;
border-radius:50%;
transition:.3s;
}

input:checked + .slider{
background:#2ea043;
}

input:checked + .slider:before{
transform:translateX(22px);
}

.btn{
width:100%;
padding:15px;
border:none;
border-radius:15px;
margin-top:15px;
background:#238636;
color:white;
font-size:16px;
cursor:pointer;
}

.red{
background:#dc2626;
}

</style>

</head>

<body>

<div class="header">

<div class="logo">⚙️</div>

<div class="title">

<h2>Settings</h2>

<p>Customize App</p>

</div>

</div>


<div class="settings">

<div class="box">

<div>

<h3>🌙 Dark Mode</h3>

<p>Enable Dark Theme</p>

</div>

<label class="switch">

<input type="checkbox" checked>

<span class="slider"></span>

</label>

</div>


<div class="box">

<div>

<h3>🔔 Notifications</h3>

<p>Receive Updates</p>

</div>

<label class="switch">

<input type="checkbox" checked>

<span class="slider"></span>

</label>

</div>


<div class="box">

<div>

<h3>📞 Contact Admin</h3>

<p>@l6x2bot</p>

</div>

</div>


<div class="box">

<div>

<h3>📚 Version</h3>

<p>Dark Library v1.0</p>

</div>

</div>


<button class="btn"
onclick="window.open('https://t.me/l6x2bot')">

🤖 Open Bot

</button>


<button class="btn"
onclick="window.open('https://t.me/+sWfgnxDvWBVhOGI9')">

📢 Join Channel

</button>


<button class="btn red"
onclick="Telegram.WebApp.close()">

🚪 Exit App

</button>

</div>


<nav class="bottom">

<a href="index.html">🏠<span>Home</span></a>

<a href="library.html">📚<span>Library</span></a>

<a href="search.html">🔍<span>Search</span></a>

<a href="profile.html">👤<span>Profile</span></a>

<a href="settings.html">⚙️<span>Settings</span></a>

</nav>

<script>

Telegram.WebApp.ready();

Telegram.WebApp.expand();

</script>

</body>
</html>
