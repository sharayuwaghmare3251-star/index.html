# index.html
Your universe of fun, games and surprises!
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>FUNVERSE | Enter the Unexpected</title>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  background: #080512;
  color: white;
  font-family: Arial, sans-serif;
  text-align: center;
}

header {
  padding: 25px 15px;
  border-bottom: 1px solid #39205d;
  background: #100a20;
}

.logo {
  color: #c99aff;
  font-size: 32px;
  font-weight: bold;
  letter-spacing: 4px;
}

header p {
  color: #aaa;
  margin-top: 8px;
}

.hero {
  padding: 85px 15px 55px;
  background: radial-gradient(circle, #38146c, #080512 70%);
}

.hero h1 {
  font-size: clamp(35px, 8vw, 65px);
  margin-bottom: 18px;
}

.hero h1 span {
  color: #c58aff;
}

.hero p {
  color: #ccc;
  font-size: 17px;
  line-height: 1.6;
}

button {
  background: linear-gradient(90deg, #873bff, #d34bff);
  color: white;
  border: none;
  padding: 14px 23px;
  border-radius: 25px;
  font-size: 15px;
  font-weight: bold;
  cursor: pointer;
  margin: 15px 5px;
}

button:hover {
  transform: scale(1.05);
}

h2 {
  margin-bottom: 25px;
  color: #d4aaff;
}

.section {
  padding: 50px 15px;
}

.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 18px;
  max-width: 950px;
  margin: auto;
}

.card {
  background: #171027;
  border: 1px solid #61358d;
  border-radius: 18px;
  padding: 28px 18px;
  transition: 0.3s;
}

.card:hover {
  transform: translateY(-6px);
  border-color: #d18aff;
  box-shadow: 0 0 20px #803baf55;
}

.card .icon {
  font-size: 40px;
  margin-bottom: 15px;
}

.card h3 {
  margin-bottom: 12px;
  color: #dfc0ff;
}

.card p {
  color: #bbb;
  line-height: 1.5;
}

#result {
  color: #f0caff;
  font-size: 18px;
  margin: 20px auto;
  max-width: 500px;
  line-height: 1.6;
}

footer {
  padding: 30px;
  color: #999;
  border-top: 1px solid #39205d;
}
</style>
</head>

<body>

<header>
  <div class="logo">✦ FUNVERSE</div>
  <p>Your universe of fun, games and surprises.</p>
</header>

<section class="hero">
  <h1>ENTER THE <span>UNEXPECTED.</span></h1>
  <p>One universe. Endless possibilities.<br>
  Games, mysteries and surprises await you.</p>
  <button onclick="document.getElementById('explore').scrollIntoView({behavior:'smooth'})">
    EXPLORE NOW ✨
  </button>
</section>

<section class="section" id="explore">
  <h2>✦ EXPLORE YOUR UNIVERSE ✦</h2>

  <div class="grid">

    <div class="card">
      <div class="icon">🎲</div>
      <h3>Random Surprise</h3>
      <p>Discover something unexpected.</p>
      <button onclick="surprise()">Try Me</button>
    </div>

    <div class="card">
      <div class="icon">🧠</div>
      <h3>Brain Challenge</h3>
      <p>Test your thinking skills.</p>
      <button onclick="quiz()">Play Quiz</button>
    </div>

    <div class="card">
      <div class="icon">🔮</div>
      <h3>Personality Lab</h3>
      <p>Discover your fun personality.</p>
      <button onclick="personality()">Discover</button>
    </div>

    <div class="card">
      <div class="icon">🕵️</div>
      <h3>Mystery Room</h3>
      <p>Can you solve a mysterious case?</p>
      <button onclick="mystery()">Investigate</button>
    </div>

  </div>

  <div id="result"></div>
</section>

<footer>
  <div class="logo">FUNVERSE ✦</div>
  <p style="margin-top:12px">Play • Explore • Discover • Have Fun!</p>
  <p style="margin-top:15px;font-size:12px">
    © 2026 FUNVERSE. All rights reserved.
  </p>
</footer>

<script>

const result = document.getElementById("result");

function surprise() {
  const things = [
    "✨ You're officially today's superstar!",
    "🌌 Somewhere, a new adventure is waiting.",
    "🎮 Challenge yourself to learn something new!",
    "💜 Your next great idea might be your best one.",
    "🚀 Fun fact: A day on Venus is longer than its year!"
  ];

  result.innerHTML = things[Math.floor(Math.random()*things.length)];
}

function quiz() {
  const answer = prompt("What is the next number? 2, 4, 8, 16, ?");
  
  if (answer === null) return;

  result.innerHTML = Number(answer) === 32
    ? "🎉 CORRECT! You're a genius!"
    : "🤔 Not quite! The answer is 32. Each number doubles.";
}

function personality() {
  const answer = prompt("Choose your favourite: 1. Stars 2. Ocean 3. Forest 4. Space");

  if (!answer) return;

  const types = {
    1: "⭐ STAR SOUL: Creative and full of dreams!",
    2: "🌊 OCEAN SOUL: Calm, curious and thoughtful!",
    3: "🌳 FOREST SOUL: Adventurous and imaginative!",
    4: "🌌 COSMIC SOUL: A curious explorer!"
  };

  result.innerHTML = types[answer] || "Choose 1, 2, 3 or 4!";
}

function mystery() {
  const answer = prompt("MYSTERY CASE #001: A man looks at a photo and says: 'Brothers and sisters I have none, but that man's father is my father's son.' Who is in the photo?");

  if (!answer) return;

  result.innerHTML = answer.toLowerCase().includes("son")
    ? "🎉 Correct! It's his son!"
    : "🕵️ Think again! Hint: The man in the photo is his child.";
}

</script>

</body>
</html>
