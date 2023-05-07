<template>
  <div class="row flex flex-center q-pt-xl q-pb-xl">
    <div
      class="col-10 text-center justify-center q-pt-lg"
      style="
        background-color: rgb(69, 179, 175);
        border-radius: 20px;
        padding-bottom: 35px;
      "
    >
      <div class="row justify-center">
        <div class="col-xs-10 q-pt-lg">
          <h4 style="color: aliceblue; font-weight: bolder">
            Siganos para mas informacion
          </h4>
        </div>
      </div>
      <div class="row justify-center">
        <div class="col-xs-10 col-sm-8 col-md-7 col-lg-7 q-pt-md">
          <h6 style="color: aliceblue; font-size: 18px">
            Deja tu correo electronico y nostros le enviaremos mas informacion
            sobre actividades que realicemos o temas sobre ayuda a los
            animalitos.
          </h6>
        </div>
      </div>
      <!--  input com boton dentro    -->
      <div class="row justify-center q-pt-lg">
        <div class="col-7 col-xs-10 col-sm-8 col-md-5 col-lg-5 q-pb-xl">
          <q-input
            color="teal"
            rounded
            outlined
            v-model="email"
            type="email"
            placeholder="Ejemplo: ceda@gmail.com"
            style="background-color: azure; border-radius: 28px"
          >
            <!--  boton del inpunt    -->
            <template v-slot:append>
              <q-btn
                rounded
                style="
                  color: white;
                  background-color: rgb(69, 179, 175);
                  width: 170px;
                "
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
