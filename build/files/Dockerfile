FROM maven:3.6.3-openjdk-11 AS build

WORKDIR /build
RUN git clone https://github.com/venkaDaria/puzzle15.git /build
RUN mvn package -DskipTests
RUN mv target/*.war /tmp/puzzle.war

FROM tomcat:jre8-alpine
WORKDIR /usr/local/tomcat/webapps
COPY --from=build /tmp/puzzle.war .
