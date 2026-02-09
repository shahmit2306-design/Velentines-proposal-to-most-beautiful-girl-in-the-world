# Velentines-proposal-to-most-beautiful-girl-in-the-world
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Valentine ❤️</title>

<style>
  body {
    margin: 0;
    font-family: "Times New Roman", Times, serif;
    background: #ffeaf1;
    min-height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    overflow-x: hidden;
  }

  .container {
    padding: 24px;
  }

  /* BIG EMOJI ON TOP */
  .top-emoji {
    font-size: 5rem;
    margin-bottom: 14px;
  }

  h1 {
    font-size: 2.3rem;
    line-height: 1.5;
    margin: 0 0 28px 0;
  }

  .buttons {
    display: flex;
    justify-content: center;
    gap: 24px;
    margin-bottom: 32px;
  }

  .btn {
    padding: 14px 38px;
    font-size: 1.4rem;
    border-radius: 16px;
    border: 3px solid #ff6fa8;
    background: white;
    cursor: pointer;
    font-weight: bold;
    user-select: none;
  }

  #yes {
    color: #ff3e8e;
  }

  #no {
    color: black;
    position: relative;
  }

  /* NO button movement */
  @keyframes runAway {
    0%   { transform: translate(0,0); }
    25%  { transform: translate(40vw, -20vh); }
    50%  { transform: translate(-40vw, 25vh); }
    75%  { transform: translate(30vw, 35vh); }
    100% { transform: translate(0,0); }
  }

  .floating {
    animation: runAway 3s linear infinite;
  }

  .bottom-text {
    font-size: 1.1rem;
  }

  /* YAY SCREEN */
  .hidden {
    display: none;
  }

  #yay h1 {
    font-size: 3.2rem;
    color: #ff3e8e;
  }

  #yay img {
    margin-top: 20px;
    max-width: 90%;
    border-radius: 18px;
  }

  /* HEARTS */
  .heart {
    position: fixed;
    bottom: -20px;
    font-size: 1.8rem;
    animation: floatUp 4s ease-in forwards;
    pointer-events: none;
  }

  @keyframes floatUp {
    to {
      transform: translateY(-120vh) scale(1.5);
      opacity: 0;
    }
  }
</style>
</head>

<body>

<div id="ask" class="container">
  <div class="top-emoji">💖</div>

  <h1>❤️ Mokshi, will you be my velentine? ❤️</h1>

  <div class="buttons">
    <div id="yes" class="btn">Yes ❤️</div>
    <div id="no" class="btn">No</div>
  </div>

  <div class="bottom-text">
    Dum hai to No click ker ke dikha ❤️
  </div>
</div>

<div id="yay" class="container hidden">
  <h1>Yay! ❤️</h1>
  <img src="https://github.com/shahmit2306-design/Velentines-proposal-to-most-beautiful-girl-in-the-world/blob/main/WhatsApp%20Video%202026-02-09%20at%202.48.46%20PM.mp4" alt="Yay GIF">
</div>

<script>
  const yesBtn = document.getElementById("yes");
  const noBtn = document.getElementById("no");
  const ask = document.getElementById("ask");
  const yay = document.getElementById("yay");

  function createHeart() {
    const heart = document.createElement("div");
    heart.className = "heart";
    heart.innerText = "❤️";
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.fontSize = (Math.random() * 18 + 18) + "px";
    document.body.appendChild(heart);
    setTimeout(() => heart.remove(), 4000);
  }

  yesBtn.onclick = () => {
    ask.classList.add("hidden");
    yay.classList.remove("hidden");
    setInterval(createHeart, 250);
  };

  noBtn.onclick = () => {
    noBtn.classList.add("floating");
  };
</script>

</body>
</html>
