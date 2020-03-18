# Kubernetes Custom Build Pipeline

A re-usable build pipeline that can be used to deploy applications to k8s clusters. Ideally should be platform independent but one cloud provider is sufficent. e.g. GKE, AKE or EKS.

This is based on this tutorial from Brendan Burns https://www.youtube.com/watch?v=5irsAdKoEBU&list=PLLasX02E8BPCrIhFrc_ZiINhbRkYMKdPT&index=6

## Components
- Source code
- Container image
- Container Registry
- K9s cluster

## Pipeline
- Source
- Build
- Deploy

# Notes
- Set up cluster so it only pulls securely from the registry. Use the admiissions controller to validate that the image is from the specified registry.
Can also use the policy controller to specify policies such as this.
- Only your build pipeline should have permissions to push into the container registry.
- Also only the build pipeline should be able to create pods in the cluster.
- In the pipeline, it's best practice to have:
    - Vulnerability Scanning
    - Credential Scanning
    - Integration Testing