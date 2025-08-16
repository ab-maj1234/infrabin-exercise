# Infrabin K8s Exercise — Starter Repo

This repository is the **starting point** for the DevOps exercise. We'll proceed step-by-step with clean, reproducible changes and clear commit history. No trial-and-error: each step will be deliberate and explained.

> Date scaffolded: 2025-08-16

## Objectives (from the brief)

1. Make a public repo to keep all your work in  
2. Install and configure a local Kubernetes environment (Rancher Desktop, Minikube, k3d/k3s, etc.)  
3. Deploy a **service mesh** via Helm (e.g. Istio) to the local cluster  
4. Deploy the **kube-prometheus-stack** Helm chart to the local cluster  
5. Create and install a **Helm chart** to deploy **infrabin** to namespace `infrabin`  
   5.1 Create a Deployment for infrabin  
   5.2 Add an HPA (CPU & Memory), min=1 max=3 replicas  
   5.3 Add a Service and Ingress to reach infrabin through `localhost`  
   5.4 Add a NetworkPolicy to only allow traffic from the ingress controller and Prometheus  
   5.5 Add liveness/readiness health checks  
   5.6 Create a ServiceMonitor so Prometheus scrapes infrabin metrics  
   5.7 Add the application to the service mesh
   
We'll implement these in sequence with separate commits and documentation under `docs/`.

## Repo layout

```
.
├── charts/                 # Helm charts (we'll add `infrabin/` later in step 5)
├── docs/                   # Step-by-step notes, commands, design decisions
├── k8s/                    # Plain manifests (e.g., values files or CRs we keep outside Helm)
├── scripts/                # Helper shell scripts (installers, make targets, etc.)
├── .github/workflows/      # (Optional) CI (lint/helm/chart testing) — to be added later
├── .gitignore
├── LICENSE
└── README.md
```

## Conventions

- **Branch:** `main`  
- **Commits:** Conventional commits (`feat:`, `chore:`, `docs:`, `fix:`)  
- **K8s namespace:** `infrabin`  
- **Tooling:** Helm 3, kubectl ≥ 1.27, service mesh (Istio via Helm), kube-prometheus-stack

## Next steps

1. Create a **public GitHub repository** and push this starter content.  
2. We'll then proceed to **Step 2**: install and configure a local Kubernetes environment.

