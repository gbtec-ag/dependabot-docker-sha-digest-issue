FROM openjdk:11-jre-slim@sha256:fb760b3216c7bac47a131ec031d8864c82b9de12717a96d32b874d2e59132576

ENV JAVA_TOOL_OPTIONS=""
ENV SERVER_PORT=8080

COPY ${project.build.finalName}.jar /${project.build.finalName}.jar

EXPOSE 8080

RUN adduser --system exec

USER exec

ENTRYPOINT ["java", "-Djava.security.egd=file:/dev/./urandom", "-jar", "/${project.build.finalName}.jar"]
