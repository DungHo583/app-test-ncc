<template>
  <div id="app">
    <router-view />
  </div>
</template>

<style>
@import url(@/assets/style/main.scss);
@import url(@/assets/responsive/responsive.scss);
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
