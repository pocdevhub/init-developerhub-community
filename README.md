`helm repo add redhat-developer https://redhat-developer.github.io/rhdh-chart`

`git clone https://github.com/pocdevhub/init-developerhub-community.git`

`cd init-developerhub-community`

`helm upgrade -i rhdh-community redhat-developer/backstage --values dev-hub-community-values.yaml -n poc-developer-hub`


Emc aso de erro:
> 0/11 nodes are available: persistentvolumeclaim "rhdh-community-audit-log" not found. preemption: 0/11 nodes are available: 11 Preemption is not helpful for scheduling..

Criar o mesmo


NOTAS:
Para o argo conseguir fazer deploy foi preciso fazer as seguinte alterações no objeto
argocd-rbac-cm
    `p, role:admin, applications, *, */*, allow
    p, role:admin, clusters, get, */*, allow
    p, role:admin, repositories, get, */*, allow`

https://argo-cd.readthedocs.io/en/stable/operator-manual/rbac/


Atribuir cluster role de admin  
    system:serviceaccount:poc-ktools:argocd-argocd-application-controller

https://docs.openshift.com/gitops/1.14/accesscontrol_usermanagement/configuring-argo-cd-rbac.html

Tem que se garantir que se consiga fazer deploy somente nos namesapces do ESB!