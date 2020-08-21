<template>
  <section id="do" class="section">
    <div class="container">
      <div class="columns">
        <div class="column is-10 is-offset-1 has-text-centered">
          <h1 class="title is-2">Lo que hago</h1>
          <separator></separator>
          <h2 class="subtitle is-5">Esto es mi día a día..</h2>
        </div>
      </div>
      <div class="columns">
        <div class="column do-col"
          v-for="panel in panels"
          :key="panel.id"
          :class="`is-${12 / panels.length}`">
          <div class="panel">
            <div class="panel-block">
              <p class="has-text-centered">
                <i class="fa icon-block" :class="panel.icon"></i>
              </p>
              <br>
              <h1 class="title is-5">{{ panel.title }}</h1>
              <p>{{ panel.text }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'do',
  data() {
    return {
      panels: [
        {
          icon: 'fa-graduation-cap',
          title: 'Autodidacta',
          text: 'Como todo científico de la computación es implícita la disciplina autodidacta. Esto es debido al constante cambio de las tecnologías y la robuztes de conocimientos que esta hermosa ciencia engloba.',
        }, {
          icon: 'fa-code',
          title: 'Desarrollador',
          text: 'Me gusta desarrollar nuevas soluciones, nuevas integraciones y/o nuevas automatizaciones. Tengo amplios conocimientos en desarrollo Web como Full Stack y móvil bajo la plataforma Android.',
        }, {
          icon: 'fa-pencil',
          title: 'Diseñador',
          text: 'Las aplicaciones con interfáz gráfica (UI) entran por los ojos. Es por eso que es importante tener una buena base en diseño gráfico y contenido multimedia. Artes gráficas, animación 2D, gifs, etc. no son problema.',
        }
      ],
    };
  },
  mounted() {
    sr.reveal('.do-col', 250);
  },
};
</script>

<style lang="scss" scoped>
  @import '~vars';

  .panel-block {
    flex-flow: column nowrap;
    border: none;

    p {
      font-size: 17px;
      line-height: 1.4;
    }

    i {
      color: $secondary;
      font-size: 5em;
    }
  }
</style>
