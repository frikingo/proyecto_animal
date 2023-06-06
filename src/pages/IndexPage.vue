<template>
  <q-layout>
    <nav_bar />
    <sobre_nosotros id="sobre1" />
    <segunda_seccion />
    <Bienestar_dos id="" />
    <perro_1 id="cosa1" />
    <div_verde id="verde" />
    <footer_ok id="contac1" />
    <final_footer />
  </q-layout>
</template>
<!-- script para importar -->
<script setup>
import { ref, onMounted } from "vue";
import nav_bar from "src/components/nav_bar.vue";
import sobre_nosotros from "src/components/sobre_nosotros.vue";
import segunda_seccion from "src/components/segunda_seccion.vue";
import Bienestar_dos from "src/components/Bienestar_dos.vue";
import perro_1 from "src/components/perro_1.vue";
import div_verde from "src/components/div_verde.vue";
import footer_ok from "src/components/footer_ok.vue";
import final_footer from "src/components/final_footer.vue";
</script>
