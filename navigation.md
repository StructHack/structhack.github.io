---
layout: default
title: Hi
permalink: /hi/
---

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>I Love You</title>
  <style>
    body {
      background: radial-gradient(circle, #ffccd5 0%, #ff6f91 100%);
      color: #fff0f5;
      text-align: center;
      font-family: 'Comic Sans MS', cursive, sans-serif;
      overflow: hidden;
      z-index:111 !important;
      width:100%;
      
    }

    h1 {
      font-size: 3em;
      margin-top: 20px;
      text-shadow: 3px 3px 8px #ff007f;
    }

    .love-text {
      position: absolute;
      font-size: 2em;
      animation: float 10s linear infinite;
      opacity: 0.6;
      text-shadow: 2px 2px 6px #ff1493;
    }

    @keyframes float {
      0% {
        transform: translateY(100vh) rotate(0deg);
        opacity: 0;
      }
      50% {
        opacity: 1;
      }
      100% {
        transform: translateY(-100vh) rotate(360deg);
        opacity: 0;
      }
    }

    .cat {
      width: 160px;
      position: absolute;
      animation: dance 0.8s infinite alternate ease-in-out;
      filter: drop-shadow(4px 4px 6px hotpink);
    }

    @keyframes dance {
      0% { transform: translateY(0) rotate(-15deg); }
      100% { transform: translateY(-25px) rotate(15deg); }
    }

    .bubble-heart {
      position: absolute;
      width: 30px;
      height: 30px;
      background-color: #ff69b4;
      clip-path: path("M15,30 C-10,10 0,-10 15,5 C30,-10 40,10 15,30 Z");
      animation: pop 6s infinite ease-in-out;
      opacity: 0.5;
    }

    @keyframes pop {
      0% { transform: scale(0.5) translateY(0); opacity: 0.6; }
      50% { transform: scale(1.2) translateY(-100px); opacity: 1; }
      100% { transform: scale(0.8) translateY(-200px); opacity: 0; }
    }

    nav {
      position: absolute;
      top: 10px;
      right: 20px;
    }

    nav a {
      background: white;
      padding: 5px 10px;
      color: red;
      border-radius: 10px;
      font-weight: bold;
      text-decoration: none;
      font-family: 'Comic Sans MS', cursive;
    }

  </style>
</head>
<body>
  <nav>
    <a href="/hi/">Hi Page</a>
  </nav>

  <h1>I Love You</h1>

  <img alt="cat lol" src="https://media.giphy.com/media/JIX9t2j0ZTN9S/giphy.gif" class="cat" style="top: 20%; left: 10%;">
  <img alt="cat lol" src="https://media.giphy.com/media/JIX9t2j0ZTN9S/giphy.gif" class="cat" style="top: 40%; left: 40%;">
  <img alt="cat lol" src="https://media.giphy.com/media/JIX9t2j0ZTN9S/giphy.gif" class="cat" style="top: 30%; left: 70%;">

  <script>
    // Floating "I ♥ You" texts
    for (let i = 0; i < 50; i++) {
      const love = document.createElement('div');
      love.className = 'love-text';
      love.innerText = 'I ♥ You';
      love.style.left = Math.random() * 100 + 'vw';
      love.style.top = Math.random() * 100 + 'vh';
      love.style.fontSize = (Math.random() * 1.5 + 1) + 'em';
      love.style.animationDuration = (Math.random() * 5 + 5) + 's';
      love.style.color = Math.random() > 0.5 ? 'hotpink' : 'deeppink';
      document.body.appendChild(love);
    }

    // Bubble hearts floating
    for (let i = 0; i < 30; i++) {
      const heart = document.createElement('div');
      heart.className = 'bubble-heart';
      heart.style.left = Math.random() * 100 + 'vw';
      heart.style.bottom = '0';
      heart.style.animationDelay = Math.random() * 5 + 's';
      heart.style.opacity = Math.random();
      document.body.appendChild(heart);
    }
  </script>
</body>
</html>
