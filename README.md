# Waifu

<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sistine Fibel | Anime Profile</title>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  background: #080808;
  color: white;
  font-family: Arial, sans-serif;
}

header {
  padding: 22px 8%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  border-bottom: 1px solid #292929;
}

.logo {
  font-size: 22px;
  font-weight: bold;
  letter-spacing: 3px;
}

.logo span {
  color: #999;
}

nav a {
  color: #aaa;
  text-decoration: none;
  margin-left: 20px;
}

.hero {
  min-height: 85vh;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 60px 10%;
  gap: 30px;
  overflow: hidden;
}

.intro {
  max-width: 500px;
}

.intro small {
  color: #aaa;
  letter-spacing: 4px;
}

h1 {
  font-size: clamp(40px, 7vw, 75px);
  margin: 20px 0;
}

h1 span {
  color: #888;
}

p {
  color: #aaa;
  line-height: 1.8;
}

.btn {
  display: inline-block;
  margin-top: 25px;
  padding: 13px 25px;
  background: white;
  color: black;
  text-decoration: none;
  border-radius: 6px;
  font-weight: bold;
}

.character {
  position: relative;
  width: 320px;
  height: 420px;
  flex-shrink: 0;
  animation: float 3s ease-in-out infinite;
}

.character img {
  width: 100%;
  height: 100%;
  object-fit: contain;
  filter: drop-shadow(0 0 25px #777);
  position: relative;
  z-index: 2;
}

.magic {
  position: absolute;
  width: 12px;
  height: 12px;
  background: #d9e8ff;
  border-radius: 50%;
  box-shadow: 0 0 20px #8abfff;
  animation: sparkle 2s infinite;
}

.magic:nth-child(2) {
  top: 20%;
  left: 10%;
}

.magic:nth-child(3) {
  top: 50%;
  right: 5%;
  animation-delay: .7s;
}

.magic:nth-child(4) {
  bottom: 20%;
  left: 15%;
  animation-delay: 1s;
}

@keyframes float {
  0%, 100% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(-20px);
  }
}

@keyframes sparkle {
  0%, 100% {
    opacity: .2;
    transform: scale(.5);
  }
  50% {
    opacity: 1;
    transform: scale(1.5);
  }
}

section {
  padding: 60px 10%;
}

h2 {
  margin-bottom: 25px;
}

.card {
  background: #141414;
  border: 1px solid #292929;
  border-radius: 12px;
  padding: 25px;
}

.music {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 20px;
  flex-wrap: wrap;
}

button {
  background: white;
  color: black;
  border: none;
  padding: 12px 24px;
  border-radius: 30px;
  cursor: pointer;
  font-weight: bold;
}

footer {
  text-align: center;
  padding: 25px;
  color: #666;
  border-top: 1px solid #292929;
}

@media(max-width: 700px) {
  header {
    flex-direction: column;
    gap: 20px;
  }

  .hero {
    flex-direction: column;
    text-align: center;
  }

  .character {
    width: 270px;
    height: 350px;
  }
}
</style>
</head>

<body>

<header>
  <div class="logo">SISTINE<span>.</span></div>
  <nav>
    <a href="#home">Home</a>
    <a href="#profil">Profil</a>
    <a href="#musik">Musik</a>
  </nav>
</header>

<div class="hero" id="home">

  <div class="intro">
    <small>ANIME CHARACTER PROFILE</small>

    <h1>SISTINE<br><span>FIBEL.</span></h1>

    <p>
      The White Cat of Alzano Imperial Magic Academy.
      A beautiful magician with silver hair and
      emerald eyes.
    </p>

    <a href="#profil" class="btn">
      Explore Profile ↘
    </a>
  </div>

  <div class="character">
    <img src="my.jpg" alt="Sistine Fibel">

    <div class="magic"></div>
    <div class="magic"></div>
    <div class="magic"></div>
  </div>

</div>

<section id="profil">
  <h2>About Sistine</h2>

  <div class="card">
    <p>Nama: Sistine Fibel</p>
    <p>Julukan: White Cat</p>
    <p>Rambut: Perak</p>
    <p>Mata: Hijau</p>
    <p>Anime: Akashic Records of Bastard Magic Instructor</p>
  </div>
</section>

<section id="musik">
  <h2>Anime Music</h2>

  <div class="card music">
    <div>
      <h3>🎧 Favorite Music</h3>
      <p>Putar musik favoritmu.</p>
    </div>

    <button id="playBtn" onclick="toggleMusic()">
      ▶ Play Music
    </button>

    <audio id="audio" loop>
      <source src="18.mp3" type="audio/mpeg">
    </audio>
  </div>
</section>

<footer>
  © 2026 | Sistine Fibel Anime Profile
</footer>

<script>
const audio = document.getElementById("audio");
const btn = document.getElementById("playBtn");

function toggleMusic() {
  if (audio.paused) {
    audio.play().then(() => {
      btn.textContent = "❚❚ Pause Music";
    }).catch(() => {
      alert("Pastikan file music.mp3 tersedia.");
    });
  } else {
    audio.pause();
    btn.textContent = "▶ Play Music";
  }
}
</script>

</body>
</html>
