<!DOCTYPE html><html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>TwinBladesGaming</title><style>
body {
    margin: 0;
    font-family: Arial;
    background: #020617;
    color: white;
}

header {
    text-align: center;
    padding: 20px;
}

.logo {
    width: 280px;
    animation: glow 2s infinite alternate;
}

@keyframes glow {
    from { filter: drop-shadow(0 0 5px #3b82f6); }
    to { filter: drop-shadow(0 0 20px #3b82f6); }
}

.container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
}

.card {
    border: 1px solid #3b82f6;
    border-radius: 12px;
    margin: 15px;
    padding: 15px;
    width: 260px;
    text-align: center;
    position: relative;
}

.card:hover {
    box-shadow: 0 0 20px #3b82f6;
}

button {
    background: #1e293b;
    color: white;
    border: 1px solid #3b82f6;
    padding: 10px 20px;
    border-radius: 8px;
    cursor: pointer;
}

.neon {
    background: #3b82f6;
    box-shadow: 0 0 10px #3b82f6;
}

.page { display: none; }
.active { display: block; }

.sword {
    position: absolute;
    width: 50px;
    top: -40px;
    opacity: 0;
}

#s1 { left: 10%; }
#s2 { right: 10%; }

.show img {
    animation: drop 0.5s forwards;
    opacity: 1;
}

@keyframes drop {
    from { top: -40px; }
    to { top: 30px; }
}

</style></head><body><header>
    <img src="logo.png" class="logo">
</header><!-- HOME PAGE --><div id="home" class="page active">
    <div class="container"><!-- MODPACK CARD -->
    <div class="card" onclick="openDetails('BladeCraft')">
        <h3>BladeCraft</h3>
        <p>FPS + Combat Modpack</p>
        <button>View</button>
    </div>

    <div class="card" onclick="openDetails('MagicWorld')">
        <h3>MagicWorld</h3>
        <p>Fantasy Mods</p>
        <button>View</button>
    </div>

</div>

</div><!-- DETAILS PAGE --><div id="details" class="page">
    <h2 id="title"></h2><p>Requirements:</p>
<ul>
    <li>Minecraft 1.20+</li>
    <li>4GB RAM</li>
</ul>

<label>Select Minecraft Version</label><br>
<select id="mc">
    <option>1.20</option>
    <option>1.19</option>
</select>

<br><br>

<label>Select Modpack Version</label><br>
<select id="modv">
    <option>v1.0</option>
    <option>v2.0</option>
</select>

<br><br>

<div style="position:relative;display:inline-block;">
    <img id="s1" class="sword" src="https://i.imgur.com/6X12UGK.png">
    <img id="s2" class="sword" src="https://i.imgur.com/6X12UGK.png">

    <button id="download" onclick="activate()">Download</button>
</div>

</div><script>
function openDetails(name){
    document.getElementById('home').classList.remove('active');
    document.getElementById('details').classList.add('active');
    document.getElementById('title').innerText = name;
}

function activate(){
    document.getElementById('download').classList.add('neon');
    document.querySelector('div').classList.add('show');

    setTimeout(()=>{
        window.open('https://yourlink.com');
    },800);
}
</script></body>
</html>
