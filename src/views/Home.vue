<template>
  <!-- <img src="@/assets/bgblck.jpg" alt="" /> -->
  <div class="background animate__animated animate__zoomIn">
    <h1>Reese Simone Abrahams</h1>
    <h2>I am <span id="text"></span></h2>
    <div class="row justify-content-center"></div>
    <a
      href="https://codepen.io/reese1997 /"
      class="fab fa-codepen"
      target="_blank"
      style="font-size: 70px; color: #222"
    ></a>
    <a
      href="https://github.com/Reese1997/"
      class="fab fa-github"
      style="font-size: 70px; color: #222"
    ></a>
    <a
      href="https://www.linkedin.com/in/reese-abrahams-19525415b/"
      class="fa fa-linkedin"
    ></a>
  </div>
</template>

<script>
export default {};
const sentences = [
  "Reese",
  "Front-End Developer",
  "Software Developer",
  "Creative and logical",
];

function waitForMs(ms) {
  return new Promise((resolve) => setTimeout(resolve, ms));
}

async function typeSentence(sentence, element, delay = 100) {
  const letters = sentence.split("");
  let i = 0;
  while (i < letters.length) {
    await waitForMs(delay);
    document.querySelector(element).append(letters[i]);
    i++;
  }
}

async function deleteSentence(element) {
  const sentence = document.querySelector(element).innerHTML;
  const letters = sentence.split("");
  while (letters.length > 0) {
    await waitForMs(100);
    letters.pop();
    document.querySelector(element).innerHTML = letters.join("");
  }
}

async function sentenceLoop(sentenceList, element) {
  let i = 0;
  while (true) {
    await typeSentence(sentenceList[i], element);
    await waitForMs(1500);
    await deleteSentence(element);
    await waitForMs(500);
    i++;
    if (i >= sentenceList.length) {
      i = 0;
    }
  }
}

sentenceLoop(sentences, "#text");

</script>

<style scoped>
.background {
  background-image: url("../assets/aboutr.jpeg");
  
  background-size: 300px 300px;
  height: 100vh;
  color: rgb(8, 8, 8);
  background-position: fixed;
  background-size: cover;
  background-repeat: none;
}

header {
  display: flex;
}

.landing-text,
.landing-img {
  width: 50%;
}

.landing-text {
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 30px;
}

.landing-img {
  max-height: 100vh;
  object-fit: cover;
}

@media screen and (max-width: 500px) {
  header {
    flex-direction: column;
  }
  .landing-text,
  .landing-img {
    width: 100%;
  }
}

.home {
  padding: 90px;
  border-radius: 10px;
  margin: 10px auto;
  max-width: 600px;
  cursor: pointer;
  color: rgb(14, 13, 13);
}
h1 {
  padding-top: 25%;
  padding-left: 80px;
  text-align: center;
  color: rgb(245, 245, 253);
  font-size: 60px;
}
h2 {
  text-align: center;
  color: rgb(255, 247, 247);
  font-size: 50px;
}

.home a {
  text-decoration: none;
}

#text {
  position: relative;
}

#text:after {
  width: 3px;
  height: 100%;
  background: black;
  position: absolute;
  animation: blink 1s infinite;
}

@keyframes blink {
  0%,
  49% {
    background: rgb(252, 248, 248);
  }
  50%,
  100% {
    background: rgb(255, 252, 252);
  }
}

.fa-codepen:before {
  padding-left: 700px;
}

.fa:hover {
}
</style>
