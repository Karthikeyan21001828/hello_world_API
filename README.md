# Create an API to print HELLO WORLD
## AIM:
to Create an API to print HELLO WORLD using sping boot.
## PROCEDURE:
### STEP 1:


## PROGRAM:
### HelloworldApplication.java
```
package com.spring.helloworld;
import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;
@SpringBootApplication
public class HelloworldApplication {
	public static void main(String[] args) {
		SpringApplication.run(HelloworldApplication.class, args);
	}
}
```
### HelloController.java
```
package com.spring.helloworld.controller;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RestController;
@RestController
public class HelloController {
    @GetMapping("/hello")
    public String helloWorld() {
        return "Hello, World!";
    }
}
```
### build.gradle
```
plugins {
	id 'java'
	id 'org.springframework.boot' version '3.1.0'
	id 'io.spring.dependency-management' version '1.1.0'
}
group = 'com.spring'
version = '0.0.1-SNAPSHOT'
java {
	sourceCompatibility = '17'
}
repositories {
	mavenCentral()
}
dependencies {
//	implementation 'org.springframework.boot:spring-boot-starter-data-jpa'
	implementation 'org.springframework.boot:spring-boot-starter-web'
//	runtimeOnly 'org.postgresql:postgresql'
	testImplementation 'org.springframework.boot:spring-boot-starter-test'
}
tasks.named('test') {
	useJUnitPlatform()
}
```
## OUTPUT:
![image](https://github.com/Karthikeyan21001828/hello_world_API/assets/93427303/6aee656e-134d-4f14-879e-ce327a878e69)

## RESULT:
An API to print HELLO WORLD using sping boot has been executed successfully.
