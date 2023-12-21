# TP : Mise en place d’un outil d’analyse de Code
Redigez un docker-compose afin de mettre en place sonarQube et SonarScanner, sur votre projet.

# TP : Mise en place d'une Application Microservices avec Kubernetes et Monitoring

## Tâche 1 : Déploiement d'une Application Microservices sur Kubernetes

### Conception d'une Application Microservices :
* Développez une application simple composée de plusieurs microservices (vous pouvez reprendre votre PA, le but étant d’inclure une multitude de micro-services.). 
* Chaque microservice doit être conteneurisé à l'aide de Docker. 

### Déploiement sur Kubernetes :
* Utilisez Minikube ou un autre outil pour créer un cluster Kubernetes.
* Déployez chaque microservice dans le cluster Kubernetes en tant que déploiement distinct. (chaque micro service disposera de son propre fichier “deployment”, et chaque conteneur tournera dans un pod distinct).
* Créez des namespaces adaptés aux micro services utilisés.
* Utilisez des ConfigMaps et des Secrets pour gérer la configuration.
* Mettez en place des services pour exposer vos pods sur l’extérieur, et
assurer la communication entre pods.

## Tâche 2 : Intégration Continue et Déploiement Continue (CI/CD)

### CI/CD avec GitHub Actions :
* Créez un pipeline CI/CD qui construit des images Docker pour chaque
microservice.
* Intégrez des tests unitaires dans le pipeline.
 
## Tâche 3 : Monitoring et Logging
Mise en place de Prometheus et Grafana pour le Monitoring :
* Déployez Prometheus dans le cluster Kubernetes pour collecter des
métriques des microservices et du cluster.
* Utilisez Grafana pour créer des tableaux de bord visualisant les
performances et la santé des microservices et du cluster.

## Tâche 4 : Mise en place d'un Système d'Alerte et de Recovery
Alertes avec Prometheus et Grafana :
* Configurez des alertes pour surveiller la santé des microservices (par
exemple, temps de réponse, taux d'erreur). Vous pouvez par exemple créer une alerte si le nombre de pods en cours est inférieur à une valeur définie.
* Testez les alertes en créant des scénarios de défaillance.
