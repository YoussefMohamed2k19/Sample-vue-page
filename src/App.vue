<template>
  <div class="container">
    <Navbar />
    <ImageGallery />
    <SendUS />
    <Footer />
  </div>
</template>

<script>
import "bootstrap/dist/css/bootstrap.css";
import "bootstrap-vue/dist/bootstrap-vue.css";
import Navbar from "./components/Navbar.vue";
import ImageGallery from "./components/ImageGallery.vue";
import SendUS from "./components/SendUS.vue";
import Footer from "./components/Footer.vue";
export default {
  name: "App",
  components: {
    Navbar,
    ImageGallery,
    SendUS,
    Footer,
  },
};
</script>

<style>
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  font-family: Poppins, sans-serif;
  background-color: #f1f1f1;
}
.font-bold {
  font-weight: 600;
}
</style>
