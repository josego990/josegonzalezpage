<template>
  <section id="about" class="section">
    <div class="container has-text-centered">
      <div class="image avatar">
        <img src="../assets/img/profile.jpg">
      </div>
      <h2 class="title is-2">Acerca de mi</h2>
      <separator></separator>
      <div class="about-text block">
        Me llamo Juan José, soy guatemalteco y desarrollador Web y <a href="https://play.google.com/store/apps/developer?id=Marck+Clarck">Móvil</a>.
        <br>
        Apasionado de la tecnología, la automatización y la integración de sistemas.
        <br>
        Trabajo casi totalmente en la nube de <a href="https://lnu.se/">Amazon AWS</a> y <a href="https://lnu.se/">Google Cloud Platform</a>.
        También me gusta la domótica, IoT y la <a href="http://arduino.org/">automatización en general</a>.
        Soy autodidacta y de esa forma he obtenido la mayoría de mis conocimientos en ciencias de la computación.
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'about',
  data() {
    return {};
  },
  mounted() {
    sr.reveal('#about .block', 200);
  },
};
</script>

<style lang="scss" scoped>
  @import '~vars';

  .avatar {
    height: 200px;
    width: 200px;
    margin: 1rem auto;

    img {
      user-select: none;
      pointer-events: none;
      border-radius: 200px;
      border: 3px solid $secondary;
    }
  }

  .about-text {
    max-width: $tablet;
    margin: auto;
  }
</style>
