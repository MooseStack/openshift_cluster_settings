# Summary

- [gitops/infra/operators/cert-manager](cert-manager): Certificate management

- [gitops/infra/operators/devspaces](devspaces): Web browser based Integrated Development Environment(IDE). Based on the upstream [Eclipse Che](https://eclipse.dev/che/)

- [gitops/infra/operators/metallb-operator](metallb-operator): Enables "LoadBalancer" type for "Kind: Service"

- [gitops/infra/operators/openshiftai](openshiftai): AI/ML platform based on upstream [[Open Data Hub](https://opendatahub.io/)](https://opendatahub.io/)

- [gitops/infra/operators/pipelines](pipelines): CI/CD tool based on [[Tekton](https://tekton.dev/)](https://tekton.dev/)

- [gitops/infra/operators/serverless-operator](serverless-operator): Based on the upstream [Knative](https://knative.dev/docs/). Similar to AWS Lambda, but for k8s.
  - OpenShift AI is dependent on this for KServe with Serverless model deployments.
  - Kustomize folder structrue is different than the rest due to requirement of separate namespaces, one for operator and other for Knative related Custom Resource Definitions(CRD's).
  
- [gitops/infra/operators/servicemeshoperator3](servicemeshoperator3): Based on the upstream [Istio](https://istio.io/) for service mesh.
  - OpenShift AI is dependent on this for mesh services.

## GPU enabling operators:
- [gitops/infra/operators/kernel-module-management](kernel-module-management): manages, builds, signs, and deploys out-of-tree kernel modules and device plugins. 

- [gitops/infra/operators/nodefeaturediscovery](nodefeaturediscovery): Labels nodes with the detected hardware features and systems, such as PCI cards, kernel, OS versions, etc.
  
- [gitops/infra/operators/amd-gpu-operator](amd-gpu-operator):Collect worker node system specifications, Build or retrieve the appropriate driver image, Deploy the driver using KMM, and Deploy the ROCM device plugin and node labeller