---
# Page settings
layout: default
keywords:
comments: false

# Hero section
title: Project Overview
description: Page description

# Author box
author:
    title: About Author
    title_url: '#'
    external_url: true
    description: Author description

# Micro navigation
micro_nav: true

# Page navigation
page_nav:
    # prev:
    #     content: Previous page
    #     url: '#'
    next:
        content: The Use Case
        url: '/use_case'
---
## The Karaoke Project
Karaoke is a Microservices project running on Kubernetes that I am using as a means to explore various Application Development, DevOps and GitOps techniques:

* **Infrastructure as Code (IaC):** 
Two IaC approaches are explored. In the first example, OpenTofu and Terragrunt are used to deploy cloud Infrastrucuture and a Kubernetes (EKS) cluster on AWS. The second approach uses Pulumi written in Python. 

* **Kubernetes**: 
This project is pretty heavy on Kubernetes usage, as it explores the Kubernetes ecosystem including Ingress and Traffic Management with products like Istio and Linkerd, as well as GitOps products like Flux and ArgoCD. Maintaining microservices as Helm charts as part of the GitOps lifecycle is also covered. 

* **GitOps**:
There are two GitOps experiments in progress, too. One uses [FluxCD](https://fluxcd.io/) to bootstrap the GitOps repositiory to the EKS cluster, while the other will uses [ArgoCD](https://argoproj.github.io/cd/). 

* **Application Development**:
The Microservices are written in Python and use [FastAPI](https://fastapi.tiangolo.com/) for the REST API and are developed using Test-Driven Development (The unit test coverage is fairly robust on these). [Tilt](https://tilt.dev/) is used as a means of running a local development environment and execution of test suites. 


### The Use Case

### Decomposing the Problem with Domain-Driven Design

### The Microoservices - Application Development

### DevOps - Two Approaches to Deployment and Continuous Delivery

|                        | Approach 1            | Approach 2 |
|------------------------|-----------------------|------------|
| Infrastructure as Code | OpenTofu & Terragrunt | Pulumi     |
| GitOps                 | Flux CD               | ArgoCD     |
| K8S Ingress & Traffic  | Istio                 | Linkerd    |
| Continuous Integration | GitHub Actions        | Gitlab CI  |

## Project Repositories - Source Code
* [karaoke-microservices](https://github.com/lukewyman/karaoke-microservices): An application development project that contains the Microservices for this project.
* [karaoke-aws-resources](https://github.com/lukewyman/karaoke-aws-resources): Contains the OpenTofu modules for building Karaoke cloud infrastructure.
* [karaoke-aws-deploy](https://github.com/lukewyman/karaoke-aws-deploy): The Terragrunt project that deploys Karaoke infrastructure and microservices to AWS.
* [karaoke-gitops-flux](https://github.com/lukewyman/karaoke-gitops-flux): A GitOps repository that bootstraps to the Kubernetes cluster with Flux CD. 