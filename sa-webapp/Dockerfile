FROM maven:3.5-jdk-8-alpine
# Environment Variable that defines the endpoint of sentiment-analysis python api.
ADD . /
RUN mvn install
EXPOSE 8080
CMD ["java", "-jar", "target/sentiment-analysis-web-0.0.1-SNAPSHOT.jar", "--sa.logic.api.url=http://sa-logic"]