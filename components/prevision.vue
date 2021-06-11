<template>
  <div>
      
     <div class="container_presion">


            <div class="animacion">
                <img src="assets/img/animacion.gif">
            </div>

            <div class="presion" id="glass">

            </div>
            <div class="fechita" id="data-caret"><i class="fas fa-caret-left"></i></div>
        </div>

        <!-- temperaturas -->
        <div class="caja_provisional">
            <!-- <div class="container_temperaturas"> -->
            <div class="temperaturaPrevision">
					<h3 class="icono" ><i class="fas fa-temperature-high"></i></h3>	
					<h4>{{dataMars.weather_report.magnitudes.max_temp}}max. </h4>
					<h4>{{dataMars.weather_report.magnitudes.min_temp}}min.</h4>  
				</div>
				<span class="borde"></span>
				<div class="temperatura_aire">
					<h3 class="icono"><i class="fas fa-clock"></i></h3>
					<h4>{{dataMars.weather_report.magnitudes.sunrise}} salida</h4>
					<h4>{{dataMars.weather_report.magnitudes.sunset}} puesta</h4>
				</div>
				<span class="borde"></span>
				<div class="temperatura_suelo">
					<h3 class="icono"><i class="fas fa-mountain"></i></h3>
					<h4>{{dataMars.weather_report.magnitudes.max_gts_temp}}max.</h4>
					<h4>{{dataMars.weather_report.magnitudes.min_gts_temp}}min.</h4>
				</div>

        </div>

     
  </div>


 
</template>
  <script> 
// let API_KEY = "8frhMzKpGP9bakdBIfgCnH5samta4mur1Mk6hN09"; 

export default {
    data() {
      
      return {
        weather_report: [],
      }
    },
    async fetch() {
      
      this.weather_report = await fetch(  
        'https://api.nasa.gov/mars-photos/api/v1/rovers/curiosity/photos?sol=1000&page=1&api_key=${API_KEY}'
      ).then(res => res.json())
    }
  }

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