<template>
  <div
    class="row"
    style="padding-top: 350px; padding-bottom: 270px; background-color: grey"
  >
    <div class="col-12 flex flex-center">
      <section
        id="poster"
        :style="`${$q.screen.xs ? ' width: 300px;  height: 230px;' : ''} `"
      >
        <img src="~assets/img1.jpg" alt="" />
        <img src="~assets/img2.jpg" alt="" />
        <img src="~assets/img3.jpg" alt="" />
      </section>
    </div>

    <div
      class="col-12 flex flex-center justify-center"
      style="padding-top: 50px"
    >
      <q-btn
        rounded
        flat
        label="Pagina Principal"
        class="q-mr-md distancia"
        color="greed"
        style="background-color: rgb(69, 179, 175)"
        @click="abrirComponente"
      />
    </div>
  </div>
</template>
<style>
section {
  display: flex;
  width: 600px;
  height: 430px;
}

section img {
  width: 0px;
  flex-grow: 1;
  object-fit: cover;
  opacity: 0.8;
  transition: 0.5s;
  -webkit-transition: 0.5s;
  -moz-transition: 0.5s;
  -ms-transition: 0.5s;
  -o-transition: 0.5s;
}

section img:hover {
  cursor: crosshair;
  width: 300px;
  opacity: 1;
  filter: contrast(150%);
  -webkit-filter: contrast(150%);
}

#poster:hover {
  box-shadow: 0px 0px 50px rgba(0, 0, 0, 1);
}
</style>

<script>
export default {
  methods: {
    abrirComponente() {
      this.$router.push("/");
    },
  },
};
</script>

<script setup>
import { onMounted } from "vue";

onMounted(() => {
  const el = document.getElementById("poster");
  const height = el.clientHeight;
  const width = el.clientWidth;
  el.addEventListener("mousemove", (evt) => {
    const { layerX, layerY } = evt;
    const yRotation = ((layerX - width / 2) / width) * 20;
    const xRotation = ((layerY - height / 2) / height) * 20;
    const string = `
perspective(500px)
scale(1.1)
rotateX(${xRotation}deg)
rotateY(${yRotation}deg)`;

    el.style.transform = string;
  });
  el.addEventListener("mouseout", () => {
    el.style.transform = `
    perspective(500px)
    scale(1)
    rotateX(0)
    rotateY(0)`;
  });
});
</script>
