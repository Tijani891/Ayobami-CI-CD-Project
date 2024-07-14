# Ayobami CI/CD Project

This project demonstrates a CI/CD pipeline for a microservices application using CircleCI, Docker, Kubernetes, and AWS. It includes automated linting, security scans, and deployment strategies like blue/green and rolling updates.

## Project Structure

- **CircleCI Config**: Configuration files for CircleCI to automate CI/CD.
- **Terraform Files**: Infrastructure as Code for setting up AWS resources.
- **Kubernetes Manifests**: Deployment and service files for Kubernetes.
- **Dockerfile**: Instructions to build Docker images for the microservices.

## Getting Started

### Prerequisites

- Docker
- Kubernetes
- AWS Account
- CircleCI Account

### Setup

1. Clone the repository:
   ```sh
   git clone https://github.com/Tijani891/Ayobami-CI-CD-Project.git
   cd Ayobami-CI-CD-Project
   ```

2. Set up AWS credentials for Terraform.

3. Initialize and apply Terraform configuration:
   ```sh
   terraform init
   terraform apply
   ```

4. Configure CircleCI with your repository and set environment variables for Docker and AWS.

5. Push code to trigger the pipeline.

### CI/CD Pipeline

1. **Linting**: Ensures code quality.
2. **Security Scanning**: Checks for vulnerabilities.
3. **Docker Build**: Builds Docker images for microservices.
4. **Push to Repository**: Pushes Docker images to AWS ECR.
5. **Kubernetes Deployment**: Deploys Docker images to the Kubernetes cluster using blue/green or rolling updates

## Contributing

1. Fork the repository.
2. Create a feature branch.
3. Commit your changes.
4. Push to the branch.
5. Create a pull request.

## License

This project is licensed under the MIT License.

---
