<template>
  <div id="q-app">
    <router-view />
  </div>
</template>
<script lang="ts">
import { defineComponent } from "@vue/composition-api";

export default defineComponent({
  name: "App",
});
</script>
<style scoped>
body {
  font-family: "Open Sans";
  font-size: 14px;
  line-height: 1.8;
  letter-spacing: 0.5px;
  word-wrap: break-word;
  font-weight: 400;
  background-color: #000000;
  text-align: initial;
}
</style>