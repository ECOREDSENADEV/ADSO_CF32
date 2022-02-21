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
      #t_2_1_intro.h2  2.1 Introducción
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
        .row.bg-color-gris.mt-4.Neg-Izq.cajon
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
        p.mb-4 Configuración de las dependencias en el archivo pom.XML
          .row
            .col-4.cajon
              img.me-0(src='@/assets/curso/tema2/hombreSenalandoDer.png') 
            .col-8
              .titulo-sexto.color-acento-contenido.mb-4
                h5 Figura 3.
                span Configuración dependencias
              img.me-0.Neg-Der(src='@/assets/curso/tema2/ConfiguracionDependencias.svg')
        p.mb-4 Las dependencias se deben visualizar en la carpeta Dependencias
          .titulo-sexto.color-acento-contenido.mb-4
            h5 Figura 4.
            span Dependencias
            .row.mt-4
              .col-8
                img.me-0(src='@/assets/curso/tema2/dependencias.png') 
              .col-4
                img.me-0.Neg-Der(src='@/assets/curso/tema2/hombreSenalando.png')
      div(titulo="Creación de la Aplicación")
        p.mb-4 Para el ejemplo se creará un programa con el ejemplo de HolaPlaneta.
        figure
          img(src='@/assets/template/tema2/codigo1.svg', alt='Codigo ejemplo de Hola Planeta')
      div(titulo="Configurar archivo XML")
        p.mb-4 Una vez se tenga la aplicación se realizará la configuración en el archivo springXMLconfig 
        figure
          img(src='@/assets/template/tema2/codigo2.svg', alt='Configuración en archivo springXMLconfig')
        p.mb-4.mt-4 A continuación, se muestra un nuevo ejemplo de código explicando más a detalle el uso del Contenedor en Spring.Para el siguiente ejemplo se tiene un proyecto llamado “Sena” el cual tiene una clase aprendiz con los siguientes atributos:
        figure
          img(src='@/assets/template/tema2/codigo3.svg', alt='Contenedor en Spring')
        p.mt-4.mb-4 Al utilizar este proyecto Sena Spring framework cuenta con un archivo XML que gestiona objetos (Spring IOC Container) para este proyecto recibe el nombre de springconfig.xml y se ve de la siguiente manera.
        figure
          img(src='@/assets/template/tema2/codigo4.svg', alt='Archivo springconfig.xml')
        .row.mt-5.mb-5
          .col-5.bg-color-gris
              img(src='@/assets/curso/tema2/estudiantes.png')
          .col-7.mt-4
            .row.cajon.mt-5.Neg-Der50.cajon.bgBlanco.p-2
              .col-12
                p.mb-0.text-small.mt-4.ms-4.me-4 En la configuración del archivo se ve que la etiqueta “bean” referencia la clase AprendizBean.java, además el atributo “class” dirige a la dirección del proyecto y cuenta con un atributo id que permite agregar un nombre para poder identificarlo. Las demás etiquetas como “property” indican los atributos de la clase AprendizBean y con la etiqueta “value” se pueden agregar valores directos. Por medio de los métodos get y set el Spring Container (Contenedor de Spring) obtiene acceso y puede modificar los objetos de la clase AprendizBean. Con los archivos de configuración XML Spring facilita una clase de listas por cada uno de los beans existentes para poder hacer llamado de ellos y asi poder manipularlos desde otras clases sin tener que realizar varias instancias.
        p.mt-4.mb-4 En el siguiente código se muestra la implementación de Spring del control de los objetos del proyecto Sena.
        figure
          img(src='@/assets/template/tema2/codigo5.svg', alt='implementación de Spring del control de los objetos del proyecto Sena')
        p.mt-4.mb-4 Lo que mostraría el código anterior sería:
        .row.justify-content-center
          .col-3
          .col-6
            h3.mt-5.me-0.text-white.color-azul.p-4.mb-0.text-center.Text-grande.rounded Zulema León, es la actual estudiante         
          .col-3
        .cajon.color-acento-contenido.mb-4.mt-4.p-3
          p La salida que muestra se logró realizando las configuraciones en el archivo XML, La utilidad del uso de Spring se evidencia en proyectos grandes con varias clases y varios objetos ya que facilita un manejo mucho más eficiente.          
    .titulo-segundo.color-acento-contenido.mb-4
      #t_2_2_sprintdata.h2  2.2 Spring Data
    .row.mt-5.mb-5
      .col-5.bg-color-gris
          img(src='@/assets/curso/tema2/maquina.png')
      .col-7
        .row.cajon.mt-2.Neg-Der50.cajon.bgBlanco.p-2
          .col-12
            p.mb-0.text-small.mt-4.ms-4.me-4  Spring ofrece una variedad de proyectos independientes que se pueden articular en un proyecto principal, cada proyecto permite resolver una necesidad en especial del negocio, algunos de ellos se muestran en la siguiente imagen.
        figure
          img.mt-4.mb-4(src='@/assets/curso/tema2/mosaico.png')
          figcaption Nota. https://spring.io/projects 
    p.mt-4.mb-4 Uno de los proyectos más utilizados es el SpringData ya que es uno de los módulos más grandes de Spring debido a que cuenta con muchos submódulos cuyo objetivo principal es proporcionar una serie de herramientas que permiten realizar integraciones muy sencillas con los diferentes entornos de almacenes de datos disponibles. Los datos que se utilizan pueden proceder de orígenes tanto de bases de datos relacionales como no relacionales.
    p.mb-4 Las funcionalidades de Spring Data son:

    .row.mb-5.justify-content-center
      .col-sm-6.col-lg-2.mb-4.mb-lg-0
        .tarjeta--boton.color-primario.text-white--hover.p-4
          .row.justify-content-center.mb-3
            .col-7
              figure
                img(src='@/assets/componentes/ej-03.svg', alt='Texto que describa la imagen')

          p.text-small Poderosos repositorios y uso personalizado de mapeo de objetos

      .col-sm-6.col-lg-2.mb-4.mb-lg-0
        .tarjeta--boton.color-secundario.text-white--hover.p-4
          .row.justify-content-center.mb-3
            .col-7
              figure
                img(src='@/assets/componentes/ej-03.svg', alt='Texto que describa la imagen')

          p.text-small Creación de consultas dinámicas fundamentadas en los nombres que tienen los métodos.

      .col-sm-6.col-lg-2.mb-4.mb-sm-0
        .tarjeta--boton.color-primario.text-white--hover.p-4
          .row.justify-content-center.mb-3
            .col-7
              figure
                img(src='@/assets/componentes/ej-03.svg', alt='Texto que describa la imagen')

          p.text-small Plantillas de clases que brindan propiedades elementales que hacen más fácil utilizar los repositorios. 

      .col-sm-6.col-lg-2.mb-4.mb-sm-0
        .tarjeta--boton.color-acento-botones.text-white--hover.p-4
          .row.justify-content-center.mb-3
            .col-7
              figure
                img(src='@/assets/componentes/ej-03.svg', alt='Texto que describa la imagen')

          p.text-small Campos que hacen referencia a fecha de creación y modificación de las clases.

      .col-sm-6.col-lg-2.mb-4.mb-sm-0
        .tarjeta--boton.color-primario.text-white--hover.p-4
          .row.justify-content-center.mb-3
            .col-7
              figure
                img(src='@/assets/componentes/ej-03.svg', alt='Texto que describa la imagen')

          p.text-small Sencilla integración con Spring Framework por medio de la configuración de clase o archivos XML.
      .col-1
    .row.mb-5
      .col-4
        h3.mt-5.me-0.text-white.bgNegro.p-2.mb-0.text-center Modulos principales
      .col-8 

    .row.mb-5
      .col-md-6.mb-5.mb-md-0
        LineaTiempoD.color-secundario
          p.text-small(numero="1" titulo="Spring Data Commons") Brinda infraestructura compartida para módulos de spring 
          
          p.text-small(numero="2" titulo="Spring Data JDBC") Implementa repositorios fundamentados en JPA
          
          p.text-small(numero="3" titulo="Spring Data JPA") Implementa repositorios fundamentados en JPA
          
          p.text-small(numero="4" titulo="Spring Data Gemfire") Implementa GemFire para aplicaciones baja latencia

          p.text-small(numero="5" titulo="Spring Data KeyValue") Implementa repositorios para datos de clave-valor

          p.text-small(numero="6" titulo="Spring Data LDAP") Implementa repositorios para soporte de LDAP

          p.text-small(numero="7" titulo="Spring Data MongoDB") Soporte para documentos y repositorios de MongoDB.

          p.text-small(numero="8" titulo="Spring Data Rest") Implementa repositorios Restful.

          p.text-small(numero="9" titulo="Spring Data Redis") Fácil acceso a Redis desde Spring

          p.text-small(numero="10" titulo="Spring Data para Apache Cassandra")  Implementación para aplicaciones orientadas a datos

          p.text-small(numero="11" titulo="Spring Data para Apache Geode") Implementación para aplicaciones orientadas a datos
      .col-md-6.mb-5.mb-md-0
        img(src='@/assets/curso/tema2/hombreServer.png')
    .cajon.color-acento-contenido.mt-4.mt-4.p-4
      p Invitación a conocer todos los módulos de SpringData en el siguiente enlace:  https://spring.io/projects/spring-data.

    .row.mt-5.mb-5
      .col-5
          img(src='@/assets/curso/tema2/imagen5.jpg')
      .col-7.mt-4
        .row
          .col-12.bg-color-gris.Neg-Der50
            .cajon.mb-4.p-3
              span.mb-0.text-small A continuación, se presenta un ejemplo de un mapeo para JPA que es uno de los submódulos de SpringData:
          p.mt-4.mb-4 Para el ejemplo se realiza la clase Persona que representa una tabla en la base de datos llamada Persona.

    .row.mb-4
      .col-5

        ImagenInfografica.color-acento-botones.mb-5
          template(v-slot:imagen)
            figure
              img(src='@/assets/template/tema2/cuadro1.svg', alt='Mapeo para JPA')

          .tarjeta.color-acento-contenido.p-3(x="11%" y="12.2%" numero="1")
            p La creación de la tabla se especifica por medio de la anotación @entity y en el atributo “name” se coloca el nombre de la tabla.

          .tarjeta.color-acento-contenido.p-3(x="11%" y="30.3%" numero="2")
            p Por medio de la anotación @Column se asigna cada uno de los campos de la tabla de la base de datos a los atributos de la clase Persona con la etiqueta “name” se hace referencia al nombre de la columna de la tabla.

      .col-7
        .row.bg-tabla3.mb-4
          .col-2.p-0
            img.ms-0.mb-0(src='@/assets/curso/tema2/listaCheck.svg')
          .col-10.text-white.p-3
            p Una vez implementada la clase Persona se crea una interfaz que extiende de la clase CrudRepository de SpringData que brinda varias funcionalidades del crud como: save (), delete (), find(),findAll() etc. 
        .row.mt-5
          .col-1
          .col-11
            img(src='@/assets/curso/tema2/codigo1.svg')
    .cajon.mt-4.mb-4.color-acento-contenido.p-3
      p Como se puede ver en el anterior código al extender de la clase CrudRepository nos facilita métodos como findByNombre que genera una consulta de todas las personas con el parámetro nombre que en base de datos relacionales seria SELECT * FROM persona WHERE nombre=? como se ve reduce considerablemente las sentencias permitiendo obtener consultas dinámicas.
    p.mb-4 Otro de los grandes proyectos de Spring es Spring Boot que se describe a continuación.
    .titulo-segundo.color-acento-contenido.mb-4
      #t_2_3_sprintboot.h2 2.3. Spring Boot y MySQL
        
    .row.mt-5.mb-5.bg-color-gris
      .col-5
          img(src='@/assets/curso/tema2/figura5.png')
      .col-7.mt-4
        .row
          .col-12.bgBlanco.Neg-Der50
            .cajon.mb-4
              span.mb-0.text-small Spring boot es una infraestructura liviana que suprime en gran parte la tarea de configurar las aplicaciones fundamentadas en Spring, Spring Boot  a diferencia de Spring Framework realiza una simplificación en cuanto a configuración y el despliegue de las aplicaciones.
        p.mt-4.mb-4.text-small Las características de Spring Boot:
        .row.align-items-center.mb-4
          .col-12
            ul.lista-ul.ms-4
              li 
                i.fab.fa-buffer.azul
                | Es intuitivo: Permite crear aplicaciones rápidamente gracias a sus valores predeterminados.
              li        
                i.fab.fa-buffer.azul
                | Permite crear aplicaciones que son independientes de Spring
              li        
                i.fab.fa-buffer.azul
                | Incluye los servidores de Undertow, Tomcat o jetty.
              li        
                i.fab.fa-buffer.azul
                | Usualmente realiza la configuración automática de librerías de Spring o de otros.
              li        
                i.fab.fa-buffer.azul
                | No hay que realizar configuraciones de archivos XML.
              li        
                i.fab.fa-buffer.azul
                | Agiliza el desarrollo.
    p.mt-4.mb-4 Spring Boot cuenta con dos mecanismos que son los que permiten la simplificación de los procesos y son: Contenedor de aplicaciones integrado y Starters.

    .tarjeta--container.row.mb-5

      .col-md.tarjeta.color-primario.p-5
        .row.justify-content-center.mb-4
          .col-4
            figure
              img(src='@/assets/componentes/tema2/hojas.svg', alt='Contenedor de aplicaciones integrado')
          
        h2.text-center Contenedor de aplicaciones integrado
        p la compilación de las aplicaciones web las compila como archivo .jar desplegado en un servidor tomcat facilitando la distribución de las aplicaciones, anteriormente se trabajaba con .war que si se requiere se puede seguir utilizando.

      .col-md.tarjeta.p-5
        .row.justify-content-center.mb-4
          .col-4
            figure
              img(src='@/assets/componentes/tema2/puzzle.svg', alt='Starters')
          
        h2.text-center Starters
        p son los encargados de brindar una variedad de dependencias las cuales se agregan al proyecto, estas pueden ser de terceros o de Spring. Los starters por defecto traen una configuración de valores por defecto.
    .cajon.mt-4.mb-4.color-acento-contenido.p-3         
      p Otra de las ventajas de Spring boot es que ofrece un mecanismo que genera la estructura del proyecto de Spring Boot automáticamente, este inicializador crea el archivo pom.xml, el main de la aplicación y un archivo de test para verificar que la aplicación corre de forma correcta.
    .titulo-sexto.color-acento-contenido.mb-4.ms-5
      h5 Figura 5.
      span Inicializador de Spring
    .row.mb-4.justify-content-center
      .col-2
      .col-8
        figure
          img(src='@/assets/curso/tema2/figura6.png', alt='Inicializador de Spring') 
          figcaption Nota. https://start.spring.io/
      .col-2

    img(src='@/assets/curso/tema2/codigo2.jpg')
    .row.bg-gris.me-5.ms-5.mb-5.p-4.Neg-Top30.position-relative.rounded
      .col-12
        p.text-center.mb-0 A continuación, se realizan los pasos para la creación de un proyecto en Spring Boot.
    .titulo-principal.color-primario
      .titulo-principal__numero
        span 1
      span Paso 1: Comienza un nuevo proyecto: ingresar a start.spring.io y crea un proyecto web.
    .row.mb-4
      .col-1
      .col-10
        img.ms-2.mb-4(src='@/assets/curso/tema2/figura7.png')
      .col-1
    .titulo-principal.color-primario
      .titulo-principal__numero
        span 2
      span Paso 2: Ingresa el código
    .row.mb-4
      .col-1
      .col-10
        img.ms-2.mb-4(src='@/assets/curso/tema2/figura8.png')
      .col-1
    .cajon.mt-4.mb-4.color-acento-contenido.p-3         
      p Lo que hace el método hello() es recibir un parámetro de tipo String con el nombre de name y después concatenar este parámetro con la palabra Hello esto quiere decir que si se ingresa un nombre Zulema la salida seria “Hello Zulema”.
    .titulo-principal.color-primario.mb-4
      .titulo-principal__numero
        span 3
      span Paso 3: Prueba del proyecto
    p.mb-4 Ahora solo es probar el proyecto para esto se debe abrir una consola Windows +r, se debe ubicar en la carpeta del proyecto y ejecutar el siguiente comando: 
    .row.mb-4
      .col-1
      .col-10.bgNegro.p-4
        p.text-white.mb-0 mvnw spring-boot:run
      .col-1
    p.mb-4 y se mostrará la siguiente imagen:
    .row.mb-4
      .col-1
      .col-10
        img.ms-2.mb-4(src='@/assets/curso/tema2/figura9.png')
      .col-1
    p.mb-4 Lo que hace es ejecutar el servidor Tomcat que ya viene por defecto dentro del Spring Boot, ahora se debe ingresar al navegador y escribir el localhost con el puerto 8080 y se mostrará la ejecución de la aplicación.  En la  siguiente video clase se explica de forma más detallada cómo utilizar Spring Boot:
    figure.mb-5
      .video
        iframe(width="560" height="315" src="https://www.youtube.com/embed/2L91WMqw96A" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen)

    .row.mt-5.mb-5
      .col-5
          img(src='@/assets/curso/tema2/imagen6.jpg')
      .col-7.mt-4
        .row
          .col-12.bg-color-gris.Neg-Der50
            .cajon.mb-4.p-3
              p Spring boot y MySQL: Para tener una aplicación web completa es necesario almacenar información por esta razón es importante realizar conexiones con bases de datos.
              p Para  este ejemplo se mostrará cómo se realiza la conexión con la base de datos MYSQL.
              p Los requerimientos fundamentales son: Tener instalado MYSQL, el entorno de desarrollo y seguir estos pasos:

    SlyderA
      .row.fondoBanner1
        .col-md-8.mb-4.mb-md-0
          .row.mt-5.ms-4
            .col-2
              .row
                .col-4
                .col-8
                  img.ms-5(src='@/assets/curso/tema2/uno.svg')
            .col-10
              p.ms-5 Declarar dependencias: JPA, MySQL JDBC Driver, Web como se mostró en el ejemplo anterior por medio del inicializador se pueden seleccionar las dependencias requeridas como se muestra en la siguiente imagen.
            img.ms-4.me-4(src='@/assets/curso/tema2/figura10.png')      
        .col-md-4.col-sm-6
          figure
            img(src='@/assets/curso/tema2/hombreSenalando.png')
      div
        .row.fondoBanner1
          .col-md-4.col-sm-6
            figure
              img.ms-5.mt-5(src='@/assets/curso/tema2/hombreSenalandoDer.png')
          .col-md-8.mb-4.mb-md-0
            .row.ms-4
              .col-2
                .row
                  .col-4
                  .col-8
                    img.ms-5(src='@/assets/curso/tema2/dos.svg')
              .col-10
                p.ms-5.mb-4 Después de agregar las dependencias clic en GENERATE y descargará un archivo zip el cuál se debe descomprimir y después importar el proyecto en el IDE para este caso Spring Tool Suite.
              img.ms-4.me-4(src='@/assets/curso/tema2/figura11.png')      
      div
        .row.fondoBanner1
          .col-md-8.mb-4.mb-md-0
            .row.mt-5.ms-4
              .col-2
                .row
                  .col-4
                  .col-8
                    img.ms-5(src='@/assets/curso/tema2/tres.svg')
              .col-10.col-sm-6
                p.ms-5 El paso siguiente es abrir el archivo “aplication.properties” y configurar todas las propiedades de la conexión así:

                ImagenInfografica.color-acento-botones.mb-5
                  template(v-slot:imagen)
                    figure
                      img(src='@/assets/curso/tema2/figura12.svg')

                  .tarjeta.color-acento-contenido.p-3(x="2.6%" y="28.8%")
                    span.text-bold Línea 1: 
                    | permite obtener los metadatos de la base de datos. 

                  .tarjeta.color-acento-contenido.p-3(x="2.7%" y="39.3%")
                    span.text-bold Línea 2: 
                    | se muestra la url de la conexión con el motor de base de datos.
                  .tarjeta.color-acento-contenido.p-3(x="2.7%" y="55.3%")
                    span.text-bold Línea 3: 
                    | Se especifica el nombre del usuario de la base de datos para la conexión
                  .tarjeta.color-acento-contenido.p-3(x="2.7%" y="67.3%")
                    span.text-bold Línea 4: 
                    | Se especifica clave de la base de datos para la conexión 
                  .tarjeta.color-acento-contenido.p-3(x="2.7%" y="77.3%")
                    span.text-bold Línea 5: 
                    | La propiedad true permite utilizar las consultas JPA a realizar en la base de datos.
 
          .col-md-4.col-sm-6
            figure
              img(src='@/assets/curso/tema2/hombreSenalando.png')
      div
        .row.fondoBanner1
          .col-md-8.mb-4.mb-md-0.col-sm-12
            .row.mt-5.ms-4
              .col-md-2
                .row
                  .col-4
                  .col-8
                    img.ms-5(src='@/assets/curso/tema2/cuatro.svg')
              .col-10
                p.ms-5.mb-4 Lo que queda es ejecutar la aplicación y comprobar que no existan problemas con la conexión a la base de datos. Para ejecutar dar clic derecho en el archivo java seleccionar la opción >Run As y >Spring Boot App Si todo está bien ahora solo queda ir al motor de bases de datos y verificar si creó el esquema.
              img.ms-4.me-4.mb-5(src='@/assets/curso/tema2/figura13.svg')      
          .col-md-4.col-sm-6
            figure
              img(src='@/assets/curso/tema2/hombreSenalando.png')
    .titulo-segundo.color-acento-contenido.mb-4
      #t_2_4_validaciones.h2 2.4. Validaciones
    .row.mt-5.mb-5.bg-color-gris
      .col-5
          img(src='@/assets/curso/tema1/imagen7.jpg')
      .col-7.mt-4
        .row
          .col-12.bgBlanco.Neg-Der50.mt-4.mb-4
            .cajon.mb-4
              span.mb-0 Es muy importante realizar validaciones cuando se están desarrollando aplicaciones web en java para impedir que se ingresen datos que afecten al programa, en Sprint viene incluido el hibernate-validator en el paquete spring-boot-starter-web que permite validar valores de los campos Beans.
        img.mt-4(src='@/assets/curso/tema2/codigo3.svg')
    .row.justify-content-center.mb-4
      .col-10.bg-grisDegrade.p-4.rounded
        p.me-0.mb-0.text-center.text-bold Para el ejemplo se realiza la creación de un bean con unas anotaciones que permiten la validación de ingreso de un usuario.       
    .row.justify-content-center.mb-4
      .col-10
        img(src='@/assets/curso/tema2/codigo4.svg')
    .row.justify-content-center.mb-4.mt-4.rounded
      .col-8.bg-grisDegrade.p-4
        p.me-0.mb-0.text-center.text-bold Una vez se crean las anotaciones se debe crear el controlador.
    .row.justify-content-center.mb-4
      .col-10
        img(src='@/assets/curso/tema2/codigo5.svg')
    p.mt-5.mb-4 Una vez se realice el controlador se puede realizar la prueba enviando una solicitud Post.
    .row.justify-content-center.mb-4.mt-4
      .col-8.bg-grisDegrade.p-4.rounded
        p.me-0.mb-0.text-center.text-bold {"nombreUsuario":"Ana","edad":120,"esFalso”: true,"nacimiento":"21010-21-12"} 
    p.mt-5.mb-4 La verificación que mostraría el resultado es:
    .row.justify-content-center.mb-4.mt-4
      .col-2
        img.ms-5(src='@/assets/curso/tema2/exclamacion.svg')
      .col-10.bg-grisDegrade.p-4
        p.ms-5.mb-0.mt-3 No es correcto el formato de la fecha
        p.ms-5.mb-0 Debe ser falso
        p.ms-5.mb-2 debe ingresar un valor correcto para la edad   
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
