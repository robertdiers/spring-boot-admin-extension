# spring-boot-admin-extension
easy steps to extend app with spring-boot-admin to monitor itself (local and development stages)


## steps to include spring boot admin

1. extend configuration - please check application.yml

2. add dependencies (server and client - I don't think that client is required if server is configured correctly)
```
        <dependency>
			<groupId>de.codecentric</groupId>
			<artifactId>spring-boot-admin-starter-server</artifactId>
			<version>${spring.boot.admin.version}</version>
		</dependency>
		<dependency>
			<groupId>org.springframework.cloud</groupId>
			<artifactId>spring-cloud-starter</artifactId>
			<version>${spring.cloud.version}</version>
		</dependency>
```
```
        <dependency>
			<groupId>de.codecentric</groupId>
			<artifactId>spring-boot-admin-starter-client</artifactId>
			<version>2.4.1</version>
		</dependency>
```

3. add annotation
```
@EnableAdminServer
```

4. start app and open
```
http://localhost:8080/
```

## issues

static content seems to be ignored when activating the admin...