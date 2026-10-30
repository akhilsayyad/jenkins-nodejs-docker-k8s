# Node.js Application CI/CD Using Jenkins, Docker and Kubernetes

## Project Overview
Built an automated CI/CD pipeline using Jenkins to build and deploy a Node.js application. The application is containerized using Docker and deployed on Kubernetes using YAML manifests.

## Technologies Used
- Node.js
- Jenkins
- Docker
- Kubernetes
- Dockerfile
- Jenkinsfile
- YAML
- Git

## Project Architecture

Developer
   |
 GitHub
   |
 Jenkins Pipeline
   |
 Docker Build
   |
 Docker Image
   |
 Kubernetes Deployment
   |
 Node.js Application
   |
 Kubernetes Service

## Project Structure
jenkins-nodejs-docker-k8s/
├── service.yml
├── server.js
├── package.json
├── nodejs-app-deploy.yml
├── deployment.yml
├── Jenkinsfile
└── Dockerfile

## Key Components

- **Jenkins:** Automates the CI/CD pipeline.
- **Jenkinsfile:** Defines pipeline stages and deployment steps.
- **Dockerfile:** Builds the Node.js application image.
- **Kubernetes Deployment:** Manages application pods and replicas.
- **Kubernetes Service:** Exposes the application.
- **Node.js:** Runs the backend application.

## CI/CD Pipeline

1. Pull source code from GitHub.
2. Jenkins executes the pipeline.
3. Build the Docker image.
4. Deploy the application to Kubernetes.
5. Expose the application using a Kubernetes Service.

## Deployment Commands

kubectl apply -f deployment.yml

kubectl apply -f service.yml


## Verify Deployment

kubectl get pods

kubectl get deployments

kubectl get services

kubectl get nodes

## Access the Application

Get the Service details:

kubectl get svc


If using NodePort, open:

http://<EC2-PUBLIC-IP>:<NODEPORT>


Ensure the EC2 Security Group allows traffic on the configured NodePort.

## Troubleshooting

kubectl describe pod <pod-name>
kubectl logs <pod-name>
kubectl get events
docker images
docker ps


## Key Learning Outcomes

- CI/CD pipeline automation using Jenkins.
- Docker image creation and containerization.
- Kubernetes application deployment.
- Managing Pods, Deployments and Services.
- Automating application delivery.
- Understanding the end-to-end DevOps workflow.

## Author

**Akhil Sayyad**

GitHub: https://github.com/akhilsayyad
