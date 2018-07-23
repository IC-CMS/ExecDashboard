FROM openjdk:8-alpine
VOLUME /var/app/config
COPY core-target/exec-core.jar /var/app/core.jar
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/var/app/core.jar"]
CMD [ "--spring.config.location=/var/app/config/application.properties" ]
