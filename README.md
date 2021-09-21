# Helmchart einer Open-Source APM Landschaft

Dieses Helmchart wurde parallel zur Bachelorarbeit "Simple Bereitstellung von Open-Source Applikationen zur Überwachung der Anwendungsleistung" geschrieben und beinhaltet folgende Komponenten:

* [InspectIT Ocelot Agent inklusive Konfigurationsserver](https://www.inspectit.rocks/)
* [Spring Petclinic](https://projects.spring.io/spring-petclinic/)
* [Grafana](https://grafana.com/)
* [Prometheus](https://prometheus.io/)
## Installation des Charts
Zur Installation dieses Charts ist ein [Kubernetes Cluster](https://kubernetes.io/) und [Helm](https://helm.sh/) erforderlich. Ist beides vorhanden, muss im Root Ordner dieses Charts folgender Befehl ausgeführt werden:
```$helm install petclinic .```

## Ändern des Hauptprozesses

Sollte ein anderer Java Prozess zum Überwachen verwendet werden, so muss in der [values.yaml](values.yaml) das Image unter image.repository sowie der Name der JAR-Datei unter containers.command angepasst werden. Das neue Image muss die JAR-Datei des neuen Prozesses beinhalten.

