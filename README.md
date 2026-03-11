<!DOCTYPE html><html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>MonkeAI Meme Coin</title>
<style>
body { font-family: Arial, sans-serif; margin: 0; padding: 0; background: #f5f5f5; color: #333; }
header { background: #ffcc00; padding: 20px; text-align: center; }
h1 { margin: 0; }
button { padding: 10px 20px; background: #ff6600; color: #fff; border: none; border-radius: 5px; cursor: pointer; }
button:hover { background: #e65c00; }
section { padding: 20px; max-width: 800px; margin: auto; }
#chatbox { border: 1px solid #ccc; padding: 10px; height: 300px; overflow-y: scroll; background: #fff; }
input[type=text] { width: 70%; padding: 10px; margin-right: 10px; border: 1px solid #ccc; border-radius: 5px; }
</style>
</head>
<body><header>
<h1>MonkeAI 🐒</h1>
<p>The Meme AI That Smells Crypto Pumps 🍌🚀</p>
<button onclick="scrollToChat()">Chat with MonkeAI</button>
</header><section id="chat-section">
<h2>Chat with MonkeAI</h2>
<div id="chatbox"></div>
<input type="text" id="userInput" placeholder="Type your message here...">
<button onclick="sendMessage()">Send</button>
</section><section>
<h2>Meme Coin Prediction Generator</h2>
<input type="text" id="coinName" placeholder="Enter coin name">
<button onclick="generatePrediction()">Predict Pump</button>
<p id="predictionResult"></p>
</section><section>
<h2>Buy MonkeAI Token</h2>
<p>Available on Solana</p>
<button onclick="window.open('https://www.pump.fun', '_blank')">Buy Now 🚀</button>
</section><section>
<h2>Join the Monke Army 🐒</h2>
<p>Follow us on X (Twitter) and Telegram for updates!</p>
<a href="https://twitter.com/" target="_blank">X (Twitter)</a> | <a href="https://t.me/" target="_blank">Telegram</a>
</section><script>
function scrollToChat() { document.getElementById('chat-section').scrollIntoView({behavior: 'smooth'}); }

function sendMessage() {
  const input = document.getElementById('userInput');
  const chatbox = document.getElementById('chatbox');
  const userMessage = input.value;
  if(!userMessage) return;

  const userDiv = document.createElement('div');
  userDiv.textContent = 'You: ' + userMessage;
  userDiv.style.marginBottom = '5px';
  userDiv.style.fontWeight = 'bold';
  chatbox.appendChild(userDiv);

  const monkeReply = generateMonkeReply(userMessage);
  const monkeDiv = document.createElement('div');
  monkeDiv.textContent = 'MonkeAI: ' + monkeReply;
  monkeDiv.style.marginBottom = '10px';
  monkeDiv.style.color = '#ff6600';
  chatbox.appendChild(monkeDiv);

  chatbox.scrollTop = chatbox.scrollHeight;
  input.value = '';
}

function generateMonkeReply(msg) {
  const responses = [
    'Monke sniffing chart… 🐒🍌 maybe pump soon 🚀',
    'Banana curve detected! 🍌 Hold strong 🐒',
    'Crash incoming? Monke says buy dip! 🐒',
    'Monke too lazy to check price… 😂',
    'Hoard bananas and meme coins! 🍌🚀',
    'Monke senses pump! 🐒💥'
  ];
  return responses[Math.floor(Math.random()*responses.length)];
}

function generatePrediction() {
  const coin = document.getElementById('coinName').value.trim();
  const result = document.getElementById('predictionResult');
  if(!coin) { result.textContent = 'Enter a coin name!'; return; }
  const predictions = ['smells like banana 🍌', 'moon incoming 🚀', 'ape mode activated 🐒', 'chart looks funny 😂', 'banana pump detected 🍌💥', 'hodl tight 🐒']
  const randomPred = predictions[Math.floor(Math.random()*predictions.length)];
  result.textContent = `Prediction for ${coin}: ${randomPred}`;
}
</script></body>
</html>
