# rest-service-custom-throughput-prometheus
A simple rest service combined with some custom http throughput metrics on the /greeting endpoint. The rest service is an example that can be found on Spring.io (https://spring.io/guides/gs/rest-service/)
I just added some java classes (src/main/java/com/example/restservice/metrics/) & 2 dependencies to add custom throughput metrics for performance testing purposes (used for autoscaling in the cloud & to increase my knowledge about how rest applications work).

1. Start the app with cmd java -jar target/rest-service-0.0.1-SNAPSHOT.jar
2. Find the prometheus metrics by checking http://localhost:8080/actuator/prometheus
3. Call the /greeting endpoint (or customise the response by calling GET http://localhost:8080/greeting?Name=YOURNAME
4. The custom_throughput_greeting metric value will increase when your load is increased, and decrease when load is decreased. Use any loadtesting tool for this (I like to use JMeter)
5. Happy testing!

