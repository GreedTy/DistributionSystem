## 분산시스템 in AWS (TIL)
IaC(Infrastructure as Code) - Terraform ([AWS-Infa](https://github.com/GreedTy/terraform-aws-infra))
![아키텍처](https://user-images.githubusercontent.com/35190067/194558779-f4cc36e1-8ccc-4825-8be6-d5ecf347753d.png)

## MSA Component & API, Batch Server Project
- Project 
  - API ([MultyModule - API](https://github.com/GreedTy/MultyModuleService/tree/master/api))
    - API 설계 Tool
      - OpenAPI3.0 openapi generator plugin ([OpenAPI](https://www.openapis.org/))
    - ERD 설계 Tool 
      - ERDCloud & MySQL WorkBench(Reverse engineering) & DataGrip
    - Framework
      - SpringBoot 2.6.x / Kotlin 1.6 (OpenJDK17)
  - Batch ([MultyModule - Batch](https://github.com/GreedTy/MultyModuleService/tree/master/batch))
  - BatchAdmin ([SCDF](https://github.com/GreedTy/scdf-batch-admin))
  - CI/CD
    - GitAction ([GitAction - Yaml](https://github.com/GreedTy/MultyModuleService/blob/master/.github/workflows/deploy-to-apiserver.yml))
    - GitOps ArgoCD ([Helm - ArgoCD](https://github.com/GreedTy/terraform-aws-infra/tree/master/infra/k8s-base-resources/argocd)) 
  - AWS EKS(K8S) & ECR  
    - EKS ([Terraform - AWS EKS](https://github.com/GreedTy/terraform-aws-infra/tree/master/infra/eks-cluster))
    - ECR ([Terraform - AWS ECR](https://github.com/GreedTy/terraform-aws-infra/tree/master/infra/ecr))
  - AWS Aurora RDS MySQL 8.0 ([Terraform - Aurora](https://github.com/GreedTy/terraform-aws-infra/tree/master/infra/database-mysql)) 
    - API common-dao modules in main/replica(CQRS pattern)
  - DataDog ([Helm - DataDog](https://github.com/GreedTy/terraform-aws-infra/tree/master/infra/k8s-base-resources/datadog))
    - Monitoring Tool
## 부하발생기
- Locust ([부하발생기](https://github.com/GreedTy/load-generator))
