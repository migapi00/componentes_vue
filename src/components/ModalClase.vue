<template>
    
    <a href="#my-modal-2" class="btn">Modal</a>
    
    <div class="modal" id="my-modal-2">
        <div class="modal-box">
            <h3 class="font-bold text-lg">Título</h3>
            <p class="py-4">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Praesentium, maiores sit rem
                blanditiis voluptatum vitae est quos explicabo nostrum, repudiandae perspiciatis. Odio illum earum illo
                molestias adipisci, praesentium magnam obcaecati?</p>
            <div class="modal-action">
                <a href="#" class="btn">Cerrar</a>
            </div>
        </div>
    </div>
    



    <!-- <div>
        <button @click="toggle">Modal</button>
        <Teleport to="body">
            <div v-show="show" class="modal">
                <h1>Título</h1>
                <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Libero tempora voluptate et doloribus placeat
                    minus numquam iure, porro recusandae inventore magnam doloremque eligendi rem eum perspiciatis! Ipsa
                    saepe incidunt commodi.</p>
                <button @click="toggle">Cerrar</button>
            </div>
        </Teleport>
    </div> -->
</template>

<script>
export default {
  data: () => ({
    show: false,
  }),
  methods: {
    toggle() {
      this.show = !this.show;
    },
  },
};
</script>

