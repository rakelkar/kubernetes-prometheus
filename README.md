# kubernetes-prometheus
Configuration files for setting up prometheus monitoring on Kubernetes cluster.

You can find the full tutorial from here https://devopscube.com/setup-prometheus-monitoring-on-kubernetes/

## port forward
kubectl port-forward $(kubectl get  pods --selector=app=prometheus-server -n  monitoring --output=jsonpath="{.items..metadata.name}") -n monitoring  8080:9090

