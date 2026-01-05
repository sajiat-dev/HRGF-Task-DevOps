# HRGF-Task-DevOps
HRGF DevOps Assessment Task Solution 

High level solution plan and architecture diagram

```mermaid
flowchart LR
    Dev[Developer]

    Dev -->|Push Code| GH[GitHub Repository]

    GH -->|Trigger| GA[GitHub Actions CI/CD]

    GA -->|Build Docker Image| Docker[Docker Build]
    Docker -->|Push Image| ECR[AWS ECR]

    GA -->|kubectl / Helm Deploy| EKS[Amazon EKS Cluster]

    subgraph AWS Cloud
        ECR
        EKS
    end

    subgraph Infrastructure
        TF[Terraform]
        TF -->|Provision| EKS
        TF -->|Provision| ECR
    end
