FROM openjdk:8-alpine
EXPOSE 8080
VOLUME /var/app/config
COPY api-target/exec-api.jar /var/app/api.jar
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/var/app/api.jar"]
CMD [ "--spring.config.location=/var/app/config/application.properties" ]
