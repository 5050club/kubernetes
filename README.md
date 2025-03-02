# kubernetes


# Create k3d cluster

https://k3d.io/v5.4.7/usage/exposing_services

Cluster must be created mapping localhost ports to ingress ports

> k3d cluster create 5050club -p "5601:5601@loadbalancer" -p "9200:9200@loadbalancer"

Then run

> export KUBECONFIG="$(k3d kubeconfig write 5050club)"