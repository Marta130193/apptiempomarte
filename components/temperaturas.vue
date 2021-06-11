<template>
  <div>
    <main class="main">
      <div class="marte_hour">
        <div class="location">MARTE</div>
        <div class="reloj"></div>
        <div id="sol"></div>
      </div>

      <div class="container_presion">
        <div class="animacion">
          <img src="/animacion.gif" />
        </div>

        <div class="presion" id="glass"></div>
        <div class="fechita" id="data-caret">
          <i class="fas fa-caret-left"></i>
        </div>
      </div>

      <div class="caja_provisional">
       

        <div class="container_temperaturas"></div>

      
      </div>
    </main>
    <Nuxt />
  </div>
</template>


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


.caja_provisional {
  display: flex;
}

#flecha {
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

.temperaturaPrevision {
  display: inline-table;
  margin: 30px;
}

.borde {
  border-left: 1px solid white;
  margin-top: 20px;
  height: 7em;
}


.container_presion {
  display: flex;
}

.presion {
  width: 15px;
  // height: 300px;
  background: rgb(246, 11, 11);
  background: linear-gradient(
    180deg,
    rgba(246, 11, 11, 0.7763480392156863) 44%,
    rgba(230, 202, 18, 0.8855917366946778) 72%,
    rgba(0, 212, 255, 1) 100%
  );
}

.fechita {
  color: white;
  padding-top: 20px;
}

</style>