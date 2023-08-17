# Kubernetes Cluster with MongoDB and Mongo Express using Minikube

This repository contains the necessary configuration files and instructions to set up a simple Kubernetes cluster using Minikube, running MongoDB and Mongo Express. The MongoDB instance is secured with credentials stored in a secret, and the Mongo Express configuration is customized using a ConfigMap.

## Prerequisites

Before you begin, ensure you have the following installed:

1. [Docker](https://docs.docker.com/get-docker/)
2. [Minikube](https://minikube.sigs.k8s.io/docs/start/)

## Getting Started

Follow these steps to set up the Kubernetes cluster with MongoDB and Mongo Express:

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/Mohamedamine991/deploy_mongodb_and_mongo_express_using_minikube.git
   cd deploy_mongodb_and_mongo_express_using_minikube
2. **Start Minikube:**

   Start Minikube with the necessary configuration:

   ```bash
   minikube start --vm-driver=<your-vm-driver>

  Replace <your-vm-driver> with your preferred VM driver (e.g., virtualbox, hyperkit, kvm2, etc.).


3. **Apply Kubernetes Configurations:**

   Apply the MongoDB deployment, Mongo Express deployment, secret, and ConfigMap:

   ```bash
   kubectl apply -f mongodb_depl.yaml
   kubectl apply -f mongo_express_depl.yaml
   kubectl apply -f mongo_secret.yaml
   kubectl apply -f mongo_express_configmap.yaml
4. **Access Mongo Express:**

   Determine the external IP of the Mongo Express service:

   ```bash
   minikube service mongo-express-service 

## Customization

Feel free to modify the YAML files to customize the configurations according to your requirements.
