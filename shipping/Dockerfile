#
# Build
#
#FROM debian:10 AS build

#RUN apt-get update && apt-get -y install maven

#WORKDIR /opt/shipping

#COPY pom.xml /opt/shipping/
#RUN mvn dependency:resolve
#COPY src /opt/shipping/src/
#RUN mvn package

#
# Run
#
#FROM openjdk:8-jdk

#EXPOSE 8080

#WORKDIR /opt/shipping

#ENV CART_ENDPOINT=cart:8080
#ENV DB_HOST=mysql

#COPY --from=build /opt/shipping/target/shipping-1.0.jar shipping.jar

#CMD [ "java", "-Xmn256m", "-Xmx768m", "-jar", "shipping.jar" ]


# Build stage
FROM maven:3.8.6-openjdk-11-slim AS build

WORKDIR /opt/shipping

COPY pom.xml .
RUN mvn dependency:resolve
COPY src ./src
RUN mvn package

# Run stage
FROM openjdk:8-jdk

WORKDIR /opt/shipping

ENV CART_ENDPOINT=cart:8080
ENV DB_HOST=mysql

COPY --from=build /opt/shipping/target/shipping-1.0.jar shipping.jar

EXPOSE 8080

CMD ["java", "-Xmn256m", "-Xmx768m", "-jar", "shipping.jar"]


