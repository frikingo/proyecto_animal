<template>
  <div class="row flex flex-center q-pt-lg">
    <div class="col-10">
      <H2>Agregar productos</H2>
      <pre>{{ producto }} - {{ seleccion }}</pre>
      <q-form
        class="row col-gutter-md"
        @submit.prevent="procesarformulario"
        @reset="reset"
        ref="myform"
      >
        <div class="col-12 col-sm-6">
          <q-input
            label="producto"
            v-model="producto"
            lazy-rules
            :rules="[
              (val) => (val && val.length > 0) || 'Escriba algo por favor',
            ]"
          />
        </div>

        <div class="col-12 col-sm-6">
          <q-select
            label="prioridad"
            v-model="seleccion"
            lazy-rules
            :options="opciones"
            :rules="[
              (val) =>
                (val && val.length > 0) || 'Elija una prioridad por favor',
            ]"
          />
        </div>
        <div class="col-12">
          <q-toggle label="aceptar los terminos" v-model="terminos" />
        </div>
        <div class="col-12">
          <q-btn color="primary" label="submit" type="submit" />
          <q-btn
            color="primary"
            label="reset"
            outline
            class="q-ml-sm"
            :ripple="false"
            type="reset"
          />
        </div>
      </q-form>

      <Pintar_tabla />
    </div>
  </div>
</template>

<script>
import { ref } from "vue";
import { useQuasar } from "quasar";
import Pintar_tabla from "src/components/Pintar_tabla.vue";
export default {
  comments: { Pintar_tabla },
  setup() {
    const myform = ref(null);
    const producto = ref(null);
    const seleccion = ref(null);
    const opciones = ["maxima", "moderada", "minima"];
    const procesarformulario = () => {
      console.log("me diste click");
      if (terminos.value === false) {
        $q.notify({
          color: "red-5",
          textcolor: "wite",
          icon: "warning",
          message: "Aceptalos terminos por favor",
        });
      } else {
        $q.notify({
          color: "green-4",
          textcolor: "wite",
          icon: "cloud_done",
          message: "solicitud aceptada",
        });
        myform.value.resetValidation();
        reset();
      }
    };
    const $q = useQuasar();
    const terminos = ref(false);
    const reset = () => {
      producto.value = null;
      seleccion.value = null;
      terminos.value = false;
    };
    return {
      producto,
      seleccion,
      opciones,
      procesarformulario,
      terminos,
      reset,
      myform,
    };
  },
  components: { Pintar_tabla },
};
</script>
