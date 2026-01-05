# HRGF-Task-DevOps
HRGF DevOps Assessment Task Solution 

High level solution plan and architecture diagram

┌────────────┐
│ Code       │
└─────┬──────┘
      ↓
┌────────────┐
│   GitHub   │  (App Code + K8s YAML)
└─────┬──────┘
      ↓
┌──────────────────────────┐
│ GitHub Actions (CI/CD)   │
│ - Build                  │
│ - Test                   │
│ - Docker Build           │
│ - Push the image to ECR  │
│ - Deploy to EKS (kubectl)│
└─────┬────────────────────┘
      ↓
┌────────────┐
│  AWS ECR   │ 
└─────┬──────┘
      ↓
┌──────────────────────────┐
│ Amazon EKS (Kubernetes)  │
└──────────────────────────┘
