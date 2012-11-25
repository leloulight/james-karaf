james-karaf
===========

Apache James 3.0beta5 deployed inside Karaf container.

Overview
========

~~~
james-karaf  - main project
+- features - defines and installs james-feature as a maven artifact
+- intetgration - contains PAX-EXAM integration tests for deploying james inside Karaf
~~~
This project aims to migrate Apache James to OSGi, particular Karaf.


Build and run
=============

The project builds and publishes a set of Karaf features:
~~~
$mvn clean install 
~~~ 

Inside Karaf-2.3.0 run: 
~~~
features:addurl mvn:org.apache.james/james-features/${version}/xml/features
~~~

Now you can install Apache James features with **features:install**. 