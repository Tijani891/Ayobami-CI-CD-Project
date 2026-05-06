Here's the reworked README:

```markdown
# microservices-cicd-pipeline

A production-ready CI/CD pipeline for microservices, built with CircleCI, Docker, Kubernetes, and AWS. Features automated linting, security scanning, and support for blue/green and rolling deployment strategies.

---

## Stack

| Tool        | Purpose                            |
|-------------|------------------------------------|
| CircleCI    | Pipeline automation                |
| Docker      | Container builds                   |
| Kubernetes  | Orchestration \u0026 deployment         |
| AWS (ECR/EKS) | Image registry \u0026 cluster hosting |
| Terraform   | Infrastructure as Code             |

---

## Project Structure

```
.
├── .circleci/        # CircleCI pipeline configuration
├── terraform/        # AWS infrastructure definitions
├── k8s/              # Kubernetes manifests (Deployments, Services)
└── Dockerfile        # Container build instructions
```

---

## Getting Started

### Prerequisites

- Docker
- kubectl
- AWS CLI (configured with credentials)
- CircleCI account linked to your repo

### Setup

1. **Clone the repo**
   ```sh
   git clone https://github.com/Tijani891/microservices-cicd-pipeline.git
   cd microservices-cicd-pipeline
   ```

2. **Provision infrastructure**
   ```sh
   terraform init
   terraform apply
   ```

3. **Configure CircleCI** — add the following environment variables in your CircleCI project settings:
   - `AWS_ACCESS_KEY_ID`
   - `AWS_SECRET_ACCESS_KEY`
   - `AWS_REGION`
   - `DOCKER_IMAGE_NAME`

4. **Trigger the pipeline** — push any commit to `main` to kick off the full pipeline.

---

## Pipeline Stages

```
Lint → Security Scan → Docker Build → Push to ECR → Deploy to EKS
```

| Stage               | Description                                          |
|---------------------|------------------------------------------------------|
| Linting             | Enforces code style and catches syntax errors        |
| Security Scanning   | Identifies vulnerabilities in dependencies \u0026 images  |
| Docker Build        | Builds optimized container images                    |
| Push to ECR         | Publishes images to AWS Elastic Container Registry   |
| Kubernetes Deploy   | Rolls out updates via blue/green or rolling strategy |

---

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feat/your-feature`)
3. Commit your changes (`git commit -m 'feat: add your feature'`)
4. Push to your branch (`git push origin feat/your-feature`)
5. Open a pull request

---

## License

MIT License — see [LICENSE](./LICENSE) for details.
```
