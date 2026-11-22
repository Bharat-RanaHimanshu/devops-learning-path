# DevOps Learning Path

A hands-on guide that goes from DevOps fundamentals through Linux, networking, Git, CI/CD, Docker, AWS, Terraform and Kubernetes to MLOps and AI infrastructure. It's built one lesson at a time, and the next lesson starts only after the current one is understood.

Each lesson folder contains:

| File | What it is |
|---|---|
| `index.html` | The interactive lesson: simulators, clickable diagrams and a self-check quiz. Open it in a browser. |
| `notes.md` | A cheat sheet for quick reference later. Its diagrams render directly on GitHub. |
| `my-notes.md` | **Your** notes, in your own words. Write them before you read `notes.md`. |
| `lab/` | Hands-on exercises and your solutions (from Lesson 02 on). |

## How to study a lesson

1. **Study** the lesson's `index.html` and work through every interactive figure.
2. **Do the lab** (from Lesson 02 on).
3. **Write `my-notes.md`** without looking at `notes.md`. Explaining it in your own words is where the learning happens.
4. **Ask your doubts.** They're logged with their answers in [DOUBTS.md](DOUBTS.md).
5. **Confirm you're ready.** Only then does the next lesson get built. Status lives in [PROGRESS.md](PROGRESS.md).

## Viewing the interactive lessons

The `index.html` pages don't render on github.com, which shows their source. To view one:

- clone the repo and open the file in a browser:
  ```bash
  git clone https://github.com/Bharat-RanaHimanshu/devops-learning-path.git
  ```
- or, once GitHub Pages is set up (a Lesson 05 exercise), open the published site.

## Roadmap

| # | Lesson | Covers |
|---|---|---|
| | **Phase 0: Foundations** | |
| 01 | [The DevOps Big Picture](lessons/01-devops-big-picture/) | Delivery loop, CI vs CD, config drift, tool map, DORA metrics, MLOps preview |
| 02 | Linux & the Shell | Filesystem, processes, permissions, systemd, package managers, shell scripting |
| 03 | Networking for DevOps | IP & CIDR, ports, DNS, HTTP & TLS, proxies, load balancers, debugging with curl and dig |
| 04 | Git & Collaboration | Commits, branches, merge vs rebase, pull requests, trunk-based development |
| | **Phase 1: Build & Ship** | |
| 05 | CI/CD Pipelines | GitHub Actions, pipeline stages, artifacts, caching, secrets, environments |
| 06 | How Containers Work | Namespaces, cgroups, images and layers, containers vs VMs |
| 07 | Docker in Practice | Dockerfiles, multi-stage builds, Compose, registries, image security |
| | **Phase 2: Cloud with AWS** | |
| 08 | Cloud & AWS Foundations | Regions & AZs, shared responsibility, IAM, account security, billing guardrails |
| 09 | AWS Networking | VPC, subnets, route tables, security groups, NAT, load balancers, Route 53 |
| 10 | AWS Compute & Storage | EC2, Auto Scaling, S3, EBS, RDS, Lambda |
| 11 | Containers on AWS | ECR, ECS, Fargate, task definitions, service autoscaling |
| 12 | Infrastructure as Code | Terraform providers, state, plan/apply, modules; where Ansible fits |
| | **Phase 3: Kubernetes** | |
| 13 | Kubernetes Architecture | Control plane, nodes, desired state and reconciliation, kubectl |
| 14 | Core Kubernetes Objects | Pods, Deployments, Services, Ingress, ConfigMaps, Secrets, volumes |
| 15 | Operating Kubernetes | Helm, probes, resource limits, autoscaling, rolling updates |
| 16 | GitOps & EKS | Argo CD, EKS clusters, IAM integration, node management |
| | **Phase 4: Run It Well** | |
| 17 | Observability | Metrics, logs, traces; Prometheus, Grafana, CloudWatch, OpenTelemetry; alerting |
| 18 | DevSecOps | Secrets management, image and dependency scanning, least privilege, supply chain |
| 19 | Reliability & Release Strategy | SLOs and error budgets, blue/green and canary, incidents, cost control |
| | **Phase 5: MLOps & AI Infrastructure** | |
| 20 | The ML Lifecycle | Why ML systems differ, MLOps maturity, training vs serving |
| 21 | Data, Experiments & Models | DVC, MLflow tracking, model registry, reproducibility |
| 22 | Serving Models & GPUs | Model APIs, batching, KServe and vLLM, GPUs on Kubernetes, SageMaker endpoints |
| 23 | ML Pipelines & Monitoring | Kubeflow and SageMaker pipelines, drift detection, retraining, LLMOps |
| | **Capstone** | |
| 24 | Capstone Project | Ship an ML-backed service end to end on AWS with CI/CD, IaC, Kubernetes and monitoring |

## Resuming after a break

[PROGRESS.md](PROGRESS.md) is the single place that records where things stand: lesson status, the current lesson, the next step and the study rules. Start any new study session by reading it.

## Safety rule for this public repo

Never commit secrets: AWS access keys, tokens, passwords, `.env` files, Terraform state. Bots scan public repositories for leaked keys and can abuse them within minutes. The `.gitignore` blocks the common cases, but it is a backstop, not a guarantee.
