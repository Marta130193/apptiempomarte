<template>
  <div class="container">
    <div class="container_header">
      <!-- header top -->
      <div class="header_brand">
        <div class="header_brand_left">
          <i class="fa fa-bars active" id="abrir" onclick="mostrar()"></i>
        </div>
        <div class="header_brand_right">
          <button class="save" id="add">
            guardar
            <i class="fas fa-plus-circle"></i>
          </button>
          <div class="searchbox hidden">
            <button class="buscar"><i class="fa fa-search"></i></button>
            <input class="texto" type="text" placeholder="Búsqueda" />
          </div>
        </div>
      </div>
    </div>

    <div id="siderbar" class="mostrar">
      <nav class="contenido">
        <div><i class="fa fa-times" id="cerrar" onclick="ocultar()"></i></div>
        <ul>
          <NuxtLink to="/">Inicio</NuxtLink>
        </ul>
        <ul class="usser">
          Usuario
        </ul>
        <li>Nombre usuario</li>
        <i class="fas fa-angle-down"></i>
        <li>Perfil</li>
        <ul class="menu__enlace">
          Archivos
        </ul>
        <i class="fas fa-angle-down" id="desplegar_submenu"></i>
        <li><NuxtLink to="/pag2">Temperaturas</NuxtLink></li>
        <li><NuxtLink to="/galeria">Galería</NuxtLink></li>
      </nav>
    </div>
   
    <Nuxt />
    <!-- <Nuxt :nuxt-child-key="someKey" /> -->
    <!-- <NuxtChild /> -->
    
  </div>
</template>
<script>
</script>
<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  cursor: pointer;
}
body {
  font-family: "Trebuchet MS", "Lucida Sans Unicode", "Lucida Grande",
    "Lucida Sans", Arial, sans-serif;
  background-color: #030839;
}
.marte_hour {
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;
  flex-direction: column;
}
.container_header {
  margin: 20px 20px 0px 20px;
}

.reloj {
  display: flex;
}
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
.main {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

#siderbar {
  //display: none;
  left: 0px;
  width: 250px;
  height: 100%;
  background-color: white;
  color: #030839;
  width: 300px;
  //position: absolute;
  .contenido {
    margin: 10px;
    ul {
      padding: 0;
      margin: 0px 0px 0px 30px;
      list-style: none;
      li {
        list-style: none;
      }
    }
  }
}

#cerrar {
  display: flex;
  justify-content: flex-end;
  cursor: pointer;
}

.header_brand {
  display: flex;
  justify-content: space-between;
  color: white;
}
.header_brand_right {
  display: flex;
}

.header_brand_left {
  display: flex;
}
.abrir {
  justify-content: center;
  align-items: center;
  display: flex;
}
.buscar {
  color: white;
  border: none;
}
.texto {
  background-color: transparent;
  border: none;
}
.save {
  color: white;
  border: none;
  margin: 0px 10px 0px;
}

.icono {
  .fas {
    display: flex;
    justify-content: center;
    margin: 0px 0px 10px;
    justify-content: center;
  }
}
</style>
