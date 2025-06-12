# Kubernetes Technical Challenge

## Overview

This challenge evaluates your understanding of Kubernetes concepts and configuration management. You will be presented with a set of Kubernetes manifests that need to be deployed in a specific namespace.

## Your Task

1. Review the provided Kubernetes manifests:
   - `namespace.yaml`
   - `deployment.yaml`
   - `service.yaml`

2. Identify and fix any configuration issues that prevent the application from running correctly.

3. Document your findings and solutions.

## Requirements

- The application must be accessible through the service
- All resources must be properly isolated in the specified namespace
- The application must be able to handle the expected load
- All configurations must follow Kubernetes best practices

## Getting Started

1. Apply the namespace:
```bash
kubectl apply -f namespace.yaml
```

2. Deploy the application:
```bash
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
```

## Evaluation Criteria

Your solution will be evaluated based on:
- Correct identification of configuration issues
- Quality of implemented fixes
- Understanding of Kubernetes concepts
- Documentation of your approach

## Time Limit

You have 45 minutes to complete this challenge.

Good luck! 