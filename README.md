<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1,maximum-scale=1,user-scalable=no">
<title>DARK LIBRARY | Premium Nursing Hub</title>

<script src="https://telegram.org/js/telegram-web-app.js"></script>

<style>
:root {
  --bg:#080d0b;
  --card:#111a15;
  --card2:#17231b;
  --green:#20c779;
  --green2:#0e8f56;
  --text:#f1f5f2;
  --muted:#92a399;
  --border:#24372b;
  --danger:#f04444;
}
*{box-sizing:border-box}
body{
  margin:0;background:var(--bg);color:var(--text);
  font-family:Arial,Helvetica,sans-serif;
  padding-bottom:95px;
}
button,input,select{font:inherit}
button{cursor:pointer}
.header{
  padding:22px 18px 18px;
  background:linear-gradient(140deg,#10291c,#09100c 75%);
  border-bottom:1px solid var(--border);
}
.brand{display:flex;align-items:center;gap:12px}
.logo{
  width:49px;height:49px;border-radius:16px;
  display:grid;place-items:center;
  background:linear-gradient(145deg,#21d581,#087343);
  font-size:25px;box-shadow:0 5px 24px #16b96a30;
}
h1{font-size:19px;margin:0;letter-spacing:1px}
.subtitle{font-size:11px;color:var(--green);margin-top:5px;letter-spacing:2px}
.status{
  display:inline-block;margin-top:17px;padding:7px 11px;
  background:#173525;border:1px solid #28543a;
  border-radius:30px;font-size:12px;color:#72e8a9;
}
main{padding:18px 15px;max-width:700px;margin:auto}
.page{display:none}
.page.active{display:block}
.heading{font-size:21px;font-weight:800;margin:7px 0}
.description{color:var(--muted);font-size:13px;line-height:1.6;margin:7px 0 19px}
.card{
  background:linear-gradient(145deg,var(--card2),var(--card));
  border:1px solid var(--border);border-radius:19px;
  padding:17px;margin-bottom:13px;
}
.profile-row{display:flex;align-items:center;gap:13px}
.avatar{
  width:55px;height:55px;border-radius:50%;
  display:grid;place-items:center;background:#21452f;
  border:2px solid #318858;font-size:23px;overflow:hidden;
}
.avatar img{width:100%;height:100%;object-fit:cover}
.name{font-weight:bold;font-size:16px}
.muted{font-size:12px;color:var(--muted);margin-top:5px}
.badge{
  display:inline-block;padding:5px 8px;border-radius:8px;
  background:#16472e;color:#80f0ad;font-size:10px;margin-top:7px;
}
.stats{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:11px}
.stat{
  background:var(--card);border:1px solid var(--border);
  padding:16px 13px;border-radius:17px;
}
.stat-icon{font-size:23px}
.stat-value{font-size:22px;font-weight:bold;margin-top:10px}
.stat-label{font-size:12px;color:var(--muted);margin-top:5px}
.section-title{font-size:16px;font-weight:bold;margin:23px 0 12px}
.grid{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:10px}
.subject{
  text-align:left;background:var(--card);color:var(--text);
  border:1px solid var(--border);border-radius:15px;padding:14px 12px;
  min-height:105px;
}
.subject:active{border-color:var(--green);background:#183122}
.subject-icon{font-size:23px}
.subject-name{font-size:13px;font-weight:bold;margin-top:10px}
.subject-count{font-size:11px;color:var(--muted);margin-top:5px}
.btn{
  width:100%;border:0;border-radius:13px;padding:14px;
  background:var(--green);color:#06170d;font-weight:bold;
  margin-top:10px;
}
.btn.secondary{
  background:#1b3023;color:#a7f3c2;border:1px solid #2c5239;
}
.btn.danger{background:#3a1719;color:#ff9a9a;border:1px solid #64272b}
.input,.select{
  width:100%;background:#0a100c;color:var(--text);
  border:1px solid var(--border);border-radius:12px;
  padding:13px;margin:7px 0;outline:none;
}
.input:focus,.select:focus{border-color:var(--green)}
.searchbar{position:relative;margin-bottom:14px}
.searchbar input{padding-left:42px}
.search-icon{position:absolute;left:14px;top:21px}
.file-row{
  display:flex;align-items:center;gap:11px;
  background:var(--card);border:1px solid var(--border);
  border-radius:13px;padding:13px;margin-top:9px;
}
.file-icon{font-size:24px}
.file-info{flex:1;min-width:0}
.file-name{font-size:13px;font-weight:bold;overflow-wrap:anywhere}
.file-sub{font-size:11px;color:var(--muted);margin-top:5px}
.small-btn{
  background:#1b3927;color:#9bf2ba;border:1px solid #2b5238;
  padding:8px 10px;border-radius:9px;font-size:12px;
}
.setting-row{
  display:flex;align-items:center;justify-content:space-between;
  gap:10px;padding:15px 0;border-bottom:1px solid var(--border);
}
.setting-row:last-child{border-bottom:0}
.setting-label{font-size:14px;font-weight:bold}
.setting-help{font-size:12px;color:var(--muted);margin-top:5px}
.switch{width:45px;height:25px;accent-color:var(--green)}
.bottom{
  position:fixed;bottom:0;left:0;right:0;z-index:10;
  display:flex;justify-content:space-around;gap:2px;
  padding:10px 3px calc(10px + env(safe-area-inset-bottom));
  background:#0b120eF5;border-top:1px solid var(--border);
  backdrop-filter:blur(12px);
}
.nav-item{
  flex:1;text-align:center;text-decoration:none;color:#819187;
  padding:5px 0;font-size:20px;border:0;background:none;
}
.nav-item span{display:block;font-size:10px;margin-top:5px}
.nav-item.active{color:var(--green)}
.notice{
  border:1px solid #4a4425;background:#242316;color:#e7d994;
  border-radius:12px;padding:12px;font-size:12px;line-height:1.5;
  margin:12px 0;
}
.empty{text-align:center;padding:25px 10px;color:var(--muted);font-size:13px}
.footer{text-align:center;color:#617267;font-size:10px;margin:25px 0 10px}
.hidden{display:none!important}
body.light{
  --bg:#edf3ef;--card:#fff;--card2:#f5faf6;
  --text:#15221a;--muted:#617267;--border:#d6e2d9;
}
body.light .input,body.light .select{background:#fff;color:#15221a}
body.light .bottom{background:#ffffffF5}
body.light .header{background:linear-gradient(140deg,#d8f8e4,#edf3ef)}
body.light .logo{color:#fff}
@media(min-width:550px){
  .grid{grid-template-columns:repeat(3,minmax(0,1fr))}
  .stats{grid-template-columns:repeat(4,minmax(0,1fr))}
}
</style>
</head>

<body>
<header class="header">
  <div class="brand">
    <div class="logo">📚</div>
    <div>
      <h1>DARK LIBRARY</h1>
      <div class="subtitle">FREE • PREMIUM • NURSING HUB</div>
    </div>
  </div>
  <div class="status">● LIBRARY SYSTEM ONLINE</div>
</header>

<main>

<!-- HOME -->
<section id="home" class="page active">
  <div class="heading">Welcome Back 👋</div>
  <div class="description">Your nursing study library, all in one place.</div>

  <div class="card">
    <div class="profile-row">
      <div class="avatar" id="avatar">👤</div>
      <div>
        <div class="name" id="name">Nursing Student</div>
        <div class="muted" id="username">Telegram User</div>
        <div class="badge">⭐ MEMBER</div>
      </div>
    </div>
  </div>

  <div class="stats">
    <div class="stat">
      <div class="stat-icon">📚</div>
      <div class="stat-value" id="booksCount">0</div>
      <div class="stat-label">Books Opened</div>
    </div>
    <div class="stat">
      <div class="stat-icon">🎥</div>
      <div class="stat-value" id="videosCount">0</div>
      <div class="stat-label">Courses Watched</div>
    </div>
    <div class="stat">
      <div class="stat-icon">📁</div>
      <div class="stat-value" id="filesCount">0</div>
      <div class="stat-label">Files Added</div>
    </div>
    <div class="stat">
      <div class="stat-icon">💾</div>
      <div class="stat-value" id="storageCount">0 B</div>
      <div class="stat-label">Local File Size</div>
    </div>
  </div>

  <div class="section-title">⚡ Quick Access</div>
  <div class="grid">
    <button class="subject" onclick="showPage('library')">
      <div class="subject-icon">📚</div><div class="subject-name">Open Library</div>
      <div class="subject-count">Browse subjects</div>
    </button>
    <button class="subject" onclick="showPage('search')">
      <div class="subject-icon">🔍</div><div class="subject-name">Search Files</div>
      <div class="subject-count">Find study material</div>
    </button>
    <button class="subject" onclick="showPage('files')">
      <div class="subject-icon">📂</div><div class="subject-name">File Manager</div>
      <div class="subject-count">Manage selected files</div>
    </button>
    <button class="subject" onclick="showPage('profile')">
      <div class="subject-icon">👤</div><div class="subject-name">My Profile</div>
      <div class="subject-count">Account information</div>
    </button>
  </div>

  <button class="btn" onclick="openBot()">🤖 OPEN TELEGRAM BOT</button>
  <button class="btn secondary" onclick="joinChannel()">📢 JOIN CHANNEL</button>

  <div class="notice">
    🔐 File uploads are stored only in this browser during local testing.
    Permanent online storage and server-side file management require a backend.
  </div>
</section>

<!-- LIBRARY -->
<section id="library" class="page">
  <div class="heading">📚 Nursing Library</div>
  <div class="description">Select a subject to browse its study materials.</div>
  <div class="searchbar">
    <span class="search-icon">🔍</span>
    <input class="input" id="subjectSearch" placeholder="Search subjects..." oninput="renderSubjects()">
  </div>
  <div class="grid" id="subjectGrid"></div>
</section>

<!-- SEARCH -->
<section id="search" class="page">
  <div class="heading">🔍 Search Library</div>
  <div class="description">Search your locally added files by name or subject.</div>
  <input class="input" id="globalSearch" placeholder="Enter file name or subject..." oninput="renderSearch()">
  <div id="searchResults"></div>
</section>

<!-- PROFILE -->
<section id="profile" class="page">
  <div class="heading">👤 My Profile</div>
  <div class="description">Your Telegram account and local usage statistics.</div>
  <div class="card">
    <div class="profile-row">
      <div class="avatar" id="profileAvatar">👤</div>
      <div>
        <div class="name" id="profileName">Nursing Student</div>
        <div class="muted" id="profileUsername">Telegram User</div>
        <div class="badge">⭐ MEMBER</div>
      </div>
    </div>
  </div>
  <div class="card">
    <div class="setting-row"><div class="setting-label">📚 Books opened</div><strong id="profileBooks">0</strong></div>
    <div class="setting-row"><div class="setting-label">🎥 Courses watched</div><strong id="profileVideos">0</strong></div>
    <div class="setting-row"><div class="setting-label">📁 Local files</div><strong id="profileFiles">0</strong></div>
  </div>
  <div class="notice">Premium membership is a visual placeholder. Actual membership status must be verified by a secure backend.</div>
</section>

<!-- SETTINGS -->
<section id="settings" class="page">
  <div class="heading">⚙️ Settings</div>
  <div class="description">Customize your library experience.</div>
  <div class="card">
    <div class="setting-row">
      <div><div class="setting-label">🌙 Dark Mode</div><div class="setting-help">Enable dark theme</div></div>
      <input class="switch" type="checkbox" id="darkMode" checked onchange="toggleTheme()">
    </div>
    <div class="setting-row">
      <div><div class="setting-label">🔔 Notifications</div><div class="setting-help">Preference only; notifications require bot setup</div></div>
      <input class="switch" type="checkbox" id="notifications">
    </div>
    <div class="setting-row">
      <div><div class="setting-label">📚 App Version</div><div class="setting-help">DARK LIBRARY v2.0</div></div>
      <span>🟢</span>
    </div>
    <button class="btn" onclick="openBot()">🤖 OPEN BOT</button>
    <button class="btn secondary" onclick="joinChannel()">📢 JOIN CHANNEL</button>
    <button class="btn danger" onclick="exitApp()">🚪 EXIT MINI APP</button>
  </div>
</section>

<!-- FILE MANAGER -->
<section id="files" class="page">
  <div class="heading">📁 File Manager</div>
  <div class="description">Add files for this browser session and download them again.</div>

  <div class="card">
    <label class="setting-label" for="fileSubject">Choose subject</label>
    <select class="select" id="fileSubject"></select>

    <label class="setting-label" for="fileInput">Choose file</label>
    <input class="input" type="file" id="fileInput">

    <button class="btn" onclick="addLocalFile()">📤 ADD FILE</button>
    <div class="muted">Demo storage: selected files remain in browser memory only until this page is closed or refreshed.</div>
  </div>

  <div class="card">
    <div class="setting-row">
      <div><div class="setting-label">📦 Files in session</div><div class="setting-help">Local demo storage</div></div>
      <strong id="managerFilesCount">0</strong>
    </div>
    <div class="setting-row">
      <div><div class="setting-label">💾 Total file size</div><div class="setting-help">Not server storage</div></div>
      <strong id="managerStorage">0 B</strong>
    </div>
  </div>

  <div class="section-title">Your Files</div>
  <div id="fileList"></div>
  <button class="btn secondary" onclick="clearLocalFiles()">🗑️ CLEAR SESSION FILES</button>
</section>

<div class="footer">DARK LIBRARY • NURSING HUB<br>Study smart. Grow stronger. 💚</div>
</main>

<nav class="bottom">
  <button class="nav-item active" data-page="home" onclick="showPage('home')">🏠<span>Home</span></button>
  <button class="nav-item" data-page="library" onclick="showPage('library')">📚<span>Library</span></button>
  <button class="nav-item" data-page="search" onclick="showPage('search')">🔍<span>Search</span></button>
  <button class="nav-item" data-page="profile" onclick="showPage('profile')">👤<span>Profile</span></button>
  <button class="nav-item" data-page="settings" onclick="showPage('settings')">⚙️<span>Settings</span></button>
</nav>

<script>
"use strict";

/* Telegram Web App */
const tg = window.Telegram && window.Telegram.WebApp ? window.Telegram.WebApp : null;

if (tg) {
  tg.ready();
  tg.expand();
}

/* Replace these with your verified official destinations if needed. */
const BOT_URL = "https://t.me/I6x2bot";
const CHANNEL_URL = "https://t.me/+sWfgnxDvWBVhOGI9";

const subjects = [
  ["BOOKS","📚","Books, Notes & PDFs"],
  ["NOTICE","📢","Official Announcements"],
  ["DOUBTS","❓","Doubts & Discussion"],
  ["CLASSES","🎬","Recorded Classes"],
  ["MCQ","🧠","Daily MCQ Challenge"],
  ["NORCET","🎯","NORCET Practice"],
  ["ADMIN","🏥","Nursing Administration"],
  ["EDU","👨‍🏫","Nursing Education"],
  ["STATS","📊","Statistics"],
  ["RSRCH","🔬","Nursing Research"],
  ["RADIO","🩻","Radiology"],
  ["PATHO","🧫","Pathology"],
  ["PSY","🧠","Psychiatric Nursing"],
  ["CHN","🌍","Community Health Nursing"],
  ["MSN","❤️","Medical Surgical Nursing"],
  ["CHILD","👶","Child Health Nursing"],
  ["OBG","🤰","Obstetrics & Gynaecology"],
  ["PHARMA","💊","Pharmacology"],
  ["ENDO","🦋","Endocrine System"],
  ["HEMATO","🩸","Hematology"]
];

let localFiles = [];
let booksOpened = 0;
let videosWatched = 0;

function showPage(id) {
  document.querySelectorAll(".page").forEach(p => p.classList.remove("active"));
  const target = document.getElementById(id);
  if (target) target.classList.add("active");

  document.querySelectorAll(".nav-item").forEach(b => {
    b.classList.toggle("active", b.dataset.page === id);
  });

  if (id === "files") renderFiles();
  if (id === "search") renderSearch();

  window.scrollTo({top:0,behavior:"smooth"});
}

function openBot() {
  if (tg && tg.openTelegramLink) tg.openTelegramLink(BOT_URL);
  else window.open(BOT_URL,"_blank","noopener");
}

function joinChannel() {
  if (tg && tg.openTelegramLink) tg.openTelegramLink(CHANNEL_URL);
  else window.open(CHANNEL_URL,"_blank","noopener");
}

function exitApp() {
  if (tg && tg.close) tg.close();
  else alert("You can close this browser tab.");
}

function toggleTheme() {
  const enabled = document.getElementById("darkMode").checked;
  document.body.classList.toggle("light",!enabled);
  try { localStorage.setItem("darkLibraryLightMode",String(!enabled)); } catch(e) {}
}

function formatSize(bytes) {
  if (bytes < 1024) return bytes + " B";
  if (bytes < 1024*1024) return (bytes/1024).toFixed(1) + " KB";
  if (bytes < 1024*1024*1024) return (bytes/(1024*1024)).toFixed(1) + " MB";
  return (bytes/(1024*1024*1024)).toFixed(2) + " GB";
}

function escapeHTML(value) {
  return String(value).replace(/[&<>"']/g, ch => ({
    "&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;","'":"&#39;"
  })[ch]);
}

function renderSubjects() {
  const q = document.getElementById("subjectSearch").value.trim().toLowerCase();
  const grid = document.getElementById("subjectGrid");
  const filtered = subjects.filter(s =>
    s[0].toLowerCase().includes(q) || s[2].toLowerCase().includes(q)
  );

  grid.innerHTML = filtered.map(s => {
    const count = localFiles.filter(f => f.subject === s[0]).length;
    return `<button class="subject" onclick="openSubject('${s[0]}')">
      <div class="subject-icon">${s[1]}</div>
      <div class="subject-name">${escapeHTML(s[2])}</div>
      <div class="subject-count">${count} local file(s)</div>
    </button>`;
  }).join("") || '<div class="empty">No subjects found.</div>';
}

function openSubject(code) {
  showPage("files");
  document.getElementById("fileSubject").value = code;
  renderFiles();
}

function addLocalFile() {
  const input = document.getElementById("fileInput");
  const subject = document.getElementById("fileSubject").value;
  const file = input.files && input.files[0];

  if (!file) {
    alert("Bhai, pehle file select karo.");
    return;
  }

  if (file.size > 50*1024*1024) {
    alert("Demo limit: maximum 50 MB per file.");
    return;
  }

  const id = Date.now().toString(36) + Math.random().toString(36).slice(2,7);
  localFiles.push({id,name:file.name,size:file.size,type:file.type,subject,blob:file});
  input.value = "";
  updateStats();
  renderFiles();
  renderSubjects();
  alert("File browser session mein add ho gayi. Permanent online upload abhi configured nahi hai.");
}

function renderFiles() {
  const list = document.getElementById("fileList");
  document.getElementById("managerFilesCount").textContent = localFiles.length;

  const total = localFiles.reduce((sum,f) => sum + f.size,0);
  document.getElementById("managerStorage").textContent = formatSize(total);

  if (!localFiles.length) {
    list.innerHTML = '<div class="empty">📂 No files yet.<br>Select a file above to begin.</div>';
    return;
  }

  list.innerHTML = localFiles.map(f => {
    const subjectName = subjects.find(s => s[0] === f.subject)?.[2] || f.subject;
    return `<div class="file-row">
      <div class="file-icon">📄</div>
      <div class="file-info">
        <div class="file-name">${escapeHTML(f.name)}</div>
        <div class="file-sub">${escapeHTML(subjectName)} • ${formatSize(f.size)}</div>
      </div>
      <button class="small-btn" onclick="downloadLocalFile('${f.id}')">⬇️</button>
      <button class="small-btn" onclick="deleteLocalFile('${f.id}')">✕</button>
    </div>`;
  }).join("");
}

function downloadLocalFile(id) {
  const f = localFiles.find(x => x.id === id);
  if (!f) return;

  const url = URL.createObjectURL(f.blob);
  const a = document.createElement("a");
  a.href = url;
  a.download = f.name;
  document.body.appendChild(a);
  a.click();
  a.remove();
  setTimeout(() => URL.revokeObjectURL(url),1000);
}

function deleteLocalFile(id) {
  const f = localFiles.find(x => x.id === id);
  if (!f) return;
  if (!confirm("Delete " + f.name + " from this session?")) return;

  localFiles = localFiles.filter(x => x.id !== id);
  updateStats();
  renderFiles();
  renderSubjects();
  renderSearch();
}

function clearLocalFiles() {
  if (!localFiles.length) {
    alert("No files to clear.");
    return;
  }
  if (!confirm("Clear all files from this browser session?")) return;

  localFiles = [];
  updateStats();
  renderFiles();
  renderSubjects();
  renderSearch();
}

function renderSearch() {
  const query = document.getElementById("globalSearch").value.trim().toLowerCase();
  const results = document.getElementById("searchResults");
  const filtered = localFiles.filter(f => {
    const subjectName = subjects.find(s => s[0] === f.subject)?.[2] || f.subje
