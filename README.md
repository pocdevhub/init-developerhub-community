helm repo add redhat-developer https://redhat-developer.github.io/rhdh-chart

helm upgrade -i rhdh-community redhat-developer/backstage --values dev-hub-community-values.yaml -n poc-developer-hub
