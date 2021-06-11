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
     
 <Temperaturas />
</div>
</template>
<script>


export default {
    
   data() {
      return {
        sol: []
      }
    },
    async fetch() {
      this.sol = await fetch(
        'https://mars-weather-rems.netlify.app/rems.json'
      ).then(res => res.json())

    }
}

</script>

<style lang="scss">

  h1{
    color: white;
  }
</style>