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

