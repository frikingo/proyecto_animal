<template>
  <q-layout>
    <header>
      <div class="row justify-center">
        <div class="col-12 col-sm-6 col-md-4 nav-me">
          <img src="~assets/jade.jpg" alt="" />
        </div>
        <!-- menu hamburguesa oculto -->
        <q-btn
          rounded
          flat
          icon=" menu"
          label="Menu"
          class="q-mr-md abrir-menu"
          color="black"
          @click="openNav"
        />

        <div
          class="col-10 col-sm-6 col-md-6 flex flex-center z-top menu-nav"
          :class="{ visible: open }"
          id="nav"
        >
          <!-- menu cerrar hamburguesa -->
          <q-btn
            rounded
            flat
            icon=" closed"
            class="q-mr-md cerrar-menu"
            color="grey-1"
            @click="closeNav"
          />
          <div class="menu-lista" id="menu">
            <!-- botones del navbar -->
            <q-btn
              rounded
              flat
              label="Inicio"
              class="q-mr-md distancia"
              color="grey-1"
              @click="goToInicio('inicio')"
            />

            <q-btn
              rounded
              flat
              label="Sobre Nosotros"
              class="q-mr-md distancia"
              color="grey-1"
              @click="goToSobre1('sobre1')"
            />
            <q-btn
              rounded
              flat
              label="Lista de animales"
              class="q-mr-md distancia"
              color="grey-1"
              @click="goToLista2('lista2')"
            />

            <q-btn
              rounded
              flat
              label="Contactenos"
              class="bg-grey-1 distancia"
              color="secondary "
              @click="goToContac1('contac1')"
            />
          </div>
        </div>
      </div>
    </header>
    <!-- textos del header -->
    <div class="relative-position">
      <div class="row flex flex-center fondo" id="inicio">
        <div class="col-10 z-top">
          <h3 style="color: aliceblue; font-weight: bolder">
            Encuentre su mascota
          </h3>
          <p style="color: aliceblue; font-weight: bolder">
            Cuando ayudas o adoptas un animal estas opteniendo un pedazo de
            historia
          </p>
        </div>
      </div>
      <div
        style="
          position: absolute;
          width: 100%;
          height: 100%;
          background-color: aqua;
          top: 0;
          opacity: 0.2;
        "
      ></div>
    </div>
    <!-- boton contactanos que aparece en el medio -->
    <div class="row justify-center">
      <div class="col-10" id="phonebtn">
        <q-btn rounded class="bg-white">
          <q-avatar class="bg-secondary" size="33px"
            ><q-icon name="phone" size="22px" style="color: #fff"
          /></q-avatar>
          +53 52519414</q-btn
        >
      </div>
    </div>

    <sobre_nosotros id="sobre1" />
    <segunda_seccion />
    <Bienestar_dos />
    <card_componente id="lista2" />
    <div_verde />
    <footer_ok id="contac1" />
    <final_footer />
  </q-layout>
</template>
<!-- script para importar -->
<script setup>
import { ref, onMounted } from "vue";
import sobre_nosotros from "src/components/sobre_nosotros.vue";
import segunda_seccion from "src/components/segunda_seccion.vue";
import Bienestar_dos from "src/components/Bienestar_dos.vue";
import card_componente from "src/components/card_componente.vue";
import div_verde from "src/components/div_verde.vue";
import footer_ok from "src/components/footer_ok.vue";
import final_footer from "src/components/final_footer.vue";
</script>

<style>
/* propiedades el nav */
header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  justify-content: space-around;
  transition: 0.7s;
  padding: 30px 20px;
  z-index: 10;
}
/* tama;o a la imagen de jade  */
header img {
  width: 100px;
  height: 45px;
}
/* fondo de pantalla del hader */
.fondo {
  position: relative;
  background-image: url(assets/photo_2023-04-01_12-16-47.jpg);
  opacity: 0.7;
  width: 100%;
  height: 600px;
  background-size: cover;
  background-position: center center;
  font-weight: bolder;
}
/* fondo del boton */
section button {
  background-color: #fff;
}
/* color del scroll */
header.abajo {
  background: #26a69a;
  padding: 5px 10px;
}
/* color de los botones con efecto scroll */
header.abajo button {
  color: #fff;
}
/* boton de contacto con numero telefonico en el medio */
#phonebtn {
  margin-top: -20px;
}
/* para que se oculten no este en vista movil */
.abrir-menu {
  display: none;
}
/* para que se oculten no este en vista movil */
.cerrar-menu {
  display: none;
}
/* estas propiedades no se van aplicar por ecima de la pantalla con 600px o mas */
@media screen and (max-width: 1170px) {
  .distancia {
    padding: 20px;
    margin: 10px;
    font-size: 15px;
  }

  .menu-lista {
    margin-top: -240px;
  }

  .abrir-menu {
    display: block;
  }

  .cerrar-menu {
    display: block;
    margin-top: -250px;
  }

  .menu-nav {
    opacity: 0;
    visibility: hidden;
    position: fixed;
  }

  .menu-nav {
    display: flex;
    flex-direction: column;
    align-items: center;
    position: fixed;
    top: 0;
    right: 0;
    background-color: #26a69a;
    padding: 2rem;
    justify-content: space-evenly;
    transition: transfrom 0.3s ease-in-out;
    box-shadow: 0 0 0 100vmax rgba(0, 0, 0, 0.5);
    bottom: 0px;
  }

  .visible {
    opacity: 1;
    visibility: visible;
  }

  .nav-lista {
    flex-direction: column;
    align-items: end;
  }
}
</style>

<script>
//efecto scroll que lo copiamos de alvaro(se agrega un evento que caundo se haga el scroll mayor que Y se aplique el css abajo)
window.addEventListener("scroll", function () {
  var header = document.querySelector("header");
  header.classList.toggle("abajo", window.scrollY > 0);
});

const open = ref(false);
// Funcionamiento del menu hamburguesa
function closeNav() {
  open.value = false;
}

function openNav() {
  open.value = true;
}

// para cuando toque el boton creado anterior mente con su id realice el scroll hasta el inicio
//no me pinchan los demas botones, no se por k(queda pendiente)

function goToInicio(id) {
  const inicio = document.getElementById(`inicio`);
  if (inicio) inicio.scrollIntoView({ behavior: "smooth", block: "start" });
}
function goToSobre1(id) {
  const sobre1 = document.getElementById("sobre1");
  if (sobre1) sobre1.scrollIntoView({ behavior: "smooth", block: "start" });
}

function goToContac1(id) {
  const contac1 = document.getElementById(`contac1`);
  if (contac1) contac1.scrollIntoView({ behavior: "smooth", block: "start" });
}
function goToLista2(id) {
  const lista2 = document.getElementById(`lista2`);
  if (lista2) lista2.scrollIntoView({ behavior: "smooth", block: "start" });
}
</script>
