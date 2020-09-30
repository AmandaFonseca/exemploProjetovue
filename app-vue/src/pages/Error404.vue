<template>
  <div class="fullscreen text-white text-center q-pa-md flex flex-center">
    <div>
      <div style="font-size: 30vh">404</div>

      <div class="text-h2" style="opacity: 0.4">Opa. Nada aqui...</div>

      <q-btn
        class="q-mt-xl"
        color="white"
        text-color="blue"
        unelevated
        to="/"
        label="Voltar"
        no-caps
      />
    </div>
  </div>
</template>

<style scoped>
.fullscreen {
  background-color: #ff9999;
}
</style>

<script lang="ts">
import { defineComponent } from "@vue/composition-api";

export default defineComponent({
  name: "Error404",
  created() {
    this.$router.push({ path: "/" });
  },
});
</script>
