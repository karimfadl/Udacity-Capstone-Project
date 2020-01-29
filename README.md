## Intro

This is my Udacity Cloud DevOps Capstone project. In this project I created a CI/CD pipeline for a basic website that deploys to a cluster in AWS Kops

## Install

To be able to use this CI/CD pipeline we will need:
- Jenkins
- kops
- Ansible
- Vagrant

1. To install Jenkins please follow this guide http://jenkins.io/doc/book/installing/
2. To install Vagrant please follow this guide https://www.vagrantup.com/downloads.html


### 1. Create AWS Cops clusters Using Vagrant

You can follow **ReadMe** file in **Vagrant-Kops-Ansible** Directory To Install AWS Kops Cluster Using Vagrant and Ansible.


### 2. Deploy Jenkins EC2 Instace.

You Can Launch EC2 Instance to Install Jenkins, Add **BlueOcean** Plugin and **Kubernetes Continuous Deploy** Plugin and **Your Docker Hub** Credentials and **kubeconfig** Credentials.


### 3. Deploy containers pipeline

**Pipeline**

You can see this  pipeline in the image called **Pipelines plan.png** in the "Pipeline 2". You can see the **Jenkinsfile** in the folder **deploy-containers-pipeline**.

**Result**
Then, in there you use the **tidy** to **lint the HTML**. Please look at the image: lint.png

Then, we use **docker cli** to build the image and push it. Please look at the images: build-image.png push-image.png docker-image-repository.png


In there you use the **kubectl** to deploy the image to the cluster in the blue and green pod and create a **service** that redirects traffic to the blue pod. Please look at the images: deploy-blue-container.png deploy-green-container.png service-redirect-blue.png

Then, the **service** is updated to redirect traffic to the green pod. Please look at the image: service-redirect-green.png

Then, the website can be access using the URL of the service and the port. Please look at the images: website.png service-pods.png

