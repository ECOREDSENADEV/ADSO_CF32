<template lang="pug">
.curso-main-container.introduccion
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5.mb-5
  
    .titulo-principal.color-acento-contenido
      .titulo-principal__numero
        span
          i.fas.fa-info.text-white
      h1 Introducción
    p.mb-4 Vamos a comenzar el presente componente formativo con un video donde se describe de una manera general la temática a tratar:
    figure.mb-5
      .video
        iframe(width="560" height="315" src="https://www.youtube.com/embed/2L91WMqw96A" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen)
      figcaption Video: Leyenda del video

    .bloque-texto-g.p-3.p-sm-4.p-md-5.bg-gris
      .bloque-texto-g__img(
        :style="{'background-image': `url(${require('@/assets/curso/intro/pared.jpg')})`}"
      )
      .bloque-texto-g__texto.p-4
        p.mb-0 Es en este contexto donde aparecen frameworks como Hibernate y Sprint para facilitar el proceso de transformación de información requerido entre el mundo de las bases de datos relacionales, la lógica de negocio y el mundo de la programación orientada a objetos.

</template>

<script>
export default {
  name: 'Introduccion',
  data: () => ({
    // variables de vue
  }),
}
</script>

<style lang="sass"></style>
