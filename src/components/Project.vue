<template>
  <div>
    <router-link id="tilbage" to="/">Tilbage</router-link>
    <h1> {{project.headline}} </h1>
    <img id="banner" v-bind:src="project.imgLink" alt="Banner Image">
    <v-row>
      
      <v-col cols="8" offset="2">
        <v-row>
          <h2>Informationer om projektet</h2>
        </v-row>
        <v-row>
          <v-col cols="3" offset="2">
            <p>Projektperiode:</p>
            <p>Medvirkende:</p>
            <p>Min Rolle:</p>
            <p>Beskrivelse:</p>
          </v-col>
          <v-col cols="3">
            <p>Projektperiode:</p>
            <p>Medvirkende:</p>
            <p>Min Rolle:</p>
            <p>Beskrivelse:</p>
          </v-col>
          <v-col>
            {{project.description}}
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </div>
</template>
<script>
export default {
  data(){
    var project = this.$route.params
    return{
      show: false,
      project:{
        id: project.id,
        headline: project.headline,
        description: project.description,
        imgLink: project.imgLink,
      }
    }
  }
}
</script>

<style lang="scss" scoped>
#tilbage{
  text-decoration: underline;
  color: black;
  font-family: 'TommyRegular';
  font-size: 32px;
  margin-top: 100px;
}
h1{
margin: 0;
}

#banner{
  height: 800px;
  width: 100%;
  
}

h2{
 margin: 0;
 margin-top: 100px  ;
}
</style>