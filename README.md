love-letter/
│
├── index.html         ← home page
├── letter.html        ← main love letter
├── memories.html      ← gallery
├── countdown.html     ← timer page
├── style.css          ← shared styles
└── herphoto.jpg       ← your uploaded image
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>For My Love 💌</title>
<link rel="stylesheet" href="style.css">
<script src="hearts.js" defer></script>
</head>
<body class="home">
  <div class="center fade-in">
    <h1 class="typewriter">Hey, my love 💕</h1>
    <p>Something special is waiting for you...</p>
    <button onclick="location.href='letter.html'">Open it 💌</button>
  </div>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>My Love Letter 💖</title>
<link rel="stylesheet" href="style.css">
<script src="hearts.js" defer></script>
</head>
<body class="letter">
  <!-- Background Song -->
  <iframe width="0" height="0"
    src="https://www.youtube.com/embed/CwGbMYLjIpQ?autoplay=1&loop=1&playlist=CwGbMYLjIpQ"
    frameborder="0" allow="autoplay; encrypted-media"></iframe>

  <div class="center fade-in">
    <h1>To My Dearest 💗</h1>
    <img src="herphoto.jpg" alt="Her beautiful smile">
    <p class="typewriter">Every day apart makes me love you more. I made this so you never forget how special you are to me 💗</p>
    <button onclick="location.href='memories.html'">Next ➡</button>
  </div>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Our Memories 📸</title>
<link rel="stylesheet" href="style.css">
<script src="hearts.js" defer></script>
</head>
<body class="memories">
  <div class="center fade-in">
    <h1>Some of Our Favorite Moments 💕</h1>
    <div class="gallery">
      <img src="herphoto.jpg" alt="Memory 1">
      <img src="herphoto.jpg" alt="Memory 2">
      <img src="herphoto.jpg" alt="Memory 3">
    </div>
    <button onclick="location.href='countdown.html'">Next ➡</button>
  </div>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Countdown ⏳</title>
<link rel="stylesheet" href="style.css">
<script src="hearts.js" defer></script>
</head>
<body class="countdown">
  <div class="center fade-in">
    <h1>Until I See You Again 💞</h1>
    <h2 id="timer"></h2>
    <button onclick="location.href='index.html'">Back Home 🏠</button>
  </div>

  <script>
    const targetDate = new Date("2025-12-13T00:00:00"); 
    const timer = document.getElementById("timer");
    setInterval(() => {
      const diff = targetDate - new Date();
      const days = Math.floor(diff / (1000*60*60*24));
      const hours = Math.floor((diff / (1000*60*60)) % 24);
      const mins = Math.floor((diff / (1000*60)) % 60);
      timer.textContent = ${days} days ${hours} hrs ${mins} mins;
    }, 1000);
  </script>
</body>
</html>
