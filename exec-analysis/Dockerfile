FROM openjdk:8-alpine
VOLUME /var/app/config
COPY analysis-target/exec-analysis.jar /var/app/analysis.jar
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/var/app/analysis.jar"]
CMD [ "--spring.config.location=/var/app/config/application.properties" ]
