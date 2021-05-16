# devops-challenge-entry-solution
Particle 41 Code Solution - Entry


Challenge :
# Particle41 DevOps Challenge - Entry level


This is an entry-level challenge for candidates who want to join the Particle41 DevOps team.

It is designed to test your level of familiarity with development and operations tools and concepts.

You will have **4 hours** to complete the challenge.


## The challenge


Create a simple microservice in any programming language of your choice, as follows:

- The application should be a web server that returns a JSON response with the following structure, when its `/` URL path is accessed:

```json
{
  "timestamp": "<current date and time>",
  "ip": "<the IP address of the visitor>"
}
```

- Create a Dockerfile for this microservice and publish the image to Docker Hub. Your application must be configured to run as a non-root user in the container.

- Create a Kubernetes manifest in YAML format, containing a Deployment and a Service, to deploy your microservice on Kubernetes. Your Deployment must use your public Docker image.

- Publish your code, Dockerfile, and Kubernetes manifests to a public Git repository in a platform of your choice (e.g. GitHub, GitLab, Bitbucket, etc.), so that it can be cloned by the team.


## Criteria


Your task will be considered successful if a colleague is able to deploy your manifests to a running Kubernetes cluster and use your microservice.

Assuming that your manifest file is named `microservice.yml` (but you can name it whatever you want), the command:

```sh
kubectl apply -f microservice.yml # i.e. your manifest file
```

must be the only command needed to deploy your microservice to Kubernetes.

Other criteria for evaluation will be:

- Code quality and style: your code must be easy for others to read, and properly documented when relevant

- Container best practices: your container image should be as small as possible, without unnecessary bloat



## SOLUTION

---
title: Toolchain Setup for macOS
weight: 20
---

## Operating System Version

This documentation is written for macOS High Sierra. If you are running
an older version, it is recommended to upgrade before proceeding. Use
this [Apple Support KB](https://support.apple.com/en-us/HT201260) to
identify and verify the macOS version you are using.

### Homebrew

We will use [Homebrew](https://brew.sh/) for managing installation of
other tools.

``` shell
# Run the official Homebrew installer
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

# Get Homebrew-Cask
brew tap caskroom/cask

# Update Homebrew
brew update
```

## Install Tools

``` shell
# Docker
# https://www.docker.com/community-edition
brew cask install docker

# Configure and Start Docker
open /Applications/Docker.app

# Kubernetes
# https://kubernetes.io/docs/tasks/tools/install-kubectl-macos/
brew install kubectl

# Test to ensure latest version of Kubernetes
kubectl version --client
```
