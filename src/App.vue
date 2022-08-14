<template>
  <div id="app">
    <router-view />
  </div>
</template>

<style>
@import url(@/assets/style/main.css);
@import url(@/assets/responsive/responsive.css);
@font-face {
  font-family: robotoRegular;
  src: url(@/assets/fonts/Roboto-Regular.ttf);
}
@font-face {
  font-family: robotoBold;
  src: url(@/assets/fonts/Roboto-Bold.ttf);
}
#app {
  font-family: robotoRegular;
  text-align: center;
  color: #000000;
}
</style>
