<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>TERMUX LAB 3.0</title>
<style>
body{background:#080b0a;color:#00ff88;font-family:monospace;margin:0;padding:20px}
.container{max-width:700px;margin:auto}
h1{color:#00ff88;text-shadow:0 0 12px #00ff88}
.box{border:1px solid #00ff88;padding:15px;margin:15px 0;border-radius:8px;background:#101713}
button{background:#00ff88;color:#000;border:0;padding:12px;margin:5px;border-radius:5px;font-weight:bold}
#output{white-space:pre-wrap;color:#b5ffd5;min-height:100px}
</style>
</head>
<body>
<div class="container">
<h1>TERMUX LAB 3.0</h1>
<p>Welcome to my terminal lab.</p>
<div class="box">
<h3>COMMAND CENTER</h3>
<button onclick="run('help')">HELP</button>
<button onclick="run('date')">DATE</button>
<button onclick="run('status')">STATUS</button>
<button onclick="run('files')">FILES</button>
<button onclick="run('clear')">CLEAR</button>
</div>
<div class="box">
<h3>TERMINAL</h3>
<div id="output">TERMUX LAB 3.0 hazır...<br></div>
</div>
<p>Educational Linux command simulator.</p>
</div>
<script>
function run(cmd){
let out=document.getElementById("output");
if(cmd==="clear"){out.innerHTML="";return;}
let messages={
help:"Komutlar: help, date, status, files, clear",
date:new Date().toLocaleString("tr-TR"),
status:"SYSTEM STATUS: ONLINE",
files:"index.html\nmain.py\nlab.py"
};
out.innerHTML+="> "+cmd+"\n"+messages[cmd]+"\n\n";
}
</script>
</body>
</html>
