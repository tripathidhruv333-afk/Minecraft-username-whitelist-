<!DOCTYPE html>
<html>
<head>
<title>Minecraft Chat</title>
</head>
<body>

<h2>Send Message To Minecraft</h2>

<input id="name" placeholder="Your Name"><br><br>

<input id="message" placeholder="Message"><br><br>

<button onclick="sendMessage()">Submit</button>

<script>
function sendMessage() {

const name =
document.getElementById("name").value;

const msg =
document.getElementById("message").value;

fetch("https://discord.com/api/webhooks/1550461116470272020/pTVV1d8D_JMFu6qUIwUlaBkeUpFbRxhtu-1mm8a3FoYAZlvWDuBw41iEwna6YOlQ3eMQ", {
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
