FROM openjdk:8

RUN git clone https://github.com/maijahaka/web-palvelinohjelmointi-projekti
WORKDIR /web-palvelinohjelmointi-projekti

RUN apt-get update && apt-get install -y maven
RUN mvn package

CMD ["java", "-jar", "./target/wepa_Projekti-1.0-SNAPSHOT.jar"]
EXPOSE 8080
