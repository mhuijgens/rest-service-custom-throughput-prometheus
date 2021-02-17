# rest-service-custom-throughput-prometheus
A simple rest service combined with some custom http throughput metrics on the /greeting endpoint. The rest service is an example that can be found on Spring.io
I just added some java classes & 2 dependencies to add custom throughput metrics for performance testing purposes (Autoscaling & to increase my knowledge about how rest applications work).

1. Start the app with cmd java -jar target/rest-service-0.0.1-SNAPSHOT.jar
2. Find the prometheus metrics by checking http://localhost:8080/actuator/prometheus
3. Call the /greeting endpoint (or customise the response by calling GET http://localhost:8080/greeting?Name=YOURNAME
4. The custom custom_throughput_greeting metric will increase when your load is increased. Use any loadtesting tool (e.g. JMeter)
5. Happy testing!

