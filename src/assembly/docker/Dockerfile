FROM openjdk:11-jre-slim@sha256:9223f8e5033f47c86323d31aa98a3779c4edd89d92194287f04e2f5391fd9ac1

ENV JAVA_TOOL_OPTIONS=""
ENV SERVER_PORT=8080

COPY ${project.build.finalName}.jar /${project.build.finalName}.jar

EXPOSE 8080

RUN adduser --system exec

USER exec

ENTRYPOINT ["java", "-Djava.security.egd=file:/dev/./urandom", "-jar", "/${project.build.finalName}.jar"]
