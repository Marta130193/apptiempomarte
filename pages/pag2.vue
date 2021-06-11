<template>
<!-- <div> -->
    <!-- <header-image :sources="'/img.jpg'"/> -->
    <!-- <img src="/img.jpg">
    <h1>Titulo</h1>
    <h2>subtitulos</h2>
      <p v-if="$fetchState.pending">Fetching mountains...</p>
  <p v-else-if="$fetchState.error">An error occurred :(</p>
  <div v-else>
    <h1>Nuxt Mountains</h1>
    <ul> -->
      <!-- <li v-for="mountain of mountains" :key="sol.api">{{ sol.title }}</li> -->
    <!-- </ul>
    <button @click="$fetch">Refresh</button>
  </div> -->
  
   <div >
  <Prevision />
</div>
</template>
<script>
// import HeaderImage from './HeaderImage.vue'

// export default {
// components: {HeaderImage},
//    data() {
//       return {
//         sol: []
//       }
//     },
//     async fetch() {
//       this.sol = await fetch(
//         'https://mars-weather-rems.netlify.app/rems.json'
//       ).then(res => res.json())

//     }
    
// }

</script>

<style lang="scss">
h1,
h2,
h3,
h4 {
  color: rgb(255, 255, 255);
  font-family: "Roboto";
  font-weight: 100;
  line-height: 1.1;
  letter-spacing: 0.025em;
  margin-top: 0 px;
  padding: 0;
}

//temperaturas aire y suelo//


.caja_provisional{
  display: flex;
}

#flecha{
  padding-top: 20px;
 color: white;
}

.container_temperaturas {
  display: flex;
  justify-content: center;
  box-shadow: white;
  border-radius: 20px;
  height: 150px;
  margin: 2em;
  background: rgba(196, 196, 196, 0.24);
}
.icono {
  .fas {
    display: flex;
    justify-content: center;
    margin: 0px 0px 10px;
    justify-content: center;
  
  }
}


.container_prevision {
  display: flex;
  justify-content: center;
  border-radius: 20px;
  height: 150px;
  width: 300px;
  background: rgba(196, 196, 196, 0.24);
}
.temperatura {
  display: contents;
}

.temperatura_actual_grados {
  color: white;
  font-size: 22px;
  margin-top: 15px;
}


.aire_suelo {
  display: contents;
}
.temperatura_aire {
  padding: 30px;
}

.temperatura_suelo {
  padding: 30px;
}

.temperaturaPrevision{
  display: inline-table;
  margin: 30px;
}

.borde {
  border-left: 1px solid white;
  margin-top: 20px;
  height: 7em;
}
  
</style>
