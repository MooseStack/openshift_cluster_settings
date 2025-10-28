# openshift_cluster_settings

Manage an OpenShift cluster using GitOps (ArgoCD)

## 1 - Install ArgoCD

https://docs.redhat.com/en/documentation/red_hat_openshift_gitops/


## 2 - User management prerequisites

ArgoCD default configurations will give Argo Admin role to the group "cluster-admins".

1. Create user and password with htpasswd, and provide cluster-admin to it - view comments in [prerequisites/user_management/1-htpasswd-secret.yaml](prerequisites/user_management/1-htpasswd-secret.yaml), edit, then apply:
  
-  `oc apply -f prerequisites/user_management`


## 3 - Manage all files in [gitops/infra](gitops/infra) by ArgoCD

- `oc apply -f gitops/infra/applicationSet.yaml`