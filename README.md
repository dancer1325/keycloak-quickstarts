# Keycloak Quickstarts

* goal
  * examples about securing applications -- via -- Keycloak
    * | DIFFERENT programming languages (& frameworks) 
  * how to extend the server capabilities -- through -- a set of Java-based [Service Provider Interfaces(SPI)](https://www.keycloak.org/docs/latest/server_development/) 

| Category  | Description                                                                           |
|-----------|---------------------------------------------------------------------------------------|
| [extension](extension/) | how to extend the server capabilities -- via -- Keycloak SPIs |
| [jakarta](jakarta/)   | how to secure Jakarta Applications                                        |
| [js](js/)        | how to secure JavaScript Applications                                  |
| [nodejs](nodejs/)    | how to secure NodeJS Applications                                      |
| [spring](spring/)    | how to secure Spring Applications                                      |
| Quarkus    | how to secure Quarkus Applications <br/> [Secure a Client Application](https://quarkus.io/guides/security-oidc-code-flow-authentication-tutorial) <br/>  [Secure a Resource Server Application](https://quarkus.io/guides/security-oidc-bearer-token-authentication-tutorial) |

## Building, Testing, and Running the Quickstarts

* | EACH quickstart,
  * see README.md

### Chrome driver version

TODO: 

Some automated tests rely on the chrome browser present on your laptop
* Also you need to have correct version of chrome driver according
to the version of the chrome browser used
* In case of the issues, see [Chrome page](https://googlechromelabs.github.io/chrome-for-testing/) and download
correct chrome driver version for your Chrome browser
* Then add system property `webdriver.chrome.driver` when running the tests according to chrome version
and add whole path to the chrome driver
* For instance something like `-Dwebdriver.chrome.driver=/somedir/chromedriver-linux64-119.0.6045.105/chromedriver`.
