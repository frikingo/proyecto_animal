<template>
  <q-page>
    {{ $q.screen.xs ? "XS" : "" }}
    {{ $q.screen.sm ? "SM" : "" }}
    {{ $q.screen.md ? "MD" : "" }}
    {{ $q.screen.lg ? "LG" : "" }}
    {{ $q.screen.xl ? "XL" : "" }}
    <section :class="`row justify-center ${$q.screen.xs ? 'q-px-lg' : ''}`">
      <section class="col-12 col-sm-10 col-md-4 flex flex-center">
        <q-avatar size="350px ">
          <img style="padding-top: 10px" src="~assets/th.jpg" />
        </q-avatar>
      </section>
      <section class="col-12 col-sm-10 col-md-7">
        <p>
          <span style="color: blue">sobre nosotros</span>
        </p>
        <h4 :style="$q.screen.xs || $q.screen.sm ? 'margin-top: -10px' : ''">
          Grupo Animalista <span style="color: blue">Cubano</span>
        </h4>

        <p :style="$q.screen.xs || $q.screen.sm ? 'margin-top: -30px' : ''">
          mucho texto ramdon debe de ir ak deberia buscar algo en google y
          ponerlo aki pero el internet esta muy lento y se me es imposible. puta
          lluvia no para de llover y yo con ganas de hacer cositas hoy en la pc,
          mi miedo es que quiten el fluido electrico y se me joda todo pero
          buueno que puede ser que no sea. tengo un hambre pero me da pereza
          levantarte.
        </p>
      </section>
    </section>

    <section class="q-pa-md">
      <section class="row justify-center">
        <section class="col-4">
          <h6>
            Como ayudar a los <span style="color: blue"> animalitos </span>
          </h6>

          <p>
            Los loros o psitácidas son animales salvajes, no domésticos, por lo
            que el entorno que encuentran en cautividad les dificulta muchísimo
            su adaptación, derivando en frecuentes problemas físicos y
            psicológicos y, por tanto, en una pobre calidad de vida. En esta
            clase abordamos la materia del bienestar animal desde el punto de
            vista de las psitácidas, entendiendo sus características y
            necesidades biológicas, y adaptando a éstas el entorno que les
            ofrecemos en condiciones controladas.
          </p>

          <section class="container">
            <section>
              <q-avatar>
                <img src="~assets/OIP.jpg" alt="" />
              </q-avatar>
            </section>

            <section>
              <h6 style="padding-left: 20px">
                <p>no se que dice en el cartel pero tiene el mismo largo</p>
              </h6>
            </section>
          </section>

          <section class="container">
            <section>
              <q-avatar>
                <img src="~assets/descarga.jpg" alt="" />
              </q-avatar>
            </section>

            <section>
              <h6 style="padding-left: 20px">
                <p>no se que dice en el cartel pero tiene el mismo largo</p>
              </h6>
              <q-btn
                class="glossy"
                rounded
                color="white"
                label="Boton redondeado"
                text-color="blue"
              />
            </section>
          </section>

          <section class="container">
            <section>
              <q-avatar>
                <img src="~assets/R.png" alt="" />
              </q-avatar>
            </section>

            <section>
              <h6 style="padding-left: 20px">
                <p>no se que dice en el cartel pero tiene el mismo largo</p>
              </h6>
            </section>
          </section>
        </section>
        <section class="col-4">
          <q-avatar size="500px">
            <img style="padding-top: 10px" src="~assets/3017316426.jpg" />
          </q-avatar>
        </section>
      </section>
    </section>

    <section style="background: gray">
      <section class="flex flex-center">
        <h4>Usted puede contactar con nosotros por los siguientes motivos</h4>

        <section class="row">
          <section class="col-10 flex flex-center" style="padding-left: 20%">
            <h6 style="margin-top: 5px">
              Es importante para nosotros que ustedes se registren enviandonos
              su correo electronico o siguiendonos en sus redes sociales para
              que esten al tanto de las actividades de la organizacion y su
              actividad es fundamental para la ayuda de los animales. Ayudanos a
              ayudarte
            </h6>
          </section>
        </section>
      </section>

      <section class="flex flex-center">
        <q-btn
          class="glossy"
          rounded
          color="white"
          label="Boton redondeado"
          text-color="blue"
        />
      </section>
      <section class="row flex flex-center q-pa-xl">
        <section class="class=col-8 col-md-2 col-sm-12">
          <q-avatar style="background-color: azure; color: cyan">
            <q-icon class="las la-undo" size="50px" style=""></q-icon>
          </q-avatar>
          <h4>El amor de un Perro</h4>
          <p class="flex flex-center">
            Los perros nos dan su amor incondicional sin pedir nada a cambio.
            ¡Eso sí que es un amigo de verdad! No lo cambio ni por todo el oro
            del mundo.
          </p>
        </section>

        <section class="class=col-8 col-md-2 col-sm-12">
          <q-avatar style="background-color: azure; color: cyan">
            <q-icon class="las la-phone" size="50px" style=""></q-icon>
          </q-avatar>
          <h4>1</h4>
          <p>1</p>
        </section>

        <section class="class=col-8 col-md-2 col-sm-12">
          <q-avatar style="background-color: azure; color: cyan">
            <q-icon class="las la-paw" size="50px" style=""></q-icon>
          </q-avatar>
          <h4>1</h4>
          <p>1</p>
        </section>

        <section class="class=col-8 col-md-2 col-sm-12">
          <q-avatar style="background-color: azure; color: cyan">
            <q-icon
              class="las la-exclamation-circle"
              size="50px"
              style=""
            ></q-icon>
          </q-avatar>
          <h4>1</h4>
          <p>1</p>
        </section>
      </section>
    </section>
  </q-page>
</template>

<style>
.container {
  display: flex;

  align-items: first baseline;
}

/*
12
breakpoints
xs  0px  All window sizes (same as no breakpoint specifier)
sm  600px  Larger than extra small sized window
md  1024px  Larger than small window
lg  1440px  Larger than medium-sized sized window
xl  1920px  Larger than large sized window
 */
</style>

<script setup>
/* */
import { useQuasar } from "quasar";

const $q = useQuasar();
</script>
