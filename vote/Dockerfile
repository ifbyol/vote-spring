FROM openjdk:11

WORKDIR /app
COPY . .
RUN /app/mvnw clean package -Dmaven.test.skip=true
COPY /app/target/*.jar app.jar

EXPOSE 8080

ENTRYPOINT ["java", "-jar", "/app/app.jar"]