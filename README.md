
Tutorial de SDN usando Opendayligth como Controlador SDN
========================================================

Éste tutorial esta dirigido a estudiantes, profesionales e interesados en el tema de SDN. Las referencias para la implementación de los ejercicios son: [our tutorial](http://sdnhub.org/tutorials/opendaylight/).

Aquí definimos cada directorio usado para construir el controlador SDN, así como algunas aplicaciones SDN
============================================================================================================

* pom.xml: El POM en el principal directorio especifíca a todos los sub-POMs para ser construidos.
* commons/parent: Contiene los "parent" pom.xml con todas las propiedades definidas para los Subprojects.
* commons/utils: Contiene las utilidaddes personalizadas construidas para la programación en OpenFlow.
* learning-switch: Aplicación SDN para L2 hub / switch
* tapapp: Aplicación SDN para el monitoreo de tráfico TAP 
* features: Define dos características del tutorial "Learning-Switch" y "TapAPP" que pueden ser cargados al controlador
* distribution/karaf-branding: Contiene el Karaf para SDN Hub.
* distribution/opendaylight-karaf: Contiene los paquetes relevantes para generar una ejecución en el directorio.

Pasos para construir el controlador
===================================

Con la finalidad de construir el controlador, es necesario tener JDK 1.8 y Maven 3.2+. Los siguientes comandos son usados para construir y ejecutar el controlador: 
```
$ mvn clean install
$ cd distribution/opendaylight-karaf/target/assembly
$ ./bin/karaf
karaf>feature:install sdnhub-XYZ
```
