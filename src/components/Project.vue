<template>
  <div id="BG" v-bind:style="BG">
    
    <router-link id="tilbage" to="/">Tilbage</router-link>
    <h1> {{project.headline}} </h1>
    <div id="banner" v-bind:style="project.imgLink" alt="Banner Image"> </div>
    
    <v-row>
      
      <v-col cols="8" offset="2">
        <v-row>
          <v-col cols="4" offset="2">
            <h2>Informationer om projektet</h2>
          </v-col>
        </v-row>
        <v-row id="tableContainer">
          <v-col cols="6" offset="2">
            <table>
              <tr>
                <td class="column1">Projekttype:</td>
                <td class="column2">{{project.type}}</td>
              </tr>
              <tr>
                <td class="column1">Projektperiode:</td>
                <td class="column2">{{project.periode}}</td>
              </tr>
              <tr>
                <td class="column1" id="medvirkendeTitel"><p>Medvirkende:</p></td>
                <td class="column2" id="medvirkende"><p v-for="(person, index) in project.medvirkende" :key="index">{{project.medvirkende[index]}}</p></td>
              </tr>
              <tr>
                <td class="column1">Min Rolle:</td>
                <td class="column2">{{project.rolle}}</td>
              </tr>
            </table>
          </v-col>
        </v-row>
        <v-row>
          <v-col id="beskrivelseContainer">
            <v-col cols="4" offset="2">
              <h2>Beskrivelse</h2>
            </v-col>
            <v-col cols="6" offset="2">
              <p id="beskrivelse">{{project.description}}</p>
            </v-col>
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
      BG: {
        backgroundImage:  'url("https://firebasestorage.googleapis.com/v0/b/portfolio-3e0a9.appspot.com/o/CV%20BG.png?alt=media&token=44676902-05a3-4732-864b-e2480f605b42")',
      },
      show: false,
      project:{
        id: project.id,
        headline: project.headline,
        type: project.type,
        periode: project.periode,
        medvirkende: project.medvirkende,
        rolle: project.rolle,
        description: project.description,
        imgLink: project.imgLink,
      }
    }
  }
}
</script>

<style lang="scss" scoped>
#BG{
  z-index: 1;
  position: absolute;
  width: 100%;
  background-size: 110%;
  background-position-x: center;
  background-position-y: -60px;
}

#tilbage{
  text-decoration: underline;
  color: black;
  font-family: 'TommyRegular';
  font-size: 32px;
  z-index: 2;
  margin: 50px 0 0 10%;
  position: fixed;
}
h1{
margin: 0;
font-size: 56px;
z-index: 2;
position: relative;
margin: 200px 100px 100px 10%;
}

#banner{
  height: 800px;
  width: 100%;
  z-index: 1;
  position: relative;
  margin-bottom: 60px;
}

h2{
 
 font-size: 32px;
 z-index: 2;
  position: relative;
}

#tableContainer{
  display: flex;
  z-index: 2;
  position: relative;
}

table{
  padding-left: 10%;
  height: 300px;
  width: 600px;
}

.column1{
width: 200px;
}
#column2{
width: 400px;
}

#medvirkendeTitel{
  z-index: 2;
  position: relative;
}

#medvirkende{
  display: flex;
  flex-flow: column;
  z-index: 2;
  position: relative;
  p{
    margin: 0;
  }
}

#beskrivelseContainer{
  display: flex;
  flex-flow: column;
  z-index: 2;
  position: relative;
}

#beskrivelse{
  padding-left: 10%;
  align-self: center;
  z-index: 2;
  position: relative;
}
</style>