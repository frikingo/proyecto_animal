<template>
  {{ $q.screen.xs ? "XS" : "" }}
  {{ $q.screen.sm ? "SM" : "" }}
  {{ $q.screen.md ? "MD" : "" }}
  {{ $q.screen.lg ? "LG" : "" }}
  {{ $q.screen.xl ? "XL" : "" }}
  <div class="row justify-center">
    <div class="col-lg-10 col-md-10 col-sm-10">
      <p :class="`${$q.screen.sm ? 'text-center' : ''}`" class="q-pt-lg">
        <span style="color: rgb(69, 179, 175)"> galeria </span>
      </p>
    </div>
    <div class="col-lg-9 col-md-8 col-sm-8">
      <h4 :class="`${$q.screen.sm || $q.screen.xs ? 'text-center' : ''}`">
        Animales disponibles para
        <span style="color: rgb(69, 179, 175)"> ayudar </span>
      </h4>
    </div>
    <div
      :class="`${$q.screen.sm || $q.screen.xs ? 'text-center  q-pt-md ' : ''}`"
      class="col-lg-1 col-md-2 col-sm-8"
    >
      <q-btn
        unelevated
        rounded
        style="background-color: rgb(69, 169, 175); color: aliceblue"
        label="ver todos"
      />
    </div>
  </div>

  <div class="row justify-center">
    <div
      class="col-10 col-xs-10 col-sm-10 col-md-4 col-lg-3 flex flex-center q-pt-lg"
    >
      <q-card
        style="border-radius: 20px"
        :style="`${$q.screen.md || $q.screen.lg ? 'width: 250px;' : ''} ${
          $q.screen.sm ? 'width: 300px;' : ''
        } `"
        class="my-card"
      >
        <img
          style="width: 500px; height: 400px"
          :style="`${$q.screen.md ? 'height: 350px;' : ''} `"
          src="~assets/photo_2023-04-01_12-16-32.jpg"
        />

        <q-card-section>
          <div class="row">
            <div class="col-10 col-sm-10 col-md-10 col-lg-10">
              <h5>Pastor aleman</h5>
            </div>
            <div class="col-2 col-sm-1 col-md-1 col-lg-2">
              <q-btn round color="negative" icon="add" />
            </div>
            <p style="size: 50px">Edad 12 años</p>
          </div>
          <p style="text-align: right">
            <span style="font-weight: bolder">P001</span>
          </p>
        </q-card-section>
      </q-card>
    </div>
    <div
      class="col-10 col-xs-10 col-sm-10 col-md-4 col-lg-3 flex flex-center q-pt-lg"
    >
      <q-card
        style="border-radius: 20px"
        :style="`${$q.screen.md || $q.screen.lg ? 'width: 250px;' : ''} ${
          $q.screen.sm ? 'width: 300px;' : ''
        }`"
        class="my-card"
      >
        <img
          style="width: 500px; height: 400px"
          :style="`${$q.screen.md ? 'height: 350px;' : ''} `"
          src="~assets/photo_2023-04-01_12-16-42.jpg"
        />

        <q-card-section>
          <div class="row">
            <div class="col-10 col-sm-10 col-md-10 col-lg-10">
              <h5>Gato</h5>
            </div>
            <div class="col-2 col-sm-1 col-md-1 col-lg-2">
              <q-btn round color="warning" icon="add" />
            </div>
            <p style="size: 50px">Edad 1 año</p>
          </div>
          <p style="text-align: right">
            <span style="font-weight: bolder">G001</span>
          </p>
        </q-card-section>
      </q-card>
    </div>
    <div
      class="col-10 col-xs-10 col-sm-10 col-md-4 col-lg-3 flex flex-center q-pt-lg"
    >
      <q-card
        style="border-radius: 20px"
        :style="`${$q.screen.md || $q.screen.lg ? 'width: 250px;' : ''} ${
          $q.screen.sm ? 'width: 300px;' : ''
        }`"
        class="my-card"
      >
        <img
          style="width: 500px; height: 400px"
          :style="`${$q.screen.md ? 'height: 350px;' : ''} `"
          src="~assets/photo_2023-04-01_12-16-37.jpg"
        />

        <q-card-section>
          <div class="row">
            <div class="col-10 col-sm-10 col-md-10 col-lg-10">
              <h5>Labrador</h5>
            </div>
            <div class="col-2 col-sm-1 col-md-1 col-lg-2">
              <q-btn round color="positive" icon="add" />
            </div>
            <p style="size: 50px">Edad 6 Meses</p>
          </div>
          <p style="text-align: right">
            <span style="font-weight: bolder">P002</span>
          </p>
        </q-card-section>
      </q-card>
    </div>
  </div>
</template>
