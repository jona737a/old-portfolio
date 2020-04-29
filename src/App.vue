<template>
  <v-app>
    <v-content>
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

h4{
  font-family: 'TommyMedium';
  font-size: 93px;
}
h5{
  font-family: 'TommyMedium';
  font-size: 78.2px;
}

#box{
  width: 100px;
  height: 20px;
  background-color: red;
}
</style>
