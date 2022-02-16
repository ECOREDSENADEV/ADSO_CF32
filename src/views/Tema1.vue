<template lang="pug">
.curso-main-container.pb-3
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5

    //- El componente "Muestras" tiene las aplicaciones de todos los componentes de la base
    //- se encuentra en src/components/Muestras.vue
    //- Una vez el componente "Muestras" no se necesite 
    //- Se debe borrar el "import Muestras from '../components/Muestras'" y en "components" en "<script"
    //- esto evitará que se compile en la carpeta final de distribución
     // Muestras
    .titulo-principal.color-acento-contenido
      .titulo-principal__numero
        span.text-white 1
      h1.mb-4 Hibernate
    .row.bg-color-gris
      .col-5.p-0
        img.mb-3(src='@/assets/curso/tema1/manosPC.jpg')
      .col-7.justify-content-center.mt-4
        p.ms-4 Hibernate es software libre con licencia GNU LGPL que presta servicios de ORM para JAVA, es decir, es plugin que puede ser integrado al IDE de desarrollo en JAVA que facilita el proceso de mapeo de tablas en una base de datos relacional a objetos Java mediante el uso de archivos declarativos en formato XML o anotaciones.

        .bloque-texto-c.color-azul.p-4.Neg-Der.position-relative
          //i.fas.fa-quote-left.text-white
          h4.mb-2.text-white.ms-5.mt-5 Hibernate utiliza JDBC para todos los procesos de comunicación con la base de datos funcionando como una capa adicional de abstracción de las funcionalidades del JDBC. En una aplicación JAVA podremos delegar la mayoría de las operaciones de bases de datos al framework de Hibernate pero en segundo plano todo estará pasando por el API de JDBC.
          h4.text-white.text-end.mt-4 Martinez (2015):
          img.hijoHoja1(src='@/assets/curso/tema1/comillas.svg')
        p.ms-4.mt-3 Así que cuando estamos configurando Hibernate para conectarse a una base de datos lo que realmente pasa es que se configura Hibernate para el Uso del JDBC y es este quien realiza las operaciones.  A continuación se presenta el esquema general del funcionamiento:
    .row
      .col-12.justify-content-center.mt-5.mb-5
        img(src='@/assets/curso/tema1/grafica1.jpg')
</template>

<script>
import Muestras from '../components/Muestras' // borrar una vez el componente "Muestras" no se necesite
export default {
  name: 'Tema1',
  components: {
    Muestras, // borrar una vez el componente "Muestras" no se necesite
  },
  data: () => ({
    // variables de vue
  }),
  mounted() {
    this.$nextTick(() => {
      this.$aosRefresh()
    })
  },
  updated() {
    this.$aosRefresh()
  },
}
</script>

<style lang="sass"></style>
