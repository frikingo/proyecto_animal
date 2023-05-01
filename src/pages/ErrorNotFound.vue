<template>
  <section
    class="fullscreen bg-blue text-white text-center q-pa-md flex flex-center"
  >
    <section>
      <section style="font-size: 30vh">404</section>

      <section class="text-h2" style="opacity: 0.4">
        Oops. Nothing here...
      </section>

      <q-btn
        class="q-mt-xl"
        color="white"
        text-color="blue"
        unelevated
        to="/"
        label="Go Home"
        no-caps
      />
    </section>
  </section>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "ErrorNotFound",
});
</script>
