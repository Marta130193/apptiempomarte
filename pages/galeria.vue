<template>
  <main class="main">
    <!-- <Imagenes
     
      :data="dataMars"
     
    /> -->
    <Imagenes dataImg="dataImg"/>
  </main>
</template>



<script>
export default{
  data() {
    return {
      dataImg: {
        title: 'title',
        image: 'icon.png',
        photos: 'image',
      }
    }
  }
}
</script>

<style lang="scss">
.container_imagenes_save {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  margin: 100px;
  grid-column-gap: 0px;
  grid-row-gap: 0px;
}

img {
  width: 500px;
  height: auto;
  margin: 0px 30px 30px;
}

.marco {
  border-radius: 30px;
  background-color: rgba(196, 196, 196, 0.24);
  margin: 0px 10px 10px 0px;
  text-align: right;
}

.marco_izq {
  border-radius: 30px;
  background-color: rgba(196, 196, 196, 0.24);
  margin: 0px 0px 10px 0px;
}

#basura {
  margin: 10px;
  color: white;
  padding: 5px;
}

.imagen1 {
  grid-area: 1 / 1 / 2 / 2;
  box-sizing: content-box;
}

.imagen2 {
  grid-area: 1 / 2 / 2 / 3;
}

.imagen3 {
  grid-area: 1 / 3 / 2 / 4;
}

.pregunta {
  color: rgb(23, 19, 65);
  font-size: 14px;
  font-weight: bold;
}
.container_modal {
  display: flex;
  position: absolute;
  background-color: white;
  border-radius: 30px;
  position: fixed;
  display: none;
}

.modal-header {
  margin: 0px;
  .title-modal {
    margin: 20px;
  }
}

.modal-body {
  display: flex;
  margin: 20px;
}

.respuestas {
  display: flex;
  font-size: 14px;
  font-weight: bold;
}

.yes {
  color: rgb(23, 19, 65);
  font-size: bold;
  font-size: 14px;
  font-weight: bold;
}

.dont {
  color: rgb(23, 19, 65);
  font-size: 14px;
  font-weight: bold;
}

button {
  background-color: transparent;
  border: none;
}

.modal .fondoModal {
  position: fixed;
  background-color: rgba(128, 128, 131, 0.596);
  width: 100%;
  height: 100%;
  top: 0;
  z-index: 100;
}

#basura {
  display: flex;
  justify-content: flex-end;
}

</style>