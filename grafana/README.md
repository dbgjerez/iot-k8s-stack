helm repo add grafana https://grafana.github.io/helm-charts
helm repo update

helm install -f values.yml -n iot grafana grafana/grafana
