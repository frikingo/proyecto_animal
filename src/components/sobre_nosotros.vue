<template>
  <section class="row justify-center">
    <section class="col-10 col-md-5 col-lg-3 flex flex-center">
      <q-avatar size="300px">
        <img src="~assets/ceda.jpg" alt="" />
      </q-avatar>
    </section>

    <section class="col-10 col-md-5 col-lg-7">
      <p :class="`${$q.screen.xs || $q.screen.sm ? 'text-center' : ''}`">
        <span style="color: blue">SOBRE NOSOTROS</span>
      </p>
      <h4 :class="`${$q.screen.xs || $q.screen.sm ? 'text-center' : ''}`">
        Grupo Animalista <span style="color: rgb(69, 179, 175)">Cubano</span>
      </h4>
      <p
        :class="`${$q.screen.xs || $q.screen.sm ? 'text-center' : ''}`"
        :style="`${$q.screen.xs ? 'font-size: 14px' : ''}`"
      >
        Esta linda perrita de tan solo un añito se escapó de su casa, vive por
        la torre Cotorro, calle 103 #611 entre 6 y 8. Se llama Sacha y la dueña
        está buscándola desesperada. Es de color amarillo clarito con el hocico
        en negro. Si la ve por favor llamar a 5-313-4377. Siempre recomendamos
        que la mascota lleve collar con los teléfonos de su dueño. Que nunca la
        dejen salir sola o sin supervisión, que la mascota esté debidamente
        esterilizada para evitar que se pierda detrás de un
      </p>
    </section>
  </section>
</template>
