# JavaScript Visual Effect

This project is a fun and chaotic JavaScript visual effect that creates a full-screen animation with dynamically changing colors and transformations. The effect is triggered immediately when executed and can also enter fullscreen mode on click.

## Features
- Generates a screen filled with color-changing divs.
- Random transformations and animations.
- Automatically scrolls to the top periodically.
- Click anywhere to enter fullscreen mode.
- Provides a colorful and dynamic visual experience with minimal code.

## Installation & Usage
1. **Copy the following minified JavaScript code:**

   ```javascript
   javascript:(function(){function g(){let color="#"+Math.floor(Math.random()*16777215).toString(16).padStart(6,'0');console.log("Generated color:",color);return color;}function r(m){let num=Math.floor(Math.random()*m)+1;console.log("Generated random number:",num);return num;}function f(e){console.log("Attempting fullscreen mode");if(e.requestFullscreen){e.requestFullscreen();}else if(e.mozRequestFullScreen){e.mozRequestFullScreen();}else if(e.webkitRequestFullscreen){e.webkitRequestFullscreen();}else if(e.msRequestFullscreen){e.msRequestFullscreen();}}document.head.innerHTML='<style>*{margin:0;padding:0;overflow:hidden}div{width:100%;height:1px;position:relative;z-index:1}</style>';document.body.innerHTML='';let h=window.screen.availHeight;console.log("Screen height:",h);for(let i=0;i<=h;i++){let d=document.createElement("div");d.id="b"+i;d.style.backgroundColor=g();document.body.appendChild(d);}console.log("Div elements created");document.body.addEventListener("click",function(){console.log("Body clicked");f(document.documentElement);});setInterval(()=>{console.log("Updating colors and transformations");for(let i=0;i<10;i++){let d=document.getElementById("b"+r(h));if(d){console.log("Updating div:",d.id);d.style.backgroundColor=g();d.style.height=r(4)+"px";}}document.body.style.backgroundColor=g();document.body.style.transform=r(256)>128?`scale(3) rotate(${r(35)}deg)`:"rotate(0deg) scale(1)";},100);setInterval(()=>{console.log("Scrolling to top");window.scrollTo(0,0);},500);})();
2. **Add it as a bookmark and run.**
&nbsp;
<div align="center">
  Happy Pranking!
</div>
