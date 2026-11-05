<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Anime Live Animation</title>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background: #101b27;
  overflow: hidden;
}

.scene {
  position: relative;
  width: 100%;
  max-width: 500px;
  height: 100vh;
  overflow: hidden;
  background: #c5e9b7;
}

.photo {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center;
  animation: hidup 8s ease-in-out infinite;
}

/* Cahaya matahari */
.sunlight {
  position: absolute;
  inset: 0;
  pointer-events: none;
  background: linear-gradient(
    115deg,
    rgba(255, 255, 200, 0.3),
    transparent 45%,
    rgba(255, 255, 255, 0.1)
  );
  animation: cahaya 5s ease-in-out infinite alternate;
}

/* Efek rambut dan gerakan lembut */
@keyframes hidup {
  0%, 100% {
    transform: scale(1.02) translateY(0);
  }

  50% {
    transform: scale(1.06) translateY(-5px);
  }
}

/* Cahaya berkilau */
@keyframes cahaya {
  0% {
    opacity: 0.3;
    filter: brightness(1);
  }

  100% {
    opacity: 0.9;
    filter: brightness(1.15);
  }
}

/* Bintik cahaya */
.sparkle {
  position: absolute;
  width: 7px;
  height: 7px;
  border-radius: 50%;
  background: #fffbd0;
  box-shadow: 0 0 15px 5px #fff3a0;
  animation: berkilau 3s ease-in-out infinite;
}

.sparkle:nth-child(2) {
  top: 25%;
  left: 20%;
  animation-delay: 1s;
}

.sparkle:nth-child(3) {
  top: 50%;
  right: 15%;
  animation-delay: 2s;
}

.sparkle:nth-child(4) {
  top: 70%;
  left: 30%;
  animation-delay: 0.5s;
}

@keyframes berkilau {
  0%, 100% {
    opacity: 0;
    transform: scale(0.5);
  }

  50% {
    opacity: 1;
    transform: scale(1.4);
  }
}
</style>
</head>

<body>

<div class="scene">

  <img
    src="punya gua.png"
    class="photo"
    alt="Ilustrasi anime"
  >

  <div class="sunlight"></div>

  <div class="sparkle"></div>
  <div class="sparkle"></div>
  <div class="sparkle"></div>
  <div class="sparkle"></div>

</div>

</body>
</html>
