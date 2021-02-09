# IOT Stack

## Kubernetes installation
This example is created with Rancher k3s because it can be run in light system like a Raspberry Pi.

### K3s installation
Start up the cluster
```bash
curl -sfL https://get.k3s.io | sh -s - --docker
```

Download the latest Kubectl version. Kubectl is a client working with Kubernetes, so it must be linked to k3s:
```bash
sudo chown $(whoami) /etc/rancher/k3s/k3s.yaml
export KUBECONFIG=/etc/rancher/k3s/k3s.yaml
```

Finally, test the installation:
```bash
$ kubectl get nodes
NAME      AGE
pc        3m
```

This example works with one worker but they cant be added easily. 

Now, create the namespace iot and start to install the system.
```bash
kubectl create namespace iot
```
