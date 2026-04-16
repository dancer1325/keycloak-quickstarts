* goal
  * example manifest -- to -- deploy Keycloak | Kubernetes

* [Keycloak | Kubernetes](https://www.keycloak.org/getting-started/getting-started-kube)

# requirements
* download software / enable you to run local Kubernetes clusters
  * [Docker desktop](https://docs.docker.com/get-started/introduction/get-docker-desktop/)
  * [kind](https://kind.sigs.k8s.io/) + [install Kubectl](https://kubernetes.io/docs/tasks/tools/#kubectl)
  * [minikube](https://minikube.sigs.k8s.io/docs/)
    * `kubectl` commands are wrapped -- via -- `minikube kubectl`
  * [microk8s](https://canonical.com/microk8s)
    * `kubectl` commands are wrapped -- via -- `microk8s kubectl`
* run a local Kubernetes cluster
  * -- via -- 
    * [Docker Desktop](https://docs.docker.com/desktop/use-desktop/kubernetes/#enable-kubernetes)
      * | Docker Desktop
        * Kubernetes > Create cluster > choose any cluster type
    * [Kind](https://kind.sigs.k8s.io/#installation-and-usage)
      * `kind create cluster`
    * minikube
      * `minikube start`
    * microk8s
## recommendations
* `kind create cluster`
* [install Cloud Provider KIND](https://kubernetes-sigs.github.io/cloud-provider-kind/#/?id=main)
* `sudo cloud-provider-kind`
  * == run cloud-provider-kind

# how to deploy | Kubernetes locally?
* | this path,
  * `kubectl apply -f keycloak-ingress.yaml`
* `PORT=$(docker ps --format '{{.Ports}}' -f name=kindccm-gw | grep -o '0.0.0.0:[0-9]*->80' | cut -d: -f2 | cut -d- -f1)`
  * extract real ingress' port | variable
  * `echo $PORT`
    * check ingress' real port
* | [keycloak.yaml](keycloak.yaml)
  * set KC_HOSTNAME / real value
* | this path,
  * `kubectl apply -f keycloak.yaml`
* | browser,
  * [keycloak.yaml](keycloak.yaml)'s `KC_HOSTNAME` value
    * _Example:_ http://keycloak.localhost:32778
      * user: admin
      * password: admin
