`helm repo add redhat-developer https://redhat-developer.github.io/rhdh-chart`
`git clone https://github.com/pocdevhub/init-developerhub-community.git`
`cd init-developerhub-community`
`helm upgrade -i rhdh-community redhat-developer/backstage --values dev-hub-community-values.yaml -n poc-developer-hub`
