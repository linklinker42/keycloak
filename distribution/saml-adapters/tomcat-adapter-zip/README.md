# Keycloak Tomcat SAML Adapter

Tomcat SAML valve adapter to enable container based SAML security. Please see the [Tomcat SAML Adapter Guide](https://www.keycloak.org/docs/latest/securing_apps/#_saml-tomcat-adapter) for official usage information.

The purpose of this fork is to better customize the Tomcat SAML adapter.


### Build
Go to the root of the Keycloak project and run this command (Skip the tests if you don't want to spend all day trying to build. My preference would be that the adapters be a seperate project so that you didn't have to build and test the entire Keycloak server.):
```shell
mvn clean install -Pdistribution -DskipTests=true
```
You will then find the zip distribution under target in this folder.
<br/>

### Environment Variables
| Environment Variable | Description | Default |
| --- | --- | --- |
| KEYCLOAK_GLOBAL_LOGOUT_PATH | Sets the relative URL that will trigger a global logout. This must be a secured path. | /logout |