<template lang="pug">
.curso-main-container.pb-3
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5
    
    .titulo-principal.color-acento-contenido
      .titulo-principal__numero
        span 1
      h1 Sprint
    .row.bg-color-gris
      .col-5.p-0
        img(src='@/assets/curso/tema2/imagen1.jpg')
      .col-7.justify-content-center.mt-4
        p.ms-4 Es un Framework de código abierto que facilita crear aplicaciones empresariales de alto rendimiento en Java, además de Java tiene soporte para los lenguajes Groovy y Kotlin. La estructura que lo compone es modular esta estructura cuenta con una flexibilidad para implementar una variedad de arquitecturas dependiendo de los requerimientos de las aplicaciones haciendo que la programación sea lo más hacedera posible, rápida y muy segura. 

        .bloque-texto-c.color-azul.p-4.Neg-Der.position-relative
          //i.fas.fa-quote-left.text-white
          h4.mb-2.text-white.ms-5.mt-5 Historia: Rod Johnson creador de Spring se da cuenta que necesitan una herramienta para simplificar y facilitar la construcción de aplicaciones JEE utilizando EJB y escribe el libro expert one-on-one J2EE Development que es un conjunto de buenas prácticas para la creación de aplicaciones empresariales y en el año 2004 lanza primera versión 1.2.6 de Spring, según el autor era el inicio de J2EE tradicional 
          h4.text-white.text-end.mt-4 Johnson (2005):
          img.hijoHoja1(src='@/assets/curso/tema1/comillas.svg')
        p.ms-4.mt-3 La siguiente figura muestra las Versiones de Spring Framework
    .row.mb-5
      .col-4
        h3.mt-5.me-0.text-white.bgNegro.p-2.mb-0.text-center Versiones de Sprint Framework
      .col-8
    img.mb-3(src='@/assets/curso/tema2/figura1.jpg')
    .row.mb-4
      .col-3.color-azuloscuro2bordes.Neg-Top.p-1
        span.text-white En la página oficial de Spring  
        span.marcaOrange.text-white https://spring.io/ 
        span.text-white , se puede ver que actualmente el framework Spring se encuentra en la versión 5.
      .col-9
    p.mb-4 Unas de las características principales de Spring son:
    .row.mb-4
      .col-7.p-3
        LineaTiempoD.color-secundario
          p.text-small(numero="1" titulo="Flexibilidad") Contiene un grupo flexible de librerías y extensiones de terceros de Spring facilitando a los desarrolladores construir aplicaciones fácilmente.
          
          p.text-small(numero="2" titulo="Inyección de dependencia (DI)") Ofrece un patrón que permite ayudar en el acoplamiento bajo, esto quiere decir que cuando existe dependencias entre las clases y se necesita crear un objeto de esta clase lo que hace spring es suministrar este objeto obteniendo beneficios en la modularidad, escalabilidad y dependencia de clases.
          
          p.text-small(numero="3" titulo="POJOs (Plan Old Java Objects)") Facilita un sencillo desarrollo por medio de los POJOs.
          
          p.text-small(numero="4" titulo="ORM (Object Relational Mapping)") Suministra un fácil   acceso a datos por medio del ORM.       
      .col-5.justify-content-center
        img.mb-3(src='@/assets/curso/tema2/figura2.jpg')
    p.mb-4 La siguiente figura nos muestra lo que se puede crear con Spring Framework: Aplicaciones de consola, Aplicaciones de escritorio, Aplicaciones Web, Aplicaciones Móviles, Servicios SOAP, REST. Spring está orientado esencialmente al backend.    

    .row.mb-5
      .col-sm-6.col-xl-4.mb-4.mb-xl-0.mt-4
        .tarjeta.tarjeta-flip.color-primario(@mouseover="indicadorTarjetaFlip = false")
          .indicador--hover(v-if="indicadorTarjetaFlip")
          .tarjeta-flip__contenedor
            .tarjeta-flip__img(:style="{'background-image': `url(${require('@/assets/curso/tema2/fondoTarjeta1.jpg')})`}")
              .row
                .col-3
                .col-6
                  img.mb-3.mt-5(src='@/assets/curso/tema2/microservicios1.svg')
                .col-3
              h3.text-center.mt-5 Microservicios
            .tarjeta-flip__contenido.p-4.p-xl-5
              .row
                .col-3
                .col-6
                  img.mb-3.mt-5(src='@/assets/curso/tema2/microservicios2.svg')
                .col-3
              h3.text-center.mt-2 Microservicios1
              p.text-center.me-2.ms-2 Permite crear y ejecutar microservicios en producción a escala
 
      .col-sm-6.col-xl-4.mb-4.mb-xl-0.mt-4
        .tarjeta.tarjeta-flip.color-primario(@mouseover="indicadorTarjetaFlip = false")
          .indicador--hover(v-if="indicadorTarjetaFlip")
          .tarjeta-flip__contenedor
            .tarjeta-flip__img(:style="{'background-image': `url(${require('@/assets/curso/tema2/fondoTarjeta1.jpg')})`}")
              .row
                .col-3
                .col-6
                  img.mb-3.mt-5(src='@/assets/curso/tema2/nube1.svg')
                .col-3
              h3.text-center.mt-5 Nube
            .tarjeta-flip__contenido.p-4.p-xl-5
              .row
                .col-3
                .col-6
                  img.mb-3.mt-5(src='@/assets/curso/tema2/nube2.svg')
                .col-3
              h3.text-center.mt-2 Nube
              p.text-center.me-2.ms-2 Ejecución de servicios en la nube

      .col-sm-6.col-xl-4.mb-4.mb-xl-0.mt-4
        .tarjeta.tarjeta-flip.color-primario(@mouseover="indicadorTarjetaFlip = false")
          .indicador--hover(v-if="indicadorTarjetaFlip")
          .tarjeta-flip__contenedor
            .tarjeta-flip__img(:style="{'background-image': `url(${require('@/assets/curso/tema2/fondoTarjeta1.jpg')})`}")
              .row
                .col-3
                .col-6
                  img.mb-3.mt-5(src='@/assets/curso/tema2/appWeb1.svg')
                .col-3
              h3.text-center.mt-5 Aplicaciones web
            .tarjeta-flip__contenido.p-4.p-xl-5
              .row
                .col-3
                .col-6
                  img.mb-3.mt-5(src='@/assets/curso/tema2/appWeb2.svg')
                .col-3
              h3.text-center.mt-2 Aplicaciones web
              p.text-center.me-2.ms-2 Creación rápida de aplicaciones web

      .col-sm-6.col-xl-4.mb-4.mb-xl-0.mt-5
        .tarjeta.tarjeta-flip.color-primario(@mouseover="indicadorTarjetaFlip = false")
          .indicador--hover(v-if="indicadorTarjetaFlip")
          .tarjeta-flip__contenedor
            .tarjeta-flip__img(:style="{'background-image': `url(${require('@/assets/curso/tema2/fondoTarjeta1.jpg')})`}")
              .row
                .col-3
                .col-6
                  img.mb-3.mt-5(src='@/assets/curso/tema2/reactive1.svg')
                .col-3
              h3.text-center.mt-5 Reactive
            .tarjeta-flip__contenido.p-4.p-xl-5
              .row
                .col-3
                .col-6
                  img.mb-3.mt-5(src='@/assets/curso/tema2/reactive2.svg')
                .col-3
              h3.text-center.mt-2 Reactive
              p.text-center.me-2.ms-2 Permite la creación de proyectos reactivos basados en mensajes


      .col-sm-6.col-xl-4.mb-4.mb-xl-0.mt-5
        .tarjeta.tarjeta-flip.color-primario(@mouseover="indicadorTarjetaFlip = false")
          .indicador--hover(v-if="indicadorTarjetaFlip")
          .tarjeta-flip__contenedor
            .tarjeta-flip__img(:style="{'background-image': `url(${require('@/assets/curso/tema2/fondoTarjeta1.jpg')})`}")
              .row
                .col-3
                .col-6
                  img.mb-3.mt-5(src='@/assets/curso/tema2/servlets1.svg')
                .col-3
              h3.text-center.mt-5 ServLets
            .tarjeta-flip__contenido.p-4.p-xl-5
              .row
                .col-3
                .col-6
                  img.mb-3.mt-5(src='@/assets/curso/tema2/servlets2.svg')
                .col-3
              h3.text-center.mt-2 ServLets
              p.text-center.me-2.ms-2 Permite la ejecución de código impulsado por eventos se encarga del escalado y la seguridad del lado del servidor.

      .col-sm-6.col-xl-4.mb-4.mb-sm-0.mt-5
        .tarjeta.tarjeta-flip.color-primario(@mouseover="indicadorTarjetaFlip = false")
          .tarjeta-flip__contenedor
            .tarjeta-flip__img(:style="{'background-image': `url(${require('@/assets/curso/tema2/fondoTarjeta1.jpg')})`}")
              .row
                .col-3
                .col-6
                  img.mb-3.mt-5(src='@/assets/curso/tema2/batch1.svg')
                .col-3
              h3.text-center.mt-5 Batch
            .tarjeta-flip__contenido.p-4.p-xl-5
              .tarjeta-flip__img(:style="{'background-image': `url(${require('@/assets/curso/tema2/fondoTarjeta2.jpg')})`}")
                .row
                  .col-3
                  .col-6
                    img.mb-3.mt-5(src='@/assets/curso/tema2/batch2.svg')
                  .col-3
                h3.text-center.mt-2 Batch
                p.text-center.me-2.ms-2 Aplicaciones de procesamiento de datos en lote.
    .titulo-segundo.color-acento-contenido.mb-4
      h2  2.1 Introducción
    .row.mt-5.mb-5.bg-color-gris
      .col-5
          img(src='@/assets/curso/tema2/imagen2.jpg')
      .col-7.mt-4
        .row
          .col-12.bgBlanco.Neg-Der50
            .cajon.mb-4
              span.mb-0.text-small El Framework Spring básicamente con su inyección de dependencias se encarga de construir objetos y configurar todas las dependencias que estos necesiten. En Spring estos objetos que son creados son llamados beans que son anotaciones que son agregadas a las clases así: @component, @Service, @Repository etc. Uno de los principios principales de Spring es el de Inversión de Dependencia (DIP) el cual habla de que los módulos de alto nivel no deben depender de los de bajo nivel, lo que quiere decir es que hay que hacer más referencia a las abstracciones que a las implementaciones por lo que no se debe depender de una clase ni de una implementación en particular. La implementación de este principio es llamado Inversión de Control (IOc) que se encarga de desacoplar el código utilizando eventos, también es llamado como el principio de Hollywood “no nos llames; nosotros te llamaremos”, que consisten en una manera de programar donde la aplicación es quien interviene en cambio del código, para realizar la implementación del IOc se necesita un agente externo que recibe el nombre de contenedor quién es el encargado de verificar el flujo de la aplicación. Los IOc utilizan Service locator, Eventos y los DI (Inyecciones de dependencias) enfocando el Spring Framework en la DI.
        p.mt-4.text-small Inyección de Dependencias: es un patrón de diseño de software, subtipo de inversión de control cuyo objetivo es tener un código fácil de mantener o desacoplado. Su función es determinar lo que los objetos necesitan.
        p.mt-4.mb-4.text-small Existen 3 formas de realizar inyección de dependencias: Constructor, Propiedades(set) Servicio/Interfaz.
        img.mb-4(src='@/assets/curso/tema2/inyeccion.png')
    .row.bgbits.mb-4
      .col-12
        .row.mb-5
          .col-4
            h3.mt-5.me-0.text-white.bgNegro.p-2.mb-0.text-center Principio inversión de control
          .col-8
      .row
        .col-12
          img(src='@/assets/curso/tema2/figura3.png')
    p.mb-4  A continuación, se muestra un ejemplo de código donde los objetos dependen entre sí:     
    .row.mb-5
      .col-4
        h3.mt-5.me-0.text-white.color-azul.p-2.mb-0.text-center Acoplamiento hermético
      .col-8
    img.mb-4(src='@/assets/curso/tema2/acoplamiento.svg')
    img.mt-5(src='@/assets/curso/tema2/imagen3.jpg')
    .row.bgNaranja.me-5.ms-5.mb-5.p-3.Neg-Top40.position-relative
      .col-12
        p.text-center.mb-0 En el código anterior se puede observar que se obtuvo el objeto desde el exterior y que el objeto puede ser cualquier tipo de café, sin necesidad de tocar la clase TiendaCafe.

    .row.mb-4
      .col-7
        .row.mt-4.bg-color-gris.mt-4.Neg-Izq.cajon
          .col-12
            p.mt-4 Resumiendo, la inversión de control es un patrón de programación para obtener un acoplamiento flexible logrando que los objetos independientes no sean responsables de sus dependencias si no que sean recibidas desde afuera; el contenedor de IOc recoge los metadatos que vienen de un archivo XML, o código Java, y recibe las indicaciones de los objetos que debe crearlos, enlazarlos, configurarlos y destruirlos por medio de POJOs (Objetos simples de Java) creando objetos por medio del proceso que recibe el nombre de Spring Beans y resultando objetos preparados para la inyección de dependencia.
        p.mt-4 La siguiente figura evidencia el funcionamiento de una vista abstracta de Spring.
      .col-5
        img.mb-5(src='@/assets/curso/tema2/imagen4.jpg')
    .row.mb-5
      .col-4
        h3.mt-5.me-0.text-white.bgNegro.p-2.mb-0.text-center Funcionamiento vista en Spring
      .col-8   
    .row.mb-4
      .col-6
        img(src='@/assets/curso/tema2/figura4.png')
      .col-6 
        p.mb-4 En el video se explican aspectos generales de la inyección de dependencias: 
        .row.color-azulclaro.ms-2
          .col-2.me-0
            img.me-0.mt-2.mb-2(src='@/assets/curso/tema1/play.svg') 
          .col-10
            .row.align-items-center
              .col-8
                h3.mb-0.mt-3 Inyección de dependencias
                p.mb-0 Estimado aprendiz, para profundizar sobre el tema puede consultar el siguiente video.
              .col-4
                a.boton.mb-0.mt-4.me-4.indicador__container(
                  href="https://www.youtube.com/embed/2L91WMqw96A"
                  target="_blank"
                  @mouseover="mostrarIndicador = false"
                )
                  span.Text-small Ver video
                  .indicador--click(v-if="mostrarIndicador")
        p Módulos del Framework: Spring Framework es un marco de trabajo muy amplio y brinda cerca de 20 módulo los cuales se asocian en el contenedor principal, “Accesos e integración de datos, Web, AOP (Programación orientada a aspectos, Instrumentación, Mensajes y Pruebas)” (Spring ,2021)  
        p Para trabajar con Spring se necesita tener instalado los siguientes requerimientos:
        ul.lista-ul.ms-4
          li 
            i.fab.fa-buffer.azul
            | Un entorno de desarrollo (IDE): se puede seleccionar cualquiera de los relacionados en la tabla No 1
          li        
            i.fab.fa-buffer.azul
            | Un JDK (Kit de desarrollo de java) se puede descargar cualquiera de los relacionados en la tabla No 2
    .titulo-sexto.color-acento-contenido.mb-4
      h5 Tabla 1.
      span Entornos para desarrollo en Spring.
    .tabla-a.color-acento-contenido.mb-5 
      table
        thead
          tr
            th Entornos de Desarrollo
            th Enlace
        tbody
          tr
            td IntelliJ IDEA
            td https://www.jetbrains.com/idea/
          tr
            td Spring Tools
            td https://spring.io/tools
          tr
            td Visual Studio Code
            td https://code.visualstudio.com/docs/languages/java
          tr
            td Eclipse
            td https://www.eclipse.org/downloads/packages/
          tr
            td NetBeans
            td https://netbeans.apache.org/
    .titulo-sexto.color-acento-contenido.mb-4
      h5 Tabla 2.
      span JDK para desarrollo en Spring
    .tabla-a.color-acento-contenido.mb-5 
      table
        thead
          tr
            th JDK
            th Enlace
        tbody
          tr
            td JDK Oracle
            td https://www.oracle.com/java/technologies/downloads/ 

          tr
            td AdoptOpenJDK
            td https://adoptopenjdk.net/
    p.mb-4 Para construir aplicaciones en Spring Framework necesitamos:
    AcordionA.mb-5(tipo="a" clase-tarjeta="tarjeta tarjeta--azul")
      .row(titulo="Elegir jars con Maven")
        .col-md-12.mb-4.mb-md-0
          p.mb-4 Lo primero que se debe hacer es la creación de un proyecto Maven o Gradle y realizar la descarga de las dependencias necesarias.
          .titulo-sexto.color-acento-contenido.mb-4
            h5 Figura 2.
            span Creación proyecto Maven
            .row.mt-4
              .col-8
                img.me-0(src='@/assets/curso/tema2/CreacionProyectoMaven.png') 
              .col-4
                img.me-0.Neg-Der(src='@/assets/curso/tema2/hombreSenalando.png')

      div(titulo="Creación de la Aplicación")
        figure
          img(src='@/assets/template/img-placeholder.svg', alt='Texto que describa la imagen')
          figcaption Leyenda de la imagen
      div(titulo="Configurar archivo XML")
        figure
          img(src='@/assets/template/img-placeholder.svg', alt='Texto que describa la imagen')
          figcaption Leyenda de la imagen

</template>

<script>
export default {
  name: 'Tema2',
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
