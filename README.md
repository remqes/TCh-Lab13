<h2>Laboratorium programowania aplikacji w chmurach obliczeniowych.</h2>

###P13.1. Wykorzystując przytoczone w instrukcji przykłady zarządzania wdrożeniem, należy:
- utworzyć dwa obrazy (udostępnione w środowisku DockerHub) wyświetlające poprzez stronę internetową informację o wersji obrazu (należy nadać obrazom dwie dowolnie wybrane nazwy),
- uruchomić obiekt Deployment działający z 3 podami z obrazem w pierwszej wersji ([deployment.yaml](/deployment.yaml)),
- przeskalować aplikację do pracy na 6 podach ([deployment2.yaml](/deployment2.yaml)),
- zaktualizować aplikację do nowej wersji obrazu - drugi z obrazów z DockerHub-a ([deployment3.yaml](/deployment3.yaml)),
- przydzielić aplikacji zasoby w dowolnie wybranej wielkości (CPU i MEMORY) ([deployment4.yaml](/deployment4.yaml)),
- wykonać downgrade aplikacji do pierwszej wersji,
- udowodnić, że aplikacja pracowała na pierwszej wersji, a potem na drugiej i znów na pierwszej (zrzuty ekranu poniżej).

Dwa obrazy nginx w dwóch wersjach (latest i stable):
[nginx.stable](https://hub.docker.com/layers/232832274/michalnurz/labox/nginx.stable/images/sha256-62accd5c832bf46871dfd604f86db86a8d2e0e9e4a376c4a05469718a56702d4?context=repo) |
[nginx.latest](https://hub.docker.com/layers/232832506/michalnurz/labox/nginx.latest/images/sha256-25dedae0aceb6b4fe5837a0acbacc6580453717f126a095aa05a3c6fcea14dd4?context=repo)

[deployment1](/images/deployment1.PNG)
[deployment2](/images/deployment2.PNG)
[deployment3](/images/deployment3.PNG)
[deployment4](/images/deployment4.PNG)
[deployment5](/images/deployment5.PNG)


<h2>Dodatkowe zadanie</h2>
Wykorzystując przykłady z poprzednich (szczególnie dwóch) slajdów należy:
- opracować plik konfiguracyjny dla obiektu Deployment ([client-deployment](/lab13Add/client-deployment.yaml), [server-deployment](/lab13Add/server-deployment.yaml), [worker-deployment](/lab13Add/worker-deployment.yaml))
- opracować plik konfiguracyjny dla obiektu ClusterIP Service ([client-cluster-ip](/lab13Add/client-cluster-ip-service.yaml), [server-cluster-ip](/lab13Add/server-cluster-ip-service.yaml))
- wdrożyć w/w obiekty w klastrze Kubernetes (minikube)
- za pomocą poznanych poleceń udowodnić poprawność wykonanych konfiguracji

[deployment6additional](/images/deployment6additional.PNG)