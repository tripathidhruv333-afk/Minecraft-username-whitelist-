<!DOCTYPE html>
<html>
<head>
<title>Minecraft Chat</title>
</head>
<body>

<h2>Send Message To Minecraft</h2>

<input id="Gamename" placeholder="Your Name"><br><br>

<input id="JAVA OR PE ?" placeholder="Message"><br><br>

<button onclick="sendMessage()">Submit</button>

<script>
function sendMessage() {

const name =
document.getElementById("name").value;

const msg =
document.getElementById("message").value;

fetch("GO7MTU1MDQ0MjkyNDM2MDIwNDMyOAUbo.RB4BmXJHkiDTwTskYLvnRqn5VY8ZEOpYgRQyew", {
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
