FROM dockerfile/java:oracle-java8

VOLUME /tmp
ADD cresoty.jar /opt/cresoty/
EXPOSE 8080
WORKDIR /opt/cresoty/
CMD ["java", "-Djava.security.egd=file:/dev/./urandom", "-Xms512m", "-Xmx1g", "-jar", "cresoty.jar"]
