<template>
  <div class="row flex flex-center q-pt-xl q-pb-xl">
    <div
      class="col-10 text-center justify-center"
      style="
        background-color: rgb(69, 179, 175);
        border-radius: 20px;
        padding-bottom: 35px;
      "
    >
      <div class="row justify-center">
        <div class="col-xs-10 q-pt-lg">
          <h4 style="color: aliceblue">Siganos para mas informacion</h4>
        </div>
      </div>
      <div class="row justify-center">
        <div class="col-8 col-xs-10 q-pt-md">
          <h6 style="color: aliceblue">
            Deja tu correo con nostros le enviarremos mas informacion sobre
            actividades que realicemos o temas sobre ayuda a los animalitos.
          </h6>
        </div>
      </div>
      <!--  input com boton dentro    -->
      <div class="row justify-center q-pt-md">
        <div class="col-7 col-xs-10 col-sm-8 col-md-5 col-lg-6">
          <q-input
            color="teal"
            rounded
            outlined
            v-model="email"
            type="email"
            label="CORREO"
            style="background-color: azure; border-radius: 28px"
          >
            <!--  boton del inpunt    -->
            <template v-slot:append>
              <q-btn
                unelevated
                rounded
                style="color: white; background-color: rgb(69, 179, 175)"
                :style="`${
                  $q.screen.xs ? 'inline-size: 55px; font-size: 12px' : ''
                } `"
                label="Enviar"
              />
            </template>
          </q-input>
        </div>
      </div>
    </div>
  </div>
</template>
