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
    span.mt-4.mb-4 Para el desarrollo de una aplicación JAVA que usa el entorno de desarrollo de Eclipse es necesario descargar todas las librerías requeridas por el framework de Hibernate las cuales puede encontrar en la página oficial del ORM 
    span.marca https://hibernate.org/orm/
    | . Una vez descargado el paquete este se debe descomprimir y podrá encontrar los archivos jar necesarios en la ubicación /lib/required los cuales deberá anexar al proyecto JAVA. 
    .row.mt-5.mb-5.bg-color-gris.pb-5
      .col-7.mt-5
        .cajon.color-primario.p-4.mb-4.Neg-Izq
          span Debido a que Hibernate utiliza el Driver JDBC necesitará también descargar el Driver correspondiente a la base de datos a acceder desde su página oficial. Para el caso de MySQL podrá encontrar el Driver en: 
          span.marca https://dev.mysql.com/downloads/connector/j/. 
        p.mt-4.mb-4 En el siguiente video se muestra un ejemplo de alistamiento de una aplicación Java en IDE de Eclipse para trabajar con Hibernate y una base de datos MySQL.
        .row.color-azulclaro.ms-2
          .col-2.me-0
            img.me-0.mt-2.mb-2(src='@/assets/curso/tema1/manoClick.svg')
          .col-10
            .row.align-items-center
              .col-9
                h3.mb-0.mt-5.text-white Alistamiento Hibernate
                p.mb-0.text-white Estimado aprendiz, para profundizar sobre el tema puede consultar el siguiente video.
              .col-3
                a.boton.mb-0.mt-4.me-4.indicador__container(
                  href="https://www.youtube.com/embed/2L91WMqw96A"
                  target="_blank"
                  @mouseover="mostrarIndicador = false"
                )
                  span.Text-mediano Ver
                  i.Text-grande.fas.fa-link
                  .indicador--click(v-if="mostrarIndicador")
      .col-5
          img.Neg-Izq(src='@/assets/curso/tema1/teclado.png')
    .cajon.color-acento-botones.p-4.mb-4
      p Teniendo en cuenta que Hibernate debe usar el Driver JDBC para la ejecución de las instrucciones en la base de datos se debe construir un archivo de configuración en formato XML donde se especifique la Url del JDBC y las credenciales de acceso a la base de datos.  En la siguiente figura se presenta el esquema general de funcionamiento en el proceso de configuración:
    .row.mb-5
      .col-4
        h3.mt-5.me-0.text-white.bgNegro.p-2.mb-0.text-center Hibernate Archivo de configuración
      .col-8
    img.ms-2(src='@/assets/curso/tema1/JDBC.jpg')
    img.mt-5(src='@/assets/curso/tema1/imagen1.jpg')
    .row.bgNaranja.me-5.ms-5.mb-5.p-3.Neg-Top40.position-relative
      .col-12
        p.text-center.mb-0 Este archivo de configuración define un conjunto de propiedades que serán utilizadas para crear las sesiones mediante las cuales se inicia un conjunto de transacciones u operaciones sobre la base de datos, entre las propiedades más importantes se encuentran las siguientes:
    .row.bgbits.align-items-center.p-5
      .col-12
        .tabla-c
          table
            thead.text-bold.text-center.mb-0.Text-grande
              th Propiedad
              th Definición
            tr.Text-mediano
              th connection.driver.class
              td 
                p Parte de la configuración del JDBC donde se define el driver a usar.
            tr.Text-mediano
              th connection.url
              td 
                p Parte de la configuración del JDBC donde se define la url de la base de datos a utilizar (protocolo: url base de datos: puerto / nombre DB)
            tr.Text-mediano
              th connection.username
              td 
                p Parte de la configuración del JDBC donde se define el usuario de la base de datos a utilizar en la conexión.
            tr.Text-mediano
              th connection.password
              td 
                p Parte de la configuración del JDBC donde se define el password del usuario de la base de datos a utilizar en la conexión.
            tr.Text-mediano
              th connection.pool_size
              td 
                p Número de conexiones simultáneas al JDBC.
            tr.Text-mediano
              th dialect
              td 
                p Aunque SQL es un estándar, cada motor de bases de datos tiene una implementación particular. En esta propiedad se especifica el dialecto a utilizar por Hibernate.
            tr.Text-mediano
              th show_sql
              td 
                p Esta propiedad permite ver en la salida estándar las sentencias SQL que ejecuta en background Hibernate lo cual sirve mucho para entender lo que está sucediendo en entornos de desarrollo.
            tr.Text-mediano
              th current_session_context_class
              td 
                p Especifica el contexto de la sesión actual, por defecto se puede asignar thread.

    p.mb-4 Es importante tener en cuenta que este archivo de configuración de Hibernate debe estar ubicado en la raíz de la carpeta src del proyecto de forma que pueda ser utilizado por Hibernate en cualquier contexto de la aplicación. A continuación, se muestra cómo debe verse un archivo de configuración de Hibernate completo donde se establece una conexión con una base de datos MySQL en un servidor que se está ejecutando en la máquina local en localhost y puerto 3306 con el usuario root y contraseña 12345:
    img.mt-5(src='@/assets/curso/tema1/codigo1.jpg')





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
