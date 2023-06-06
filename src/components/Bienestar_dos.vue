<template>
  <section class="q-pt-lg" style="background-color: gainsboro">
    <section class="row justify-center">
      <section class="col-10 text-center">
        <h6>Usted puede contactar con nosotros por los siguientes motivos</h6>
        <div class="row justify-center">
          <div class="col-8">
            <p>
              Es importante para nosotros que usted se registren, enviando su
              correo electronico o siguiendonos en las redes sociales para que
              esten al tanto de las actividades de la organizacion y si
              actividad es fundamental para la ayuda de los animales. AYUDENOS
              SALVARLOS.
            </p>
          </div>
        </div>
        <q-btn
          style="background-color: aliceblue; color: rgb(69, 179, 175)"
          rounded
          label="contactenos"
        />
      </section>
    </section>

    <section class="row text-center justify-center q-pt-md q-gutter-sm">
      <section class="col-10">
        <section class="row">
          <section class="col-sm-6 col-md-3">
            <q-btn
              round
              style="color: rgb(69, 179, 175); background-color: aliceblue"
              icon="call_missed"
            ></q-btn>

            <q-card-section>
              <section class="text-h6">Reportar alguna perdida</section>
            </q-card-section>
            <q-card-section
              class="q-pt-none"
              :style="`${$q.screen.sm ? 'padding-top: 35px' : ''}`"
            >
              Si usted o alguna persona allegada a perdido algun animalito puede
              contactar con nosotros y l@ ayudaremos. Promoxionando atraves de
              los correos electronicos de las personas que nos siguen.
            </q-card-section>
          </section>
          <section class="col-sm-6 col-md-3">
            <q-btn
              round
              style="color: rgb(69, 179, 175); background-color: aliceblue"
              icon="call"
            ></q-btn>
            <q-card-section>
              <section class="text-h6">Reportar animal en peligro</section>
            </q-card-section>
            <q-card-section class="q-pt-none">
              ak va un texto random de varias lineas sobres los animales , son
              las 5 Am y no he dormido pork el texto anterior fue una kk y debe
              de ser de varias lineas, amalia me esta agitando para quue la
              lleve a la parada.
            </q-card-section>
          </section>
          <section class="col-sm-6 col-md-3">
            <q-btn
              round
              style="color: rgb(69, 179, 175); background-color: aliceblue"
              icon="pets"
            ></q-btn>

            <q-card-section>
              <section class="text-h6">Adopcion de un animal</section>
            </q-card-section>
            <q-card-section class="q-pt-none">
              Si usted quiere adoptar algun animalito puede contactar con
              nosotros. en los comentarios ponga el codigo del animalito que
              desea ayudar.
            </q-card-section>
          </section>
          <section class="col-sm-6 col-md-3">
            <q-btn
              round
              style="color: rgb(69, 179, 175); background-color: aliceblue"
              icon="info"
            ></q-btn>
            <q-card-section>
              <section class="text-h6">Pedir informacion</section>
            </q-card-section>
            <q-card-section class="q-pt-none">
              Si usted tiene alguna duda o necesita informacion sobre nosotros,
              puede contactarnos sin ningun problema, en el apartado del
              comentario haga su pregunta.
            </q-card-section>
          </section>
        </section>
      </section>
    </section>
  </section>
</template>
