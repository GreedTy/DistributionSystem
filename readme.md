## 분산시스템 in AWS
- IaC(Infrastructure as Code) Tool: Terraform(HashiCorp-HCL/https://registry.terraform.io)
![아키텍처](https://user-images.githubusercontent.com/35190067/194558779-f4cc36e1-8ccc-4825-8be6-d5ecf347753d.png)
## MSA Stack
- API & ERD 설계 Tool
  - OpenAPI3.0 - openapi generator plugin (https://www.openapis.org/)
  - ERDCloud & MySQL WorkBench(Reverse engineering)
- Application : SpringBoot 2.6.x / Kotlin 1.6 (OpenJDK17)
- Project 구성방식(https://github.com/GreedTy/MultyModuleService)
  - Multy Module - settings.gradle
    - API & Batch
    - Layer
      - core / dao / service
    - Gradle Dependency
      - Implementation: SpringSecurity(OAuth2.0), SpringBatch, SpringDataJdbc, WebFlux, kotlinx(reactor, coroutine)
      - Test & Coverage: kotest(junit5, assertion, coroutine, reactor, wiremock) & Jacoco
  - CI/CD: GitAction/ArgoCD 
    - K8S/ECR(Helm/DockerFile)
- Database : AuroraDB
- Monitoring : DataDog
## LoadTest Stack
- Application : Locust / Python 3.8
  - master1/worker5/dashboard
- CI/CD: GitAction/ArgoCD


