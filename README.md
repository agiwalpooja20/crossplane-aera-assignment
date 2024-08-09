# crossplane-aera-assignment

This repository contains a Crossplane configuration, which deploys fully managed Azure AKS cluster along with Virtual Network and Subnets.
It also sets up Helm to deploy nginx using helm charts through crossplane

## Overview
It contains 3 files
1. Claim.yaml
2. Composition.yaml
3. Definition.yaml
Apply all these files to create the resources required for fully managed AKS cluster along with required networking resources.

```
kubectl apply -f definition.yaml
kubectl apply -f composition.yaml
kubectl apply -f claim.yaml
```

Verify the resources
```
kubectl get xaks
NAME         SYNCED   READY   COMPOSITION   AGE
aera-<>      True     True    composition   48m
```
