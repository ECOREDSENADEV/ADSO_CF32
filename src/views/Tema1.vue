<template lang="pug">
.curso-main-container.pb-3
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5

    //- El componente "Muestras" tiene las aplicaciones de todos los componentes de la base
    //- se encuentra en src/components/Muestras.vue
    //- Una vez el componente "Muestras" no se necesite 
    //- Se debe borrar el "import Muestras from '../components/Muestras'" y en "components" en "<script"
    //- esto evitará que se compile en la carpeta final de distribución
    //- Muestras

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
          img(src='@/assets/curso/tema1/teclado.png')
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
    img.mt-5(src='@/assets/curso/tema1/codigo1.svg')

    .row.mt-5.mb-5.bg-color-gris
      .col-5
          img(src='@/assets/curso/tema1/imagen2.jpg')
      .col-7.mt-4
        .row
          .col-12.bgBlanco.Neg-Der50
            .cajon.mb-4
              span.mb-0.text-small  Se invita a revisar en los anexos el archivo de configuración mostrado anteriormente para que pueda ser descargado y utilizado en la construcción de su proyecto, teniendo en cuenta que debe editar las propiedades de acuerdo con sus necesidades.

        p.mt-4.mb-4.text-small Luego de esto se requiere definir todas las Entity Classes que serán utilizadas por Hibernate para realizar el proceso de mapeo hacia una base de datos relacional y viceversa. Una Entity Class básicamente es una clase Java tradicional que tiene las mismas características definidas una tabla de la base de datos, es decir, es una imagen de la tabla (ver siguiente figura) pero desde la perspectiva de la programación orientada a objetos que adicionalmente tiene unas anotaciones especiales que le permiten a Hibernate realizar el trabajo adecuado.
    img(src='@/assets/curso/tema1/grafica2.jpg')

    .row.bgbitsGrande
      .col-12
        .cajon.color-acento-botones.p-4.mb-4.mt-4
          p Las anotaciones pueden ser utilizadas al importar la librería de persistencia de Java javax.persistence.*, entre las más utilizadas encontramos:

        .row.align-items-center.p-5
          .col-12
            .tabla-c
              table
                thead.text-center.text-bold.mb-0.Text-grande
                  th Anotación
                  th Significado
                tr.Text-mediano
                  th @Entity
                  td 
                    p Especifica que la clase definida en una Entity Class
                tr.Text-mediano
                  th @Table(name = “ ”)
                  td 
                    p Permite especificar que la clase será mapeada con una tabla en la base de datos especificada en la propiedad name.
                tr.Text-mediano
                  th @Column(name = “ ”)
                  td 
                    p Permite especificar que el atributo por ser definido será mapeado con una columna especificada por la propiedad name. Cuando el nombre del atributo coincide con el nombre de la columna en la tabla se puede omitir la especificación de la propiedad name y solo dejar la anotación @Column
                tr.Text-mediano
                  th @Id
                  td 
                    p Permite especificar que el atributo a definir corresponde con el identificador primario a ser mapeado en la tabla.
        img(src='@/assets/curso/tema1/clasesJAVA.png')
        p.mt-4.mb-4 A continuación, se muestra un corto video donde se agrega el archivo de configuración de Hibernate al proyecto y se crea la clase Entity para la gestión de una tabla en una base de datos MySQL.
    figure.mb-5
      .video
        iframe(width="560" height="315" src="https://www.youtube.com/embed/2L91WMqw96A" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen)
      figcaption Video: Leyenda del video
    .titulo-segundo.color-acento-contenido
      #1_1_oper_basicas.h2 1.1 Operaciones básicas
    .row.mt-5.mb-5.bg-color-gris
      .col-5
          img(src='@/assets/curso/tema1/imagen3.jpg')
      .col-7.mt-4
        .row
          .col-12.bgBlanco.Neg-Der50
            .cajon.mb-4
              span.mb-0.text-small Una vez se tienen registradas todas dependencias, los archivos de configuración de Hibernate y las respectivas clases de entidad se puede utilizar las facilidades ofrecidas por Hibernate para la manipulación de la base de datos de forma transparente por medio de los procesos de mapeo que ofrece este framework.
        p.mt-4.mb-4.text-small Hibernate utiliza principalmente dos clases que debemos utilizar, las cuales se describen a continuación:
        .row.align-items-center.mb-4
          .col-12
            .tabla-a
              table
                thead.text-center.text-bold.mb-0.Text-mediano.bgBlanco
                  th Class
                  th Descripción
                tr.Text-small.bgBlanco
                  th SessionFactory
                  td 
                    p Esta clase lee el archivo de configuración de Hibernate y crea los objetos de sesión. Por ser una clase que genera objetos pesados por los procesos de los que es responsable solo debo crearlo una vez por toda la aplicación.
                tr.Text-small
                  th Session
                  td 
                    p Esta clase envuelve todo lo correspondiente a una conexión JDBC y es el tipo de objeto que será usado para guardar o recibir objetos desde y hacia la base de datos. Es instanciado a partir de una clase SessionFactory. Los objetos creados de este tipo son más livianos por lo que pueden ser creados y desechados tantas veces como se necesite dentro de la aplicación.
    .cajon.color-acento-botones.p-4.mb-4.mt-4
      p En el siguiente fragmento de código se muestra un esqueleto de como es el proceso de definición de los objetos SessionFactory y Session para poder hacer la manipulación de la base de datos.
    .row.mt-4.mb-4
      .col-7
        img(src='@/assets/curso/tema1/codigo2.svg')
      .col-5
        img(src='@/assets/curso/tema1/imagen4.jpg')
    p.mb-4 Note que en el código anterior para creación del objeto SessionFactory se indica el nombre del archivo de configuración de Hibernate en método configure(), si este parámetro no se incluyera Hibernate buscará en el directorio raíz del proyecto un archivo que contenga el nombre por defecto de este tipo de archivos de configuración el cual es hibernate.cfg.xml. También note que en el método addAnnotatedClass() se indica la clase de entidad a ser utilizada.

    AcordionA.mb-5(tipo="a" clase-tarjeta="tarjeta tarjeta--azul")
      .row(titulo="Método Save")
        .col-md-12.mb-4.mb-md-0
          p El método save() del objeto Session permite hacer el proceso de inserción de un nuevo registro en la base de datos enviando como parámetro un objeto de tipo entidad con sus valores. La forma correcta de hacer un proceso de inserción de un nuevo registro de una base de datos con un objeto de tipo sesión incluye los siguientes pasos:
        .row.mt-4
          .col-1

          .col-10
            img(src='@/assets/curso/tema1/cuadros.svg')
          .col-1

        .row
          .col-md-12
            figure
              img(src='@/assets/template/tema1/codigo3.svg', alt='Método Save')

      div(titulo="Método Get")
        p.mt-4.mb-4 El método get() del objeto session permite obtener un registro de la base de datos por medio de una consulta por su llave primaria. Este método recibe como parámetro la clase de entidad que será utilizada para hacer el mapeo del registro en la respuesta y un segundo parámetro que corresponde al valor a ser buscado en la llave primaria de la tabla. Este método ofrece como resultado un objeto de la clase de entidad especificado en la invocación del método. La forma correcta de hacer un proceso de consulta de un registro particular por medio de su llave primaria y un objeto de tipo session incluye los siguientes pasos:
        .row.mb-4
          .col-5
            figure
              img(src='@/assets/template/tema1/figuraAcordion1.svg', alt='Método Get')
          .col-7
            .shadow.p-3.mb-2.bg-body.rounded
              .row.align-items-center
                .col-2
                  img.Neg-Der50(src='@/assets/curso/tema1/circuloAcordion1.svg')
                .col-10      
                  p Iniciar una transacción por medio del método beginTransaction()
            .shadow.p-3.mb-2.bg-body.rounded
              .row.align-items-center
                .col-2
                  img.Neg-Der50(src='@/assets/curso/tema1/circuloAcordion2.svg')
                .col-10      
                  p Invocar el método get() de la sesión enviando como parámetro la clase de tipo entidad para hacer mapeo y el valor de la llave primaria a buscar. La invocación de este método requiere de un objeto compatible que reciba el resultado.          
            .shadow.p-3.mb-2.bg-body.rounded
              .row.align-items-center
                .col-2
                  img.Neg-Der50(src='@/assets/curso/tema1/circuloAcordion3.svg')
                .col-10      
                  p.mb-4 Confirmar la transacción realizada por medio del método getTransaction().commit()
        img(src='@/assets/curso/tema1/codigo3.svg')
      div(titulo="Método CreateQuery")
        .row.mt-5.mb-5.bg-color-gris
          .col-5
              img(src='@/assets/curso/tema1/imagen5.jpg')
          .col-7.mt-4
            p.mt-4.mb-4.text-small Hibernate permite el proceso de creación de consultas usando HQL, el cual es una versión especial de Hibernate para establecer consultas SQL pero es orientado a objetos y comprende nociones propias del paradigma orientado a objetos como la herencia, el polimorfismo y las asociaciones. Es importante tener en cuenta que aunque las palabras reservadas y sentencias de SQL no son sensibles a mayúsculas los nombres de las clases y sus atributos usados en HQL si lo son.
            .row
              .col-12.Neg-Der50
                .cajon.color-acento-botones.mb-4.p-3
                  span.mb-0.text-small.mt-4 Para el caso en el que se requiera realizar consultas más avanzadas se puede utilizar la potencia de HQL para establecer las características de los registros a ser consultados, como este tipo de consulta puede producir como resultado más de un registro proveniente de la base de datos es necesario usar el método getResultList(), para poder mapear la respuesta a una lista de objetos java.
        p En la siguiente tabla se muestra algunas de las cláusulas HQL más comúnmente utilizadas, tengo en cuenta que en HQL se hace referencia a las clases de entidad JAVA con sus atributos los cuales son sensibles a mayúsculas y estas sentencias son mapeadas a su equivalente estructura en la base de datos usando los nombres de tablas y atributos los cuales ya no son sensibles a mayúsculas:
        .row.align-items-center.p-5
            .col-12
              .tabla-a
                table
                  thead.text-center.text-bold.mb-0.Text-grande
                    th Sentencia HQL
                    th Equivalente en SQL
                  tr
                    th from 
                      span.marcaAmarilla Usuario
                    td.text-mediano 
                      span SELECT * FROM 
                      span.marca usuario
                  tr
                    th 
                      span from 
                      span.marcaAmarilla Usuario 
                      span u where u.
                      span.marcaAmarilla userName 
                      span  = 'Raul'
                    td 
                      span SELECT * FROM 
                      span.marca usuario 
                      span U WHERE u.
                      span.marca username 
                      span = ‘Raul’

                  tr
                    th from 
                      span.marcaAmarilla DomesticCat 
                      span cat order by cat.
                      span.marcaAmarilla name 
                      span asc
                    td 
                      span SELECT * FROM 
                      span.marca domesticCat 
                      span Cat ORDER BY Cat. 
                      span.marca name 
                      span ASC
                  tr
                    th from 
                      span.marcaAmarilla Cat 
                      span as cat inner join Cat.
                      span.marcaAmarilla mate 
                      span as mate
                    td 
                      span SELECT * FROM 
                      span.marca cat 
                      span cat INNER JOIN 
                      span.marca cat_mate 
                      span mate ON Cat.
                      span.marca id 
                      span = mate.
                      span.marca id
              p.mt-4 Para más información sobre las características y particularidades del lenguaje de consulta de Hibernate HQL se invita a consultar en los anexos la guía oficial de este lenguaje.
              p.mb-4 A continuación, se muestran diferentes ejemplos haciendo uso de consultas por medio de HQL:
              img(src='@/assets/curso/tema1/codigo4.svg', alt='Ejemplo del método CreateQuery')
      div(titulo="Actualizaciones")
        p.mb-4 El proceso de actualización es muy similar al proceso de consulta ya que se puede hacer uso directo de los objetos obtenidos de las clases de entidad por medio de los métodos modificadores de sus atributos (Metodos set()) y confirmar las transacciones realizadas o también se puede hacer uso de createQuery() el cual permite enviar consultas HQL un poco más elaboradas pero asociándolo con el método executeUpdate() para que se reflejen los cambios en la base de datos una vez se confirma la transacción.   
        img.mb-4(src='@/assets/curso/tema1/codigo5.svg', alt='Actualizaciones')
        img(src='@/assets/curso/tema1/codigo6.svg', alt='Ejemplo del método CreateQuery')
      div(titulo="Método Delete")
        .row.mt-5.mb-5.bg-color-gris
          .col-7.mt-4
            .row
              .col-12
                .cajon.color-acento-botones.mb-4.p-3.Neg-Izq
                  span.mb-0.text-small.mt-4 El método delete() del objeto session permite eliminar un registro de la base de datos por medio de un objeto recibido como parámetro para identificar el registro de la tabla a eliminar. La forma correcta de hacer un proceso de eliminación de un registro particular incluye los siguientes pasos:  
                .shadow.p-3.mb-2.bg-body.rounded.ms-5
                  .row.align-items-center
                    .col-2
                      img.Neg-Der50(src='@/assets/curso/tema1/circulodelete1.svg')
                    .col-10      
                      p Iniciar una transacción por medio del método beginTransaction()  
                .shadow.p-3.mb-2.bg-body.rounded.ms-5
                  .row.align-items-center
                    .col-2
                      img.Neg-Der50(src='@/assets/curso/tema1/circulodelete2.svg')
                    .col-10      
                      p Utilizar un mecanismo para obtener una instancia de la clase entidad con el objeto que referencia del registro a eliminar ya sea por medio del método get() o CreateQuery.
                .shadow.p-3.mb-2.bg-body.rounded.ms-5
                  .row.align-items-center
                    .col-2
                      img.Neg-Der50(src='@/assets/curso/tema1/circulodelete3.svg')
                    .col-10      
                      p Invocar el método delete() del objeto de session pasando como parámetro el objeto que referencia el registro a eliminar.
                .shadow.p-3.mb-2.bg-body.rounded.ms-5
                  .row.align-items-center
                    .col-2
                      img.Neg-Der50(src='@/assets/curso/tema1/circulodelete4.svg')
                    .col-10      
                      p Confirmar la transacción realizada por medio del método getTransaction().commit()      
          .col-5
              img(src='@/assets/curso/tema1/imagen6.jpg')
        img.mb-4(src='@/assets/curso/tema1/codigo7.svg')
        img.mb-4(src='@/assets/curso/tema1/codigo8.svg')

    .row.mt-5.mb-5.bg-color-gris.pb-5
      .col-5
          img(src='@/assets/curso/tema1/imagen7.jpg')
      .col-7.mt-5
        .cajon.color-primario.p-4.mb-4.Neg-Der
          span A continuación, se muestran  video de clases practicando cada una de las operaciones básicas necesarias para la realización de un CRUD en una tabla de la base de datos.
          br
          br
          br
        .row.color-azulclaro.ms-2.Neg-Top.cajon
          .col-2.me-0
            img.me-0.mt-2.mb-2(src='@/assets/curso/tema1/play.svg')
          .col-10
            .row.align-items-center
              .col-9
                h3.mb-0.mt-3 Método Save
                p.mb-0 Estimado aprendiz, para profundizar sobre el tema puede consultar el siguiente video.
              .col-3
                a.boton.mb-0.mt-4.me-4.indicador__container(
                  href="https://www.youtube.com/embed/2L91WMqw96A"
                  target="_blank"
                  @mouseover="mostrarIndicador = false"
                )
                  span.Text-mediano Ver
                  i.Text-grande.fas.fa-link
                  .indicador--click(v-if="mostrarIndicador")
        .row.color-azulclaro.ms-2.cajon.mt-3
          .col-2.me-0
            img.me-0.mt-2.mb-2(src='@/assets/curso/tema1/play.svg')
          .col-10
            .row.align-items-center
              .col-9
                h3.mb-0.mt-3 Método CreateQuery
                p.mb-0 Estimado aprendiz, para profundizar sobre el tema puede consultar el siguiente video.
              .col-3
                a.boton.mb-0.mt-4.me-4.indicador__container(
                  href="https://www.youtube.com/embed/2L91WMqw96A"
                  target="_blank"
                  @mouseover="mostrarIndicador = false"
                )
                  span.Text-mediano Ver
                  i.Text-grande.fas.fa-link
                  .indicador--click(v-if="mostrarIndicador")
        .row.color-azulclaro.ms-2.cajon.mt-3
          .col-2.me-0
            img.me-0.mt-2.mb-2(src='@/assets/curso/tema1/play.svg')
          .col-10
            .row.align-items-center
              .col-9
                h3.mb-0.mt-3 Método Delete
                p.mb-0 Estimado aprendiz, para profundizar sobre el tema puede consultar el siguiente video.
              .col-3
                a.boton.mb-0.mt-4.me-4.indicador__container(
                  href="https://www.youtube.com/embed/2L91WMqw96A"
                  target="_blank"
                  @mouseover="mostrarIndicador = false"
                )
                  span.Text-mediano Ver
                  i.Text-grande.fas.fa-link
                  .indicador--click(v-if="mostrarIndicador")
    separador
    .titulo-segundo.color-acento-contenido
      #1_2_asociaciones.h2 1.2 Asociaciones
    .row.mt-5.mb-5.bg-color-gris
      .col-7.mt-4
        p.mt-4.ms-4 Normalmente al desarrollar una aplicación que gestione una base de datos, se requiere mucho más que una única tabla para hacer la gestión de la información en la base de datos, por lo que es común tener modelos de datos con múltiples tablas relacionadas con asociaciones de diferentes tipos y diferentes cardinalidades. Por lo cual es importante establecer en las clases de entidad este tipo de relaciones para que el proceso de mapeo sea coherente. Los tipos de asociaciones más comúnmente utilizadas son las que expresan relaciones uno a uno, relaciones uno a muchos, relaciones mucho a uno y relaciones muchos a muchos.
        .row
          .col-12
            .cajon.color-acento-botones.mb-4.p-3.Neg-Izq
              span.mb-0.mt-4 Para mostrar cada uno de estos casos utilizaremos como referencia el siguiente modelo de datos que ya fue mapeado de forma individualizada y a medida que se agrega una asociación de diferente tipo se establecerán los cambios que debería estar presentes, y que se presenta en la siguiente figura:
      .col-5
          img(src='@/assets/curso/tema1/imagen8.jpg')    
    .row.bgbits.mt-4
      .col-12
        img(src='@/assets/curso/tema1/cuadro2.svg')
      .col-12
    //-tarjetas botones
    .row.mb-5
      .col-sm-6.col-lg-4.mb-4.mb-lg-0.mt-4
        .tarjeta--boton.color-primario.p-4.bordePrimario.a.indicador__container(@click="modal1 = true")
          .indicador--click(v-if="mostrarIndicador")
          .row.justify-content-center.mb-3
            .col-7
              figure
                img(src='@/assets/componentes/tema1/onetoone.svg', alt='Relaciones OneToOne')

          h3.text-center Relaciones OneToOne

      .col-sm-6.col-lg-4.mb-4.mb-lg-0.mt-4
        //- .tarjeta--boton debe ir acompañado de una de una de estas clases => 
        //- .color-primario, .color-secundario, .color-acento-contenido, .color-acento-botones
        //- estas clases tambien tienen un modificador --borde
        .tarjeta--boton.color-primario.bordePrimario.p-4.a.indicador__container(@click="modal3 = true")
          .indicador--click(v-if="mostrarIndicador")
          .row.justify-content-center.mb-3
            .col-7
              figure
                img(src='@/assets/componentes/tema1/manytoone.svg', alt='Relaciones OneToMany')

          h3.text-center Relaciones OneToMany

      .col-sm-6.col-lg-4.mb-4.mb-sm-0.mt-4
        //- .tarjeta--boton debe ir acompañado de una de una de estas clases => 
        //- .color-primario, .color-secundario, .color-acento-contenido, .color-acento-botones
        //- estas clases tambien tienen un modificador --borde
        .tarjeta--boton.color-primario.bordePrimario.p-4.a.indicador__container(@click="modal4 = true")
          .indicador--click(v-if="mostrarIndicador")
          .row.justify-content-center.mb-3
            .col-7
              figure
                img(src='@/assets/componentes/tema1/manytomany.svg', alt='Relación ManyToMany')

            h3.text-center Relaciones ManyToMany

    ModalA(:abrir-modal.sync="modal1")
      .row.mb-5
        .col-3
          h3.mt-5.me-0.color-azulclaro.p-2.mb-0.text-center.text-white Relaciones OneToOne
        .col-9
      .row.mb-5
        .col-4
          img(src='@/assets/curso/tema1/imagen9.jpg')
        .col-8
          p.mt-4 En este tipo de relaciones queremos expresar un vínculo en el que un ejemplar de una tabla tiene relación con un y solo un ejemplar de una segunda tabla. Desde el punto de vista de las bases de datos se creará una relación de integridad referencial vinculando una llave primaria con una llave foránea. Tomando como consideración el modelo de datos presentado anteriormente supongamos que se desea indicar que un usuario tiene asociado un recurso. Para resolver este nuevo requerimiento debemos modificar la clase de entidad de usuario para agregar un nuevo atributo que haga referencia al objeto recurso con el cual está relacionado y agregar la anotación correspondiente llamada @OneToOne de forma que Hibernate haga el mapeo correcto.  El esquema se presenta a continuación en la siguiente figura:
      .row.mb-5
        .col-4
        .col-4
          h3.mt-5.me-0.color-azuloscuro.p-2.mb-0.text-center.text-white.Text-mediano @OneToOne
        .col-4
      .row.bgbits.mt-4
        .col-12
          img(src='@/assets/curso/tema1/cuadro3.svg')
        .cajon.color-acento-botones.mb-4.p-3.mt-5
          span.mb-0.mt-4 Mientras que en la base de datos se debe agregar un nuevo campo foráneo en la tabla usuario que haga referencia a la llave primaria de la tabla recurso para poder establecer la relación, en las clases de tipo entidad bastará con especificar el nuevo atributo del tipo de objeto correspondiente que referencia agregando de la anotación de tipo @OneToOne. Si el campo nuevo requerido en la tabla usuario no existe el mapeador de Hibernate se encargará de agregarlo.

    ModalA(:abrir-modal.sync="modal3")
      .row.mb-5
        .col-4
          h3.mt-5.me-0.color-azulclaro.p-2.mb-0.text-center.text-white Relaciones OneToMany - ManyToOne
        .col-8
      .row.mb-4.bg-color-gris
        .col-12.bgBlanco.mt-2.p-3
          p Las relaciones OneToMany tiene la particularidad de afectar cada una de las entidades vinculadas en la relación y es importante identificar el lugar que es una relación OneToMany y en qué lugar la relación es ManyToOne. 
        .row.mb-4
          .col-7
            p.mt-4 Recordando las reglas de transformación del modelo lógico de una base de datos relacional en este tipo de relaciones se indica que en la tabla del lado de la relación donde la cardinalidad máxima muchos (*) deberá ser transferido como un campo foráneo la llave primaria de la tabla donde la cardinalidad máxima es 1, como se aprecia en la siguiente figura:
          .col-5
            img.Neg-Top30.mb-5(src='@/assets/curso/tema1/imagen10.jpg')

      .row.bgbits
        .col-12
          .row.mb-5
            .col-5
            .col-2
              h3.mt-5.me-0.color-azuloscuro.p-2.mb-0.text-center.text-white.Text-mediano @OneToMany @ManyToOne
            .col-5
          img.Neg-Top30.mb-5(src='@/assets/curso/tema1/cuadro4.svg')
          .cajon.color-acento-botones.mb-4.p-3.mt-5
            .row
              .col-3
                img(src='@/assets/curso/tema1/grafica3.svg')
              .col-9
                span.mb-0.mt-4 Para el caso de las clases de entidad deberá especificarse en la clase donde la cardinalidad máxima es 1, un atributo del tipo lista de la clase de entidad con la que tiene un vínculo @OneToMany, este atributo será de tipo lista porque se está vinculando con varios. En el ejemplo, la entidad usuario se relaciona con varios recursos, es decir un usuario puede estar vinculado con múltiples recursos. Por otra parte, la clase de entidad donde la cardinalidad máxima es muchos deberá especificar un atributo de tipo objeto con la entidad vinculada agregándole la anotación @ManyToOne. En el ejemplo un recurso estará siempre vinculado con un único usuario. Es importante anexar en la entidad de cardinalidad @OneToMany el nombre del atributo en la entidad @ManyToOne que será usada para el mapeo de la asociación por parte de Hibernate. En el ejemplo se le indica en la entidad Usuario que la relación @OneToMany será mapeada usando el atributo user de la entidad @ManyToOne.

    ModalA(:abrir-modal.sync="modal4")  
      .row.mb-5
        .col-4
          h3.mt-5.me-0.color-azulclaro.p-2.mb-0.text-center.text-white Relaciones ManyToMany
        .col-8
      .row.mt-5.mb-5.bg-color-gris
        .col-5
            img(src='@/assets/curso/tema1/imagen11.jpg')
        .col-7.mt-4
          p.mt-4.mb-4.ms-4.text-small Las relaciones ManyToMany obligan a la construcción de una nueva entidad de mapeo en la cual se alojarán las respectivas llaves primarias de las entidades vinculadas por medio de la relación @ManyToMany. Para su correcta implementación deberán agregarse en cada una de las clases entidad un objeto de tipo lista de la entidad a la cual está relacionada etiquetada con la anotación @ManyToMany. Adicionalmente en una de las clases de entidad deberá especificar el objeto de mapeo del otro extremo que será utilizado por Hibernate para realizar la asociación.
          .row
            .col-12.Neg-Der50
              .cajon.color-acento-botones.mb-4.p-3
                span.mb-0.text-small.mt-4 En el ejemplo siguiente, se establece una relación ManyToMany entre la clase Usuario y la clase Recurso por lo cual en cada una de ellas se agrega la correspondiente lista del tipo de entidad a la cual se asocian con la anotación @ManyToMany. En el caso de la clase Usuario se agrega el atributo de tipo lista de Recursos llamado recursos para indicar que un usuario puede estar vinculado con muchos recursos y por el lado de la clase Recursos se agrega una lista de tipo Usuario para indicar que un recurso puede estar vinculado con múltiples usuarios. Adicionalmente la relación entre usuario y recurso se mapea con el objeto users presente en la clase Recurso. La relación entre recurso y usuario no se mapea explícitamente por lo que generará la tabla intermedia recurso_usuario, lo cual cumple las reglas de transformación de un modelo lógico para una relación de muchos a muchos.
      .row.bgbits
        .col-12
          .row.mb-5
            .col-5
            .col-2
              h3.me-0.color-azuloscuro.p-2.mb-0.text-center.text-white.Text-mediano.Neg-Top @ManyToMany
            .col-5
          img(src='@/assets/curso/tema1/cuadro5.svg')
    .titulo-segundo.color-acento-contenido
      #1_3_ciclo_vida.h2 1.3 Ciclo de vida
    p.mb-4 Los objetos manipulados por Hibernate para el proceso de gestión de la persistencia pasa por cuatro estados diferentes, a continuación, se describe cada uno de ellos:
    .row.mb-4
      .col-7
        img(src='@/assets/curso/tema1/PCS.svg')
      .col-5
        SlyderF(columnas="col-12")
          .tarjeta.bgBlanco.p-4
            .row.justify-content-center.mb-3
              .col-8
                img(src='@/assets/componentes/tema1/circuloslider1.svg' alt='Estado transitorio')
            h2.text-center Estado transitorio
            p Corresponde al primer estado de un objeto de entidad y sucede cuando instanciamos y manipulamos el objeto de tipo entidad sin conectarlo por medio de la sesión a un registro de la base de datos. Así cualquier manipulación de este objeto no afecta la base de datos. En este estado un objeto de tipo entidad se comporta como cualquier otro objeto JAVA.

          .tarjeta.bgBlanco.p-4
            .row.justify-content-center.mb-3
              .col-8
                img(src='@/assets/componentes/tema1/circuloslider2.svg' alt='Estado persistente')
            h2.text-center estado persistente
            p Corresponde al estado que logra el objeto una vez se conecta con una sesión de Hibernate, lo cual ocurre cuando se invoca por ejemplo una operación de tipo save() o cuando el objeto fue producto de realizar un proceso de consulta a la base de datos por un método get(). Todos los cambios que se realizan sobre un objeto en estado persistente son observados por Hibernate y podrán eventualmente realizar modificaciones en la base de datos.

          .tarjeta.bgBlanco.p-4
            .row.justify-content-center.mb-3
              .col-8
                img(src='@/assets/componentes/tema1/circuloslider3.svg' alt='Estado independiente')
            h2.text-center Estado independiente
            p A este estado pasan los objetos en estado persistentes una vez se realiza un cierre de sesión y en este momento son dejados de observar por Hibernate y cualquier cambio no será propagado en la base de datos. Un objeto independiente puede volver a ser persistente una vez se vuelva a abrir una nueva sesión y se use uno de los siguientes métodos save() o merge().     

          .tarjeta.bgBlanco.p-4
            .row.justify-content-center.mb-3
              .col-8
                img(src='@/assets/componentes/tema1/circuloslider4.svg' alt='Estado eliminado')
            h2.text-center Estado eliminado
            p Es el último estado en el ciclo de vida de un objeto de tipo entidad y ocurre cuando el objeto en cuestión es eliminado de la base de datos por medio del método delete(). Cualquier cambio realizado sobre este objeto no afectará la base de datos.
    .cajon.color-acento-botones.mb-4.p-3.mt-5
      span.mb-0.mt-4 A continuación, se muestra un resumen de los estados del ciclo de vida y sus transiciones completas con todos los posibles métodos.
    img.mb-4.mt-4(src='@/assets/curso/tema1/estadosCicloVida.svg' alt='Estado del ciclo de vida')

</template>

<script>
export default {
  name: 'Tema1',
  components: {},
  data: () => ({
    mostrarIndicador: true,
    modal1: false,
    modal3: false,
    modal4: false,
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
