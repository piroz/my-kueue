# my-kueue
kueue sample

# setup

## minikube

```
$ brew install minikube
$ minikube start --container-runtime containerd
$ minikube addons enable metrics-server
$ minikube dashboard
```

## kubectl

```
$ brew install kubectl
$ kubectl version --client
```

## kueue

```
$ VERSION=v0.5.3
$ kubectl apply --server-side -f https://github.com/kubernetes-sigs/kueue/releases/download/$VERSION/manifests.yaml
```

### prometheus-operator-crd

```
kubectl apply -f https://raw.githubusercontent.com/coreos/prometheus-operator/release-0.38/example/prometheus-operator-crd/monitoring.coreos.com_servicemonitors.yaml
```
