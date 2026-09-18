<!DOCTYPE html>
<html>
<head>
<title>Minecraft Chat</title>
</head>
<body>

<h2>Send Message To Minecraft</h2>

<input id="Gamename" placeholder="Game name"><br><br>

<input id="JAVA OR PE ?" placeholder="JAVA?-&-PE?"><br><br>

<button onclick="sendMessage()">Submit</button>

<script>
function sendMessage() {

const name =
document.getElementById("Game name").value;

const msg =
document.getElementById("JAVA?-&-PE?").value;

fetch("https://discord.com/api/webhooks/1550585298017058999/hRs9SlXT83cY9osHLjxmE4WeKOHp_Egejfx3RI_hTWHx-NJFL1ycxr1itTw-wtE8cqk8", {
method: "POST",
headers: {
"Content-Type": "application/json"
},
body: JSON.stringify({
content: "[WEB] " + name + ": " + msg
})
});

alert("Message Sent!");
}
</script>

</body>
</html>
