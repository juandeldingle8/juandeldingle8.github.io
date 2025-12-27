<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>player.exe</title>
<link rel="icon" href="winxp.png">

<style>
body {
  margin: 0;
  height: 100vh;
  background: linear-gradient(#3a6ea5, #0a246a);
  font-family: Tahoma, Verdana, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden;
}

/* ===== XP WINDOW ===== */
.window {
  width: 700px;
  background: #ece9d8;
  border: 2px solid #000;
  box-shadow: 8px 8px 0 #000;
}

/* TITLE BAR */
.title {
  background: linear-gradient(to right, #0a246a, #3a6ea5);
  color: white;
  padding: 6px;
  font-weight: bold;
}

/* CONTENT */
.content {
  display: flex;
}

/* VIDEO */
.video-wrap {
  position: relative;
  width: 480px;
  background: black;
}

video {
  width: 100%;
  filter: contrast(1.2) saturate(0.8);
}

/* VHS SCANLINES */
.video-wrap::after {
  content: "";
  position: absolute;
  inset: 0;
  background: repeating-linear-gradient(
    to bottom,
    rgba(255,255,255,0.05),
    rgba(255,255,255,0.05) 1px,
    transparent 2px
  );
  pointer-events: none;
}

/* VISUALIZER */
canvas {
  width: 100%;
  height: 80px;
  background: black;
}

/* PLAYLIST */
.playlist {
  width: 220px;
  border-left: 2px inset #808080;
  background: #c0c0c0;
  padding: 6px;
}

.track {
  background: #ece9d8;
  border: 2px outset #fff;
  padding: 4px;
  margin-bottom: 6px;
  cursor: pointer;
  font-size: 13px;
}

.track:hover {
  background: #0a246a;
  color: white;
}
</style>
</head>

<body>

<div class="window">
  <div class="title">Windows Media Player — deldingle</div>

  <div class="content">
    <div class="video-wrap">
      <video id="video" autoplay loop playsinline>
        <source src="videos/video1.mp4" type="video/mp4">
      </video>
      <canvas id="viz"></canvas>
    </div>

    <div class="playlist">
      <div class="track" data-src="videos/video1.mp4">📼 video_01.mp4</div>
      <div class="track" data-src="videos/video2.mp4">📼 video_02.mp4</div>
      <div class="track" data-src="videos/video3.mp4">📼 video_03.mp4</div>
    </div>
  </div>
</div>

<script>
const video = document.getElementById("video");
const canvas = document.getElementById("viz");
const ctx = canvas.getContext("2d");

canvas.width = 480;
canvas.height = 80;

// Audio Context
const audioCtx = new (window.AudioContext || window.webkitAudioContext)();
const source = audioCtx.createMediaElementSource(video);
const analyser = audioCtx.createAnalyser();
analyser.fftSize = 64;

source.connect(analyser);
analyser.connect(audioCtx.destination);

const data = new Uint8Array(analyser.frequencyBinCount);

function draw() {
  requestAnimationFrame(draw);
  analyser.getByteFrequencyData(data);
  ctx.clearRect(0, 0, canvas.width, canvas.height);

  const barWidth = canvas.width / data.length;
  data.forEach((v, i) => {
    const h = v / 2;
    ctx.fillStyle = "lime";
    ctx.fillRect(i * barWidth, canvas.height - h, barWidth - 2, h);
  });
}

draw();

// Playlist
document.querySelectorAll(".track").forEach(track => {
  track.onclick = () => {
    video.src = track.dataset.src;
    video.play();
  };
});

// Force audio context resume
document.body.addEventListener("click", () => audioCtx.resume(), { once: true });

// Try fullscreen
document.documentElement.requestFullscreen?.();
</script>

</body>
</html>
