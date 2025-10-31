# openshift_cluster_settings

Manage an OpenShift cluster using GitOps (ArgoCD)

## 1 - Install ArgoCD

https://docs.redhat.com/en/documentation/red_hat_openshift_gitops/


## 2 - User management prerequisites

ArgoCD default configurations will give Argo Admin role to the group "cluster-admins".

1. Create user and password with htpasswd, and provide cluster-admin to it - view comments in [prerequisites/user_management/1-htpasswd-secret.yaml](prerequisites/user_management/1-htpasswd-secret.yaml), edit, then apply:
  
-  `oc apply -f prerequisites/1-user_management`


 ## 3 - Manage all files in [gitops/infra](gitops/infra) and [gitops/app-of-apps](gitops/app-of-apps) by ArgoCD

1. Creates:
   - ArgoCD project
   - Connects to https://github.com/MooseStack/openshift_cluster_settings.git
   - ArgoCD ApplicationSet to track gitops/infra/<any folder here> folder
   - app-of-apps parent application pattern to track gitops/app-of-apps/*
  
     - `oc apply -f prerequisites/2-argo_bootstrap`