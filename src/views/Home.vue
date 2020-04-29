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

      <div id="work" v-for="(item, index) in projects" :key="index">
        <img id="picture" v-bind:src=" item.imgLink ">
      </div> 
      
    </div>
  </div>
</template>

<script>



export default {
  data() {
    return {
      projects: [
        {
          headline: "homer one",
          description: "homer hungry description",
          imgLink: "https://firebasestorage.googleapis.com/v0/b/portfolio-3e0a9.appspot.com/o/_MG_7140.jpg?alt=media&token=329a2790-4cef-4426-8edd-e699abfc39f9"
        },
        {
          headline: "homer two",
          description: "homer really hungry description",
          imgLink: "https://firebasestorage.googleapis.com/v0/b/portfolio-3e0a9.appspot.com/o/6d3.jpg?alt=media&token=798cb652-18ff-4977-8bf0-5226891a3d95"
        },
        {
          headline: "homer one",
          description: "homer hungry description",
          imgLink: "https://firebasestorage.googleapis.com/v0/b/portfolio-3e0a9.appspot.com/o/_MG_7140.jpg?alt=media&token=329a2790-4cef-4426-8edd-e699abfc39f9"
        },
        {
          headline: "homer one",
          description: "homer hungry description",
          imgLink: "https://firebasestorage.googleapis.com/v0/b/portfolio-3e0a9.appspot.com/o/_MG_7140.jpg?alt=media&token=329a2790-4cef-4426-8edd-e699abfc39f9"
        },
        {
          headline: "homer one",
          description: "homer hungry description",
          imgLink: "https://firebasestorage.googleapis.com/v0/b/portfolio-3e0a9.appspot.com/o/_MG_7140.jpg?alt=media&token=329a2790-4cef-4426-8edd-e699abfc39f9"
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
    align-items: center;
    
  }
  .parallax__layer--back{
      z-index: 1;
      position: absolute;
      transform: translateZ(-3px) translateY(9000px) scale(5.5);
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
    margin-top: 400px;
    
  }
  #work:nth-child(odd){
    margin-left: random(70) / 100 * 100%;
  
  }
   #work:nth-child(even){
    margin-left: random(70) / 100 * 100%;
    
  }
  #work:last-child{
    margin-bottom: 300px;
  }
  #picture{
    background-color: map-get($map: $colorz, $key: primary);
    height: 97%;
    width: 97%;
    clip-path: polygon(25% 0%, 75% 0%, 100% 50%, 75% 100%, 25% 100%, 0% 50%);
  }
</style>