FROM maven:3.6.3-openjdk-11 AS build

WORKDIR /build
COPY . .
RUN rm -rf target/*.war
RUN mvn package war:war
RUN mv target/*.war /tmp/puzzle15.war

FROM tomcat:jre8-alpine
WORKDIR /usr/local/tomcat/webapps
COPY --from=build /tmp/puzzle15.war .
