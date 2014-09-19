OpenShift CAS Quickstart
========================
Apereo CAS running on Tomcat 7 (JBoss EWS) cartridge.

What is it?
-----------
[Apereo CAS](https://github.com/Jasig/cas) (Central Authentication Service) is a open source Single Sign On solution for the web. visit CAS's documentation [here](http://jasig.github.io/cas/4.0.0/index.html). 

The web application is built using Maven WAR Overlay Method, which allows developers to override / merge with the original war with minimum code duplication. For more information about Maven Overlay visit the [Maven Overlay Plugin Documentation](http://maven.apache.org/plugins/maven-war-plugin/overlays.html)

Running on openshift
--------------------
Create the application via rhc client 
`rhc app create cas jbossews-2.0 --from-code https://github.com/adrianchia/openshift-cas-quickstart.git`

or add it from the Openshift web console:

1. Click on **Add Application...** button
2. Click on **Tomcat 7 (JBoss EWS 2.0)** under Java section
3. give your application a name (e.g. cas) and point the source code URL to **https://github.com/adrianchia/openshift-cas-quickstart.git**
4. Click **Create Application** and wait for the application creation to finish.
5. visit your CAS application at **https://cas-{yourdomain}-rhcloud.com**

The default username/password for CAS 4.0 is casuser/Mellon. see [this link](https://github.com/Jasig/cas/blob/master/cas-server-webapp/src/main/webapp/WEB-INF/deployerConfigContext.xml#L107) for more information

What's Next
-----------
* Customize your own authentication mechanism (e.g. RDBMS, OAuth, etc)
* Customize your own UI

License
-------
openshift-cas-quickstart is licensed under [Apache License 2.0](http://www.apache.org/licenses/LICENSE-2.0). A copy of this license is available under the *LICENSE* file.

Apereo CAS is licensed under [Apache License 2.0](http://www.apache.org/licenses/LICENSE-2.0), see [here](https://github.com/Jasig/cas) for more information.