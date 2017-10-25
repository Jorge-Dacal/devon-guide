Spring boot admin is an application to monitor and manage the different Spring.io applications.There are the different way to configure spring boot admin with spring.io apps. As many features available in it, you can configure as per the project requirement. Please refer the wiki  [[ Spring boot admin Integration with OASP4J|https://github.com/devonfw/devon-guide/wiki/Spring-boot-admin-Integration-with-OASP4J]] , [[ Spring Boot Admin Reference Guide|http://codecentric.github.io/spring-boot-admin/1.5.3/#getting-started]]. 

### Integrate spring boot admin with the module.  
To setup spring boot admin for spring.io project you can refer the above wiki or simply use the module. Please follow below steps to configure the module to OASP4J app.     

### Spring boot Admin server

You can directly check out the Spring boot Admin server from the [[ repo |https://github.com/Himanshu122798/spring-bootadmin-server]] or you can create own using the above reference document. 

###  Configure module to OASP4J app. 
  
  1. Add the dependency in pom.xml file
```xml
  <dependency>
      <groupId>com.capgemini.devonfw.modules</groupId>
      <artifactId>devonfw-springbootadminclient</artifactId>
      <version>2.2.0</version>
  </dependency>
``` 
  2. Add the below property and change the values as per the spring boot admin server configuration like admin.url , username, password 

```java
eureka.client.serviceUrl.defaultZone=${EUREKA_URI:http://localhost:8180/eureka}
spring.boot.admin.url=http://localhost:1111
management.security.enabled=false
spring.boot.admin.username=admin
spring.boot.admin.password=admin123
logging.file=target/${spring.application.name}.log

eureka.instance.hostname=localhost
eureka.client.register-with-eureka=false
eureka.client.fetch-registry=false

health.config.enabled=true 
```

 

 