## DistributionSystem Architecture(AWS)

## MSA Stack
- API & ERD 설계 Tool
  - OpenAPI3.0 - openapi generator plugin (https://www.openapis.org/)
  - ERDCloud & MySQL WorkBench(Reverse engineering)
- Application : SpringBoot 2.6.x / Kotlin 1.6 (OpenJDK17)
- Project 구성방식
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


