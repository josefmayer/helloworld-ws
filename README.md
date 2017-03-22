# helloworld-ws: Hello World JAX-WS Web Service


## Technologies
JAX-WS
Wildfly
Arquillian


## Requirements
Wildfly Server
Maven


## Steps
Start a Wildfly Server:
For Linux:   WILDFLY_HOME/bin/standalone.sh
For Windows: WILDFLY_HOME\bin\standalone.bat


Build and Deploy the webservice:
*mvn clean install wildfly:deploy*


Display Deployed WSDL Enpoint:
http://localhost:8080/helloworld-ws/HelloWorldService?wsdl


Undeploy Webservice:
*mvn wildfly:undeploy*


Run a Client Test:
Deploy webservice, creates a webservice-client, run tests with arquillian, undeploy webservice
*mvn clean test -Parq-wildfly-remote*


## original source
<https://github.com/wildfly/quickstart/>



