# manual-spring
for me

### 설치
spring2 + intellij(coummunity)
https://daddyprogrammer.org/post/19/spring-boot2-start-intellij/

spring5 + intellij(coummunity)
https://www.bsidesoft.com/?p=6926

### 설치요약
1. intellij 커뮤니티 설치
2. gradle 수정
```
plugins {
    id 'org.springframework.boot' version '2.1.4.RELEASE'
    id 'java'
}
 
apply plugin: 'io.spring.dependency-management'
 
group = 'com.rest'
version = '0.0.1-SNAPSHOT'
sourceCompatibility = '9'
 
configurations {
    compileOnly {
        extendsFrom annotationProcessor
    }
}
 
repositories {
    mavenCentral()
}
 
dependencies {
    implementation 'org.springframework.boot:spring-boot-starter-data-jpa'
    implementation 'org.springframework.boot:spring-boot-starter-freemarker'
    implementation 'org.springframework.boot:spring-boot-starter-web'
    compileOnly 'org.projectlombok:lombok'
    runtimeOnly 'com.h2database:h2'
    runtimeOnly 'mysql:mysql-connector-java'
    annotationProcessor 'org.projectlombok:lombok'
    testImplementation 'org.springframework.boot:spring-boot-starter-test'
}
```

Lombok
```
settings - plugns - lombok 설치
settings - annotation processeor - enable annotation processor
```
