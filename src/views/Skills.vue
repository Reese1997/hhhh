<template>
<br><h3>Skills:</h3><br>

  <div class="skill-bars">
  <div class="bar">
    <div class="info">
      <span>HTML</span>
    </div>
    <div class="progress-line html">
      <span></span>
    </div>
  </div>
  <div class="bar">
    <div class="info">
      <span>CSS</span>
    </div>
    <div class="progress-line css">
      <span></span>
    </div>
  </div>
  <div class="bar">
    <div class="info">
      <span>JavaScript</span>
    </div>
    <div class="progress-line javascript">
      <span></span>
    </div>
  </div>
  <div class="bar">
    <div class="info">
      <span>NodeJS</span>
    </div>
    <div class="progress-line nodejs">
      <span></span>
    </div>
  </div>
   <div class="bar">
    <div class="info">
      <span>ExpressJS</span>
    </div>
    <div class="progress-line css">
      <span></span>
    </div>
  </div>
  <div class="bar">
    <div class="info">
      <span>MongoDB</span>
    </div>
    <div class="progress-line css">
      <span></span>
    </div>
  </div>
  <div class="bar">
    <div class="info">
      <span>MySQL</span>
    </div>
    <div class="progress-line mysql">
      <span></span>
    </div>
  </div>
</div>

<section>
  "Design is not just what it looks like and feels like. 
  Design is how it works. - Steve Jobs"
</section>

</template>

<script>
export default {};
</script>

<style scoped>
h3 {
  text-align: center;
}
body {
  
  margin: 0;
  padding: 0;
  background-color: rgb(255, 236, 236);
}

@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@200;300;400;500;600;700&display=swap');
*{
  
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Poppins', sans-serif;
}
html,body{
  display: grid;
  height: 100%;
  place-items: center;
  
}
::selection{
  color: #fff;
  background: #7ca9d3;
}
.skill-bars{
  padding: 100px 137px;
  padding-left: 130px;
  padding-right: 130px;
  padding-top: 10%;
  width: 800px;
  background: #fff;
  box-shadow: 5px 5px 20px rgba(0,0,0,0.2);
  border-radius: 10px;
}
.skill-bars .bar{
  margin: 20px 0;
  

}
.skill-bars .bar:first-child{
  margin-top: 0px;
  
}
.skill-bars .bar .info{
  margin-bottom: 5px;
  
}
.skill-bars .bar .info span{
  font-weight: 500;
  font-size: 19px;
  opacity: 0;
  animation: showText 0.5s 1s linear forwards;
}
@keyframes showText {
  100%{
    opacity: 1;
  }
}
.skill-bars .bar .progress-line{
  height: 10px;
  width: 100%;
  
  background: #f0f0f0;
  position: relative;
  transform: scaleX(0);
  transform-origin: left;
  border-radius: 10px;
  box-shadow: inset 0 1px 1px rgba(0,0,0,0.05),
              0 1px rgba(255,255,255,0.8);
  animation: animate 1s cubic-bezier(1,0,0.5,1) forwards;
}
@keyframes animate {
  100%{
    transform: scaleX(1);
  }
}
.bar .progress-line span{
  height: 100%;
  
  position: absolute;
  border-radius: 10px;
  transform: scaleX(0);
  transform-origin: left;
  background: rgb(15, 112, 202);
  animation: animate 1s 1s cubic-bezier(1,0,0.5,1) forwards;
}
.bar .progress-line.html span{
  width: 90%;
}
.bar .progress-line.css span{
  width: 90%;
}
.bar .progress-line.javascript span{
  width: 85%;
}
.bar .progress-line.nodejs span{
  width: 97%;
}
.bar .progress-line.expressjs span{
  width: 95%;
}
.bar .progress-line.mongodb span{
  width: 95%;
}
.bar .progress-line.mysql span{
  width: 95%;
}
.progress-line span::before{
  position: absolute;
  content: "";
  top: -10px;
  right: 0;
  height: 0;
  width: 0;
  border: 7px solid transparent;
  border-bottom-width: 0px;
  border-right-width: 0px;
  border-top-color: #000;
  opacity: 0;
  animation: showText2 0.5s 1.5s linear forwards;
}
.progress-line span::after{
  position: absolute;
  top: -28px;
  right: 0;
  font-weight: 500;
  background: #000;
  color: #fff;
  padding: 1px 8px;
  font-size: 12px;
  border-radius: 3px;
  opacity: 0;
  animation: showText2 0.5s 1.5s linear forwards;
}
@keyframes showText2 {
  100%{
    opacity: 1;
  }
}
.progress-line.html span::after{
  content: "90%";
}
.progress-line.css span::after{
  content: "90%";
}
.progress-line.javascript span::after{
  content: "85%";
}
.progress-line.nodejs span::after{
  content: "90%";
}
.bar .progress-line.expressjs span{
  width: "95%";
}
.bar .progress-line.mongodb span{
  width: "95%";
}
.progress-line.mysql span::after{
  content: "95%";
}

@media screen {
  
}
</style>
