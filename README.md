`helm repo add redhat-developer https://redhat-developer.github.io/rhdh-chart`

`git clone https://github.com/pocdevhub/init-developerhub-community.git`

`cd init-developerhub-community`

`helm upgrade -i rhdh-community redhat-developer/backstage --values dev-hub-community-values.yaml -n poc-developer-hub`


Emc aso de erro:
> 0/11 nodes are available: persistentvolumeclaim "rhdh-community-audit-log" not found. preemption: 0/11 nodes are available: 11 Preemption is not helpful for scheduling..

Criar o mesmo
