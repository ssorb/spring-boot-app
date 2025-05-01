# spring-boot-app
Test app exposing JVM metrics at /actuator/prometheus (built from des-felins/spring-boot-k8s-demo)

In minikube env:

minikube service spring-boot-app --url
http://127.0.0.1:61686
❗  Because you are using a Docker driver on darwin, the terminal needs to be open to run it.

curl http://127.0.0.1:61686
Hello Kubernetes!% 

curl http://127.0.0.1:61686/actuator/health
{"status":"UP","groups":["liveness","readiness"]}% 

curl http://127.0.0.1:61686/actuator/prometheus
(see prom_output.txt for sample output)
