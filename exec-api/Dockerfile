FROM openjdk:8-alpine
VOLUME /var/app/config
COPY api-target/exec-api.jar /var/app/api.jar
COPY application.properties /var/app/config/application.properties
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/var/app/api.jar"]
CMD [ "--spring.config.location=/var/app/config/application.properties" ]
