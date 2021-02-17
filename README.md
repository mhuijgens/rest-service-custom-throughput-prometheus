# rest-service-custom-throughput-prometheus
A simple rest service combined with some custom http throughput metrics on the /greeting endpoint

1. Start the app with cmd java -jar target/rest-service-0.0.1-SNAPSHOT.jar
2. Find the prometheus metrics by checking http://localhost:8080/actuator/prometheus
3. Call the /greeting endpoint (or customise the response with /greeting?Name=YOURNAME
4. The custom custom_throughput_greeting metric will increase when your load is increased. Use any loadtesting tool (e.g. JMeter)
5. Happy testing!

