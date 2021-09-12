<template>
  <div id="app">
    <Main />
    <PaketKursus />
  </div>
</template>

<script>
import Main from "./components/main.vue";
import PaketKursus from "./components/packet.vue";

export default {
  name: "App",
  components: {
    Main,
    PaketKursus,
  },
};
</script>

<style></style>
