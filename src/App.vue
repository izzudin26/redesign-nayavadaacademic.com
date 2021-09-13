<template>
  <div id="app" class="transform transition-all duration-1000">
    <Header />
    <Main />
    <PaketKursus />
    <Social />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/header.vue";
import Main from "./components/main.vue";
import PaketKursus from "./components/packet.vue";
import Social from "./components/social.vue";
import Footer from "./components/footer.vue";

export default {
  name: "App",
  components: {
    Header,
    Main,
    PaketKursus,
    Social,
    Footer,
  },
};
</script>

<style></style>
