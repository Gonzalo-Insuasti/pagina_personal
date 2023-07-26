<template>
  <div id="app">
    <PresentationPage />
  </div>
</template>

<script setup>
import PresentationPage from './components/PresentationPage.vue';

</script>

<style>
body, html, #app{
  margin: 0px;
}
h1 {
  font-family:sans-serif;
  font-size: 2.2vw;
display: inline-block;
position: relative;
}
h1::after,h1::before{
  content: '';
  position: absolute;
  width: 150px;
  height: 3px;
  background-color: currentColor;
  top: 0.8em;
  transform: scale(0);
  transition: all .2s ease-in;
}
h1:hover::after, h1:hover::before{
  transform: scale(1);
}
h1::after{
  right: -165px;
}
h1::before{
  left: -165px;
}
h2 {
  font-family:sans-serif;
  font-size: 2.2vw;
display: inline-block;
position: relative;
}
h2::after,h2::before{
  content: '';
  position: absolute;
  width: 300px;
  height: 3px;
  background-image: linear-gradient(
      150deg,
      #9500ff,
      #09f,
      #00DDFF);
  top: 0.8em;
}
h2::after{
  right: -305px;
}
h2::before{
  left: -305px;
}
</style>
