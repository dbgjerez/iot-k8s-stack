curl -sfL https://get.k3s.io | sh -s - --docker
sudo chown $(whoami) /etc/rancher/k3s/k3s.yaml
export KUBECONFIG=/etc/rancher/k3s/k3s.yaml
kubectl get nodes
```bash
NAME      AGE
pc        3m
```

kubectl create namespace iot
