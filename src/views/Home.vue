<template>
  <div>
    <header>
      <img id="headline" src="https://firebasestorage.googleapis.com/v0/b/portfolio-3e0a9.appspot.com/o/Portfolio.png?alt=media&token=70dfd451-657e-42b1-bcc8-cd8db9c0f79f" alt="Portfolio">
      <h1>Jonathan Evald</h1>
      <h2>Stenholdt Madsen</h2>
      <h3>Multimedia Designer</h3>
    </header>
    <main>
      

      <div id="work" v-for="(item, index) in projects" :key="index">
        <img id="picture" v-bind:src=" item.imgLink ">
      </div> 
      
    </main>
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
      ]

    };
  }
}
</script>

<style lang="scss">
@import "./../scss/variables.scss";
  main{
    display: flex;
    flex-flow: column;
    width: 100%;
  }
  #work{
    background-color: map-get($map: $colorz, $key: secondary);
    height: 800px;
    width: 1000px;
    clip-path: polygon(25% 0%, 75% 0%, 100% 50%, 75% 100%, 25% 100%, 0% 50%);
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 0;
    margin-left: -10%;
    margin-top: 400px;
    
  }
  #work:nth-child(odd){
    margin-left: random(70) / 100 * 100%;
  
  }
   #work:nth-child(even){
    margin-left: random(70) / 100 * 100%;
    
  }
  #picture{
    background-color: map-get($map: $colorz, $key: primary);
    height: 97%;
    width: 97%;
    clip-path: polygon(25% 0%, 75% 0%, 100% 50%, 75% 100%, 25% 100%, 0% 50%);
  }
</style>