+++
date = '2026-02-21T17:34:06+08:00'
draft = false
title = '亲爱的小源 ✨'
+++
<div id="love_time" style="text-align: center; font-size: 1.2rem; color: #ff69b4; font-weight: bold; margin: 20px 0;"></div>

> "如果你不曾出现，我大概还在这空荡的世界里漫无目的地流浪。"

<script>
    var start = new Date("2022-10-27T00:00:00"); // 这里改成你们认识/在一起的日期
    function updateTime() {
        var now = new Date();
        var diff = now - start;
        var days = Math.floor(diff / (1000 * 60 * 60 * 24));
        var hours = Math.floor((diff / (1000 * 60 * 60)) % 24);
        var mins = Math.floor((diff / (1000 * 60)) % 60);
        var secs = Math.floor((diff / 1000) % 60);
        document.getElementById('love_time').innerHTML = "我们已经相识 " + days + " 天 " + hours + " 小时 " + mins + " 分 " + secs + " 秒";
    }
    setInterval(updateTime, 1000);
</script>

### 💌 我想对你说
<h2 id="typing" style="color: #555; line-height: 1.6;"></h2>

<script>
    var i = 0;
    var txt = '贝贝我们已经在一起好久啦，我还特地弄了个时间放在上面，本来是下午的突发奇想，想要搭建一个自己的博客，突然就想要用程序员的方式向你表达一下爱意，在一起的这段时间，我感觉我们俩个都变得比原来更好了，在你累的时候我会给你讲故事，在你吐槽傻逼客户的时候我会无条件站在你这边，在你情绪低落的时候我会给你托底，晚上我们可以一起说小话，下午可以一起吃cumei看炭治郎，中午可以一起烧菜做一顿难吃的饭，早上可以一起睡到太阳晒屁股，跟你在一起的每一天都是特别特别开心有意思的一天！我们现在已经有快快啦，我们正在朝着我们理想中的生活前进！我们一起努力，一起奋斗，一起享受，好耶！';
    var speed = 150; // 打字速度（毫秒）

    function typeWriter() {
        if (i < txt.length) {
            document.getElementById("typing").innerHTML += txt.charAt(i);
            i++;
            setTimeout(typeWriter, speed);
        }
    }
    window.onload = typeWriter;
</script>

<div class="slideshow-container">
    <div class="mySlides fade">
        <img src="/images/cx1.jpg" style="width:100%; border-radius: 15px;">
    </div>
    <div class="mySlides fade">
        <img src="/images/cx2.jpg" style="width:100%; border-radius: 15px;">
    </div>
    <div class="mySlides fade">
        <img src="/images/cx3.jpg" style="width:100%; border-radius: 15px;">
    </div>
    <div class="mySlides fade">
        <img src="/images/byz.jpg" style="width:100%; border-radius: 15px;">
    </div>
    <div class="mySlides fade">
        <img src="/images/cx4.jpg" style="width:100%; border-radius: 15px;">
    </div>
    <div class="mySlides fade">
        <img src="/images/yyh.jpg" style="width:100%; border-radius: 15px;">
    </div>
    <div class="mySlides fade">
        <img src="/images/flower.jpg" style="width:100%; border-radius: 15px;">
    </div>
</div>

<style>
.slideshow-container {
    max-width: 500px;
    position: relative;
    margin: auto;
    overflow: hidden;
}

.mySlides {
    display: none;
}

.mySlides img {
    height: 350px;
    object-fit: cover; /* 保证不同尺寸的照片都能整齐显示 */
}

/* 文字样式 */
.text {
    color: #ff69b4;
    font-size: 18px;
    padding: 8px 12px;
    position: absolute;
    bottom: 20px;
    width: 100%;
    text-align: center;
    background-color: rgba(255, 255, 255, 0.6);
    font-weight: bold;
}

/* 动画效果：淡入 */
.fade {
    animation-name: fade;
    animation-duration: 1.5s;
}

@keyframes fade {
    from {opacity: .4} 
    to {opacity: 1}
}
</style>

<script>
let slideIndex = 0;
showSlides();

function showSlides() {
    let i;
    let slides = document.getElementsByClassName("mySlides");
    for (i = 0; i < slides.length; i++) {
        slides[i].style.display = "none";  
    }
    slideIndex++;
    if (slideIndex > slides.length) {slideIndex = 1}    
    slides[slideIndex-1].style.display = "block";  
    setTimeout(showSlides, 3000); // 每3秒自动切换一张
}
</script>

<p align="center">
  <font color="#ff69b4" size="5">❤ 永远喜欢你！！！ ❤</font>
</p>

<script>
(function () {
  var hearts = [];
  window.requestAnimationFrame = (function () {
    return window.requestAnimationFrame || window.webkitRequestAnimationFrame || window.mozRequestAnimationFrame || window.oRequestAnimationFrame || window.msRequestAnimationFrame ||
      function (callback) { setTimeout(callback, 1000 / 60); }
  })();
  init();
  function init() {
    css(".heart{width: 10px;height: 10px;position: fixed;background: #f00;transform: rotate(45deg);-webkit-transform: rotate(45deg);-moz-transform: rotate(45deg);}.heart:after,.heart:before{content: '';width: inherit;height: inherit;background: inherit;border-radius: 50%;position: absolute;}.heart:after{top: -5px;}.heart:before{left: -5px;}");
    attachEvent();
    gameloop();
  }
  function gameloop() {
    for (var i = 0; i < hearts.length; i++) {
      if (hearts[i].alpha <= 0) {
        document.body.removeChild(hearts[i].el);
        hearts.splice(i, 1);
        continue;
      }
      hearts[i].y--;
      hearts[i].scale += 0.004;
      hearts[i].alpha -= 0.013;
      hearts[i].el.style.cssText = "left:" + hearts[i].x + "px;top:" + hearts[i].y + "px;opacity:" + hearts[i].alpha + ";transform:scale(" + hearts[i].scale + ") rotate(45deg);background:" + hearts[i].color;
    }
    requestAnimationFrame(gameloop);
  }
  function attachEvent() {
    var old = typeof window.onclick === "function" && window.onclick;
    window.onclick = function (event) {
      old && old();
      createHeart(event);
    };
  }
  function createHeart(event) {
    var d = document.createElement("div");
    d.className = "heart";
    hearts.push({
      el: d,
      x: event.clientX - 5,
      y: event.clientY - 5,
      scale: 1,
      alpha: 1,
      color: randomColor()
    });
    document.body.appendChild(d);
  }
  function css(css) {
    var style = document.createElement("style");
    style.type = "text/css";
    try { style.appendChild(document.createTextNode(css)); }
    catch (ex) { style.styleSheet.cssText = css; }
    document.getElementsByTagName('head')[0].appendChild(style);
  }
  function randomColor() {
    return "rgb(" + (~~(Math.random() * 255)) + "," + (~~(Math.random() * 255)) + "," + (~~(Math.random() * 255)) + ")";
  }
})();
</script>

<style>
  /* 整个网页范围内生效 */
  body, a, button, img {
    cursor: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="%23ff69b4"><path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5 2 5.42 4.42 3 7.5 3c1.74 0 3.41.81 4.5 2.09C13.09 3.81 14.76 3 16.5 3 19.58 3 22 5.42 22 8.5c0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/></svg>'), auto !important;
  }
</style>
