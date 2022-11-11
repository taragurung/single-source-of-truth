# Single-Source-of-Truth
Everything has to go and managed from single source

## About the project:
As we work in a learge or even small team. When application start to scale and the architecture start to become complex managing the application and the underlying system becomes unmanageable and untrackable. 

To eliminate these problem, A single source of Truth can be one solution where all the changes on the application and the infrastructure will be done via single source or from the CICD Pipeline that runs once changes are pushed. 

### Primary Rule:
1. All the changes be it on Application part or System part are pushed to Github or any other respository of the choice.
2. No human intervention is allowed for the build and deployment process.
3. Automate the process.


## How to achieve it with simple example:
The application will be simple nodejs api hosted on AWS EKS with AWS RDS as a database

1. We will make use of AWS services as much as possible. more details on resources later
2. We provision every AWS resources using the Terraform script on AWS. 
3. We will use Github Action for the CICD 

#### Future Goals:
Initially we will write script can be in Makefile or bashscript for managing the CICD but for the deployment part ultimately we will be using the ***ARGOCD*** for application management on the kubernetes cluster, so we don't have to depend on writing commands on scripts.

## Benefits of this approach:
1. When no one is allowed to manually intervene means less chances of unknown changes among team.
2. When someone makes changes on system manaully by logging into AWS and making changes, thats really hard to track. No such problem to occur and have clear understanding of what resources are in the place and at what stage. This we achieve with aws. 
3. Easy to re-create new environment. 

## Tools To Be Used:
1. AWS as Cloud Provider
2. Terraform for resource provisioning
3. Kubernetes for containerization and orchestration
4. Helm for package management
5. ArgoCD

## Folder structure
These will be added later as we make a problem standard for it

## High Level Single Source of Truth WorkFlow
![alt text](https://github.com/taragurung/single-source-of-truth/blob/main/ssot.png)
