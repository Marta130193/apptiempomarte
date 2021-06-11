<template>
    <main class="main">
    <div class="container_imagenes_save">
      <div class="marco">
            <div class="cerrar_imagen">
                <button>
                <i class="fas fa-trash-alt" id="basura"></i></button>
            </div>
            <img class="imagen1" :src="dataImg.photos[1].img_src"/>
        </div>
    </div>

    <div class="container_modal" id="modal">
      <div class="modal-content">
        <div class="modal-header">
          <div class="title-modal">
            <h2 class="pregunta">
              ¿Estás segurx que deseas eliminar la imagen?
            </h2>
          </div>
        </div>
        <div class="modal-body">
          <div class="respuestas">
            <button class="si" id="close_modal">
              <NuxtLink to="/save">
                <h2 class="yes">Sí</h2>
              </NuxtLink>
            </button>
            <button class="no">
              <NuxtLink to="/save">
                <h2 class="dont" id="close_modal">No</h2>
              </NuxtLink>
            </button>
          </div>
        </div>
      </div>
    </div>
  </main>
    
    

</template>
<script>
export default {
    props: {
        dataImg: {
            type:Object, 
            default: () => {

            }
        }
    }
}
</script>