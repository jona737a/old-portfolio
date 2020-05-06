<template>
  <div id="container">
    <div id="header">
      <img id="headline" src="https://firebasestorage.googleapis.com/v0/b/portfolio-3e0a9.appspot.com/o/Portfolio.png?alt=media&token=70dfd451-657e-42b1-bcc8-cd8db9c0f79f" alt="Portfolio">
      <h1>Jonathan Evald</h1>
      <h2>Stenholdt Madsen</h2>
      <h3>Multimedia Designer</h3>
      
    </div>
    <div id="main">
      <img class="parallax__layer parallax__layer--back" src="https://firebasestorage.googleapis.com/v0/b/portfolio-3e0a9.appspot.com/o/CV%20BG.png?alt=media&token=44676902-05a3-4732-864b-e2480f605b42" alt="Background">
      <kinesis-container id="kinesis" v-for="(project, index) in projects" :key="index" v-bind:style="{marginLeft: project.random}">
        <kinesis-element id="work" strength="2" type="depth">
          <router-link id="link" v-bind:to="{ name: 'project', params: { 
            id: project.id,
            headline: project.headline,
            type: project.type,
            periode: project.periode,
            medvirkende: project.medvirkende,
            rolle: project.rolle,
            description: project.description,
            imgLink: project.imgLink,
            }}" ><div id="picture" v-bind:style=" project.imgLink "></div> </router-link>
        </kinesis-element> 
      </kinesis-container>
      
    </div>
    <div id="footer">
        <h4>Contact</h4>
        <div id="infoContainer">
          <div class="info"><h5>Email:</h5><p>jonathansmadsen@gmail.com</p></div>
          <div class="info"><h5>CV</h5><a href="https://firebasestorage.googleapis.com/v0/b/portfolio-3e0a9.appspot.com/o/CV%20Jonathan.pdf?alt=media&token=dd8a14a9-9cf6-4ce8-9d38-07294440d290">CV</a></div>
          <div class="info"><h5>Video CV</h5></div>
          <div class="info"><h5>Github</h5></div>
        </div>
      </div>
  </div>
</template>

<script>
function getRandomArbitrary(min, max) {
  return Math.random() * (max - min) + min;
}
export default {
  data() {
    return {
      projects: [
        {
          id: 1,
          headline: "astroXpress",
          type: "Skoleprojekt ",
          periode: "29/11-2019 – 21/12-2019",
          medvirkende: ["Malene Tranholm","Cecilie Dichmann","Patrick Jensen"],
          rolle: "Front-end developer",
          description: "astroXpress er mit 1. semester projekt på multimediedesigner uddannelsen. Vi fik besked på at lave en hjemmeside og noget tilhørende infografisk materiale, ud fra emnet “Space”. Det fik sat tankerne i gang hos alle gruppemedlemmer da det ikke lige var et emne der lå særlig nært hos nogen. Til sidst endte vi med at vi ville arbejde med rumturisme, og besluttede os for at opdigte virksomheden astroXpress. Det var et fuldt projekt med at inkluderet, og alle trin i Design Thinking modellen blev brugt. Vi sluttede det hele af med en eksamen i januar 2020, hvor vi skulle forsvare vores projekt. Alle i gruppen kom ud med et rigtig flot 12 tal. ",
          imgLink: {backgroundImage: 'url("https://firebasestorage.googleapis.com/v0/b/portfolio-3e0a9.appspot.com/o/_MG_7140.jpg?alt=media&token=329a2790-4cef-4426-8edd-e699abfc39f9")'},
          random: getRandomArbitrary(-10, 60) + "%"
        },
        {
          id: 2,
          headline: "PARKVUE",
          type: "Skoleprojekt",
          periode: "20/2-2020 – 26/3-2020",
          medvirkende: ["Tobias Søllingvraa","Daniel Radosa","Patrick Jensen"],
          rolle: "Multimediedesigner",
          description: "Dette projekt fik vi til opgave at designe en hjemmeside der skulle danne et overblik over gratis udendørs aktiviteter i Esbjerg. Fokusset skulle ligge på forarbejdet og det var der vi skulle ligge det meste af vores energi. Planen var heller ikke at vi skulle ende med et færdigt produkt. Projektet sluttede med at vi lavede en prototype i Adobe XD. ",
          imgLink: {backgroundImage: 'url("https://firebasestorage.googleapis.com/v0/b/portfolio-3e0a9.appspot.com/o/_MG_7140.jpg?alt=media&token=329a2790-4cef-4426-8edd-e699abfc39f9")'},
          random: getRandomArbitrary(-10, 60) + "%"
        },
        {
          id: 3,
          headline: "CMS",
          type: "Skoleprojekt (I samarbejde med Center For Maritim Sundhed)",
          periode: "17/2-2020 – 1/3-2020",
          medvirkende: ["Lars Bo Pedersen", "Filip Ahlmann", "Tobias Søllingvraa", "Patrick Jensen"],
          rolle: "Kamera og redigering",
          description: "I dette projekt havde CMS kontaktet skolen og spurgt om vi ville hjælpe dem med at lave en video der skulle vise hvad det var de lavede. Det var også meget vigtigt at der blev vist en masse klip af deres simulations scenarier, da videoen skulle bruges på en messe i USA der handlede om forskellige simulations teknologier og teknikker. Det endte så med at vi fik lavet en lille video på under 2 min, som egnede sig til at køre i ring på en standerskærm til messen. ",
          imgLink: {backgroundImage: 'url("https://firebasestorage.googleapis.com/v0/b/portfolio-3e0a9.appspot.com/o/_MG_7140.jpg?alt=media&token=329a2790-4cef-4426-8edd-e699abfc39f9")'},
          random: getRandomArbitrary(-10, 60) + "%"
        },
        {
          id: 4,
          headline: "Foto",
          type: "Hobby",
          periode: "2016 - nu",
          medvirkende: "Mig selv",
          rolle: "Fotograf",
          description: "I de seneste år har jeg taget billeder med mit kamera. Det har for det meste været en hobby som startede da jeg gik på efterskole. De fleste billeder jeg tager, er når jeg er på ferie med familien. Da det for det meste er en hobby, har jeg ikke brugt det kommercielt. Jeg har mest af alt brugt det til at udfolde min kreativitet og skabe minder. ",
          imgLink: {backgroundImage: 'url("https://firebasestorage.googleapis.com/v0/b/portfolio-3e0a9.appspot.com/o/_MG_7140.jpg?alt=media&token=329a2790-4cef-4426-8edd-e699abfc39f9")'},
          random: getRandomArbitrary(-10, 60) + "%"
        },
        {
          id: 5,
          headline: "Den rene skære sandhed",
          type: "Skoleprojekt (efterskole)",
          periode: "1 uge i foråret 2017 ",
          medvirkende: "Alle elever og lærere på Mariager efterskole 2016-2017",
          rolle: "PR og grafisk design",
          description: "Projektet var det første projekt nogen sinde hvor jeg arbejdede med grafisk design. Efterskolen skulle vise en musical, og til det skulle der være en masse reklame. Til det skulle der bruges plakater, postkort, content til Sociale Medier og en folder der skulle ligge på stolen til forestillingen. Jeg arbejdede mest med at lave de trykte materialer, men jeg tog også billeder og videoer i løbet af ugen som blev brugt til diverse sociale medier og andet. ",
          imgLink: {backgroundImage: 'url("https://firebasestorage.googleapis.com/v0/b/portfolio-3e0a9.appspot.com/o/_MG_7140.jpg?alt=media&token=329a2790-4cef-4426-8edd-e699abfc39f9")'},
          random: getRandomArbitrary(-10, 60) + "%"
        },
      ]
    };
  }
}

</script>

<style lang="scss">
@import "./../scss/variables.scss";


#container{
    perspective: 1px;
    height: 100vh;
    overflow-x: hidden;
    overflow-y: scroll;
}

  #header{
    display: flex;
    align-items: center;
    flex-flow: column;
  }
  #headline{
    z-index: 2;
    width: 110%;
    position: absolute;
    transform: translateZ(-1px) translateY(-300px) scale(2);
  }
  #main{
    display: flex;
    flex-flow: column;
  }
  .parallax__layer--back{
      z-index: 1;
      position: absolute;
      transform: translateZ(-3px) translateY(9000px) scale(5.5);
    }

  #kinesis{
    height: 800px;
    width: 1000px;
    margin-top: 400px;
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 2;
    box-sizing: border-box;
  }
  #work{
    z-index: 2;
    background-color: map-get($map: $colorz, $key: secondary);
    height: 800px;
    width: 1000px;
    clip-path: polygon(25% 0%, 75% 0%, 100% 50%, 75% 100%, 25% 100%, 0% 50%);
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 0;
    
    p{
      z-index: 4;
      position: relative;
    }
  }
  
  #work:last-child{
    margin-bottom: 300px;
  }
  a#link{
    height: 100%;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    box-sizing: border-box;
  }
  #picture{
    background-color: map-get($map: $colorz, $key: primary);
    height: 97%;
    width: 97%;
    clip-path: polygon(25% 0%, 75% 0%, 100% 50%, 75% 100%, 25% 100%, 0% 50%);
    z-index: 3;
  }

  #footer{
    z-index: 2;
    position: relative;
    height: 200px;
    background-color: map-get($map: $colorz, $key: secondary);

    table{
      width: 90%;
      td{
        width: 15%;
        margin: auto;
      }
    }
  }
</style>