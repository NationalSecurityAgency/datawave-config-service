# Config Service

The Config service is an implementation of the Spring Cloud
[config](https://cloud.spring.io/spring-cloud-static/Greenwich.SR3/single/spring-cloud.html#_spring_cloud_config) 
service with some DATAWAVE-specific extensions. In particular, this service
adds the following on top of the default config service provided by Spring
Cloud:

* Encrypted private keys are supported
* Allows for specification of PKCS12 repositories as `.p12` files. The default
  Spring behavior is to take the extension and use it as the keystore type.
  However, Java has no `p12` keystore type, only `pkcs12` and `jks`.
