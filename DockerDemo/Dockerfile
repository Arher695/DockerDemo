FROM eclipse-temurin:17-jre-alpine

# Создаём непривилегированного пользователя (best practice)
RUN addgroup -g 1001 -S appuser && \
    adduser -u 1001 -S appuser -G appuser

USER appuser

EXPOSE 8080

COPY target/DockerDemo-0.0.1-SNAPSHOT.jar app.jar

CMD ["java", "-jar", "app.jar"]