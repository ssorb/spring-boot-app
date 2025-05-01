# spring-boot-app
Test app exposing JVM metrics at /actuator/prometheus (built from des-felins/spring-boot-k8s-demo)<br/>

In minikube env:<br/>
$ kubectl apply -f deployment.yaml<br/>
$ kubectl apply -f service.yaml<br/>

$ minikube service spring-boot-app --url<br/>
http://127.0.0.1:61686<br/>
❗  Because you are using a Docker driver on darwin, the terminal needs to be open to run it.

$ curl http://127.0.0.1:61686<br/>
Hello Kubernetes!% <br/>

$ curl http://127.0.0.1:61686/actuator/health<br/>
{"status":"UP","groups":["liveness","readiness"]}% <br/>

$ curl http://127.0.0.1:61686/actuator/prometheus<br/>
(see prom_output.txt for sample output)<br/>
