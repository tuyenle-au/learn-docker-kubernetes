# learn-docker-kubernetes

Week 1-2: Learn Docker Basics

Mini Project 1: Containerize a Basic Web Application

Choose a simple web application (e.g., a static HTML website, a Node.js or Python Flask application)
Create a Dockerfile with the following steps:
a. Use a base image (e.g., node, python)
b. Set the working directory
c. Copy the application files into the container
d. Install dependencies (if required)
e. Expose the application port
f. Define the command to start the application
Build the Docker image using docker build
Run a container from the image using docker run
Test the web application by accessing it in your browser

Week 3-4: Deep Dive into Docker

Mini Project 2: Multi-Container Web Application with Docker Compose

Choose or create a web application with a frontend, backend, and database (e.g., a simple Todo app)
Containerize the frontend and backend using Dockerfiles (if not done in Mini Project 1)
Create a docker-compose.yml file with the following services:
a. Frontend service with build context, ports, and environment variables (if needed)
b. Backend service with build context, ports, environment variables, and links to the database
c. Database service using an official image (e.g., MySQL, PostgreSQL, MongoDB) with environment variables for configuration
Run the multi-container application using docker-compose up
Test the web application by accessing it in your browser

Week 5-6: Learn Kubernetes Basics

Mini Project 3: Deploy a Web Application on a Local Kubernetes Cluster

Use the web application from Mini Project 1 or choose another simple web application
Create Kubernetes YAML manifests for the following objects:
a. Deployment for the web application (including container image, replicas, and resource requests/limits)
b. Service for the web application (to expose the application to the network)
Apply the manifests to your local Kubernetes cluster using kubectl apply
Test the web application by accessing it through the service (e.g., NodePort or LoadBalancer)

Week 7-8: Advanced Kubernetes Concepts

Mini Project 4: Stateful Application with Autoscaling

Choose or create a stateful application (e.g., a web application with a database or a message broker like RabbitMQ)
Create Kubernetes YAML manifests for the following objects:
a. StatefulSet for the stateful application (including container image, replicas, and resource requests/limits)
b. Persistent Volume and Persistent Volume Claim for each replica
c. Service for the stateful application (to expose the application to the network)
d. Horizontal Pod Autoscaler (HPA) to automatically scale the application based on CPU or memory usage
Apply the manifests to your local Kubernetes cluster using kubectl apply
Test the stateful application by accessing it through the service
Monitor the HPA using kubectl get hpa and test the autoscaling by generating load on the application

Week 9-10: Kubernetes Best Practices and CI/CD

Mini Project 5: CI/CD Pipeline for Docker and Kubernetes

Choose a CI/CD platform (e.g., Jenkins, GitLab CI, GitHub Actions)
Set up the CI/CD platform and integrate it with your version control system (e.g., Git)
Create a CI/CD pipeline with the following stages:
a. Build the Docker image for your web application
b. Push the Docker image to a container registry (e.g., Docker Hub, Google Container Registry)
c. Deploy the Docker image to your Kubernetes cluster
Configure the pipeline to trigger automatically on code changes (e.g., using webhooks or polling)
Create the necessary configuration files for the CI/CD platform (e.g., Jenkinsfile, .gitlab-ci.yml, or github/workflows/*.yml)
a. Define the build stage with steps to build and push the Docker image
b. Define the deployment stage with steps to apply the Kubernetes manifests
c. Add any required secrets or environment variables to the pipeline configuration (e.g., container registry credentials, Kubernetes cluster access)
Test the pipeline by making a code change and verifying that the new version of the application is successfully deployed to the Kubernetes cluster
