<template>
  <v-app>
    <v-content id="content">
      <router-view></router-view>

    </v-content>
  </v-app>
</template>

<script>

export default {
  name: 'App',

};
</script>

<style lang="scss">
@import "./scss/variables.scss";
@font-face {
  font-family: 'TommyBold';
  src:  url(./assets/fonts/MADETommySoftBoldPERSONALUSE.otf) format("opentype");
}

@font-face {
  font-family: 'TommyBoldOutline';
  src: url(assets/fonts/MADETommySoftBoldOutlinePERSONALUSE.otf) format("opentype");
}

@font-face {
  font-family: 'TommyRegular';
  src: url(./assets/fonts/MADETommySoftRegularPERSONALUSE.otf) format("opentype");
}

@font-face {
  font-family: 'TommyMedium';
  src: url(assets/fonts/MADETommySoftMediumPERSONALUSE.otf) format("opentype");
}

h1{
  font-family: 'TommyMedium';
  font-size: 93px;
  width: fit-content;
  margin: 0;
  margin-top: 200px;
  z-index: 2;
}
h2{
  font-family: 'TommyMedium';
  font-size: 78.2px;
  width: fit-content;
  z-index: 2;
}
h3{
  font-family: 'roboto';
  font-size: 50px;
  width: fit-content;
  z-index: 2;
}
::-webkit-scrollbar {
  width: 10px;
}
::-webkit-scrollbar-track {
  background: transparent;
}
::-webkit-scrollbar-thumb {
  background-color: map-get($map: $colorz, $key: primary);
}
</style>
