<template>
  <section class="row justify-center q-pb-md">
    <section class="col-lg-6 col-md-6 col-xs-10 col-sm-10">
      <h4 class="text-center">
        Como ayudar a los <span style="color: rgb(69, 179, 175)">animales</span>
      </h4>
      <p
        :class="`${$q.screen.xs ? 'text-center' : ''}`"
        :style="`${$q.screen.xs ? 'font-size: 14px' : ''}`"
      >
        Somos la Fundación para el Asesoramiento y Acción en Defensa de los
        Animales (FAADA). La ONG que lucha para la protección animal y que
        pretende cambiar los hábitos de la sociedad que perjudican a los
      </p>

      <section>
        <section class="row justify-center">
          <section class="col-12 col-sm-2 col-md-2 flex flex-center">
            <q-avatar size="80px">
              <q-img src="~assets/OIP.jpg" />
            </q-avatar>
          </section>
          <section class="col-12 col-sm-10 col-md-10">
            <h6 :class="`${$q.screen.xs ? 'text-center' : ''}`">
              Encuentre el animalito deseado
            </h6>
            <p
              :class="`${$q.screen.xs ? 'text-center' : ''}`"
              :style="`${$q.screen.xs ? 'font-size: 14px text-center' : ''}`"
            >
              Somos la Fundación para el Asesoramiento y Acción en Defensa de
              los Animales (FAADA). La ONG que lucha para la protección animal y
              que pretende cambiar los hábitos de la sociedad que perjudican a
              los
            </p>
          </section>
        </section>
      </section>
      <section>
        <section class="row justify-center">
          <section class="col-12 col-sm-2 col-md-2 flex flex-center">
            <q-avatar size="80px">
              <q-img src="~assets/descarga.jpg" />
            </q-avatar>
          </section>
          <section class="col-12 col-sm-10 col-md-10">
            <h6 :class="`${$q.screen.xs ? 'text-center' : ''}`">
              Contacte con nosotros
            </h6>
            <section :class="`${$q.screen.xs ? 'flex flex-center' : ''}`">
              <q-btn
                style="background-color: aliceblue; color: rgb(69, 179, 175)"
                rounded
                label="Contactenos"
              />
            </section>
          </section>
        </section>
      </section>
      <section>
        <section class="row justify-center">
          <section
            :class="`col-12 col-sm-2 col-md-2 flex flex-center ${
              $q.screen.xs ? 'q-pt-lg' : ''
            }`"
          >
            <q-avatar size="80px">
              <q-img src="~assets/descarga.jpg" />
            </q-avatar>
          </section>
          <section class="col-12 col-sm-10 col-md-10">
            <h6 :class="`${$q.screen.xs ? 'text-center' : ''}`">
              Le haremos llegar su solicitud
            </h6>
            <p
              :class="`${$q.screen.xs ? 'text-center' : ''}`"
              :style="`${$q.screen.xs ? 'font-size: 14px' : ''}`"
            >
              Somos la Fundación para el Asesoramiento y Acción en Defensa de
              los Animales (FAADA). La ONG que lucha para la protección animal y
              que pretende cambiar los hábitos de la sociedad que perjudican a
              los
            </p>
          </section>
        </section>
      </section>
    </section>
    <section class="col-lg-4 col-md-4 col-xs-10 col-sm-10 flex flex-center">
      <q-avatar size="300px">
        <img src="~assets/photo_2023-04-01_12-16-22.jpg" alt="" />
      </q-avatar>
    </section>
  </section>
</template>
