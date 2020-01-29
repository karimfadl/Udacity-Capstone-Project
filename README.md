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

You can see this  pipeline in the PDF Graph called **Pipelines.png** in "Screenshots" Directory.
