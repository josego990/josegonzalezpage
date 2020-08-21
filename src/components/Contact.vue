<template>
  <section id="contact" class="section">
    <div class="container has-text-centered">
      <h2 class="title is-2">Contact</h2>
      <separator color="black"></separator>
      <h5 class="subtitle reveal is-5">
        Siempre en búsqueda de emocionantes oportunidades de desarrollo y hacer nuevos amigos 👋
      </h5>
      <div class="block reveal">
        <a class="button grow is-dark" href="https://api.whatsapp.com/send?phone=50246249172" target="_blank">
            <span>Envíame un mensaje</span>
            <b-icon icon="fab fa-whatsapp" size="is-small" />
        </a>
      </div>
       <div class="block reveal">
        <a class="button grow is-dark" :href="`mailto:${email}`" target="_blank">
            <span>o un correo</span>
            <b-icon icon="fa fa-envelope" size="is-small" />
        </a>
      </div>
      
    </div>
  </section>
</template>

<script>
export default {
  name: 'contact',
  data() {
    return {
      email: 'josego990@gmail.com',
    };
  },
  mounted() {
    sr.reveal('#contact .reveal', 250);
  },
};
</script>
