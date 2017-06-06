# To run Kubernetes on a Laptop

Following tools need to be installed :
1. Kubectl
2. Minikube
3. Docker

### 1. Install Kubectl
*  __On Linux, use the following command__ :
    ```sh
    $ curl -LO https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl && chmod +x kubectl && sudo mv kubectl /usr/local/bin/
    ```

* __On macOS, use the following command__ :
    ```sh
    $ curl -LO https://storage.googleapis.com/kubernetes-release/release/$(curl 
  -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/
  darwin/amd64/kubectl && chmod +x kubectl && sudo mv kubectl /usr/local/bin/
    ```
* __To verify kubectl availability, use the following command__ :
    ```sh
    $ kubectl version
    ```
    Official guide to install kubectl is [here](https://kubernetes.io/docs/tasks/tools/install-kubectl/)
### 2. Install Minikube
* __On Linux, use the following command, for version v0.19.0__ :
    ```sh
    $ curl -Lo minikube https://storage.googleapis.com/minikube/releases/v0.19.0/minikube-linux-amd64 && chmod +x minikube && sudo mv minikube /usr/local/bin/
    ```
* __On macOS, use the following command, for version v0.19.0__ :
    ```sh
    $ curl -Lo minikube https://storage.googleapis.com/minikube/releases/v0.19.0/minikube-darwin-amd64 && chmod +x minikube && sudo mv minikube /usr/local/bin/
    ```
* __To use a specific release, configure minikube__ : 
    ```sh
    $ minikube config set kubernetes-version 1.6.4
    ```
* __To verify minikube availability, use the following command__ :
    ```sh
    $ minikube version
    ```
    Official guide to install minikube is [here](https://github.com/kubernetes/minikube/releases)
### 3. Install Docker
* __Download and install community edition binary from the [docker store.](https://store.docker.com/search?offering=community&type=edition)__
* __To quickly install Docker on Ubuntu 16.04 or higher, use the following command__ :
    ```sh
        $ sudo apt-get update
        $ curl -fsSL https://get.docker.com/ | sh
    ```
* __To quickly install Docker on [other distribution](https://docs.docker.com/engine/installation/)__
* __To verify Docker availability, use the following command__ : 
    ```sh
    $ docker version
    ```
* __To reference minikube's docker daemon from your host, use__ :
    ```sh
    $ eval $(minikube docker-env)
    ```
### Other References :
* Official Kubernetes docs [here](https://kubernetes.io/docs/home/).
* Kubernetes docs on [github](https://github.com/kubernetes/kubernetes/tree/master/docs).

