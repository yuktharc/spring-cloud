# spring-cloud

1.Make sure to be out of VPN connection while testing.
2.Issue CURL request "curl -X POST http://localhost:8080/refresh" against config-client NOT on config-server. So Actuator dependency is also only required at config-client.
3."management.security.enabled=false" is only necessary on config-client app to refresh the properties from config-server
4.When the CURL PORT request is issued on config-client it in turn requests config-server and the config-server refreshes the properties from GitHub (in this case).

