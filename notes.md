# 1.0 Kubernetes and cloud native ecosystem

# What is Kubernetes?

## The Beginning

Kubernetes was launched as an open-source project in 2015, after being announced by Google in 2014. Its design was inspired by Google's internal cluster management system called Borg.

Instead of keeping the technology private, Google partnered with the Linux Foundation to create the Cloud Native Computing Foundation, and Kubernetes became the first open-source project under CNCF.

---

## What Kubernetes Means

"Kubernetes" is a Greek word meaning pilot or helmsman of a ship.

It is also commonly called "K8s" because there are 8 letters between the "K" and "s".

The name fits because Kubernetes acts like the captain of a ship. It decides:

* Where containers should run
* How many copies of an application should exist
* When to scale up or down
* What to do if a server or application fails

In simple words, Kubernetes is a **container orchestrator**.

---

## What Kubernetes Does

Containers package applications so they can run anywhere consistently.

But when a company has hundreds or thousands of containers, managing them manually becomes impossible.

That is where Kubernetes helps.

It automatically manages:

* Deployment of applications
* Scaling applications up or down
* Recovery from failures
* Load balancing
* Resource usage across servers

Kubernetes is written in the Go programming language and is designed for very large-scale systems.

---

## Why Kubernetes Became So Popular

Kubernetes became popular because it can support both:

* Small companies starting with a few applications
* Huge companies handling millions of users

According to the 2021 CNCF survey:

* 96% of organizations were either using or evaluating Kubernetes
* More than 5.6 million developers were using it

It is considered one of the largest and most important open-source projects in the world, second only to the Linux kernel.

---

## Real-World Example: Spotify

Spotify originally used its own container platform called Helios.

As Spotify grew to over 200 million monthly users, Helios became difficult to maintain.

So in 2018, Spotify migrated to Kubernetes.

This gave them major benefits:

* Services that once took about an hour to deploy could now be launched in seconds or minutes
* Kubernetes automatically scaled systems during high traffic
* One major service was able to handle around 10 million requests per second
* When traffic dropped, Kubernetes scaled resources down to save money

This ability to automatically grow and shrink resources is called **elasticity** or **autoscaling**.

---

## Where Kubernetes Can Run

Kubernetes is flexible and can run almost anywhere:

* On-premises data centers
* Public cloud platforms
* Hybrid environments

Many cloud providers offer managed Kubernetes services, including:

* Google
* Amazon
* Microsoft
* IBM
* Red Hat
* DigitalOcean

These services let companies install and start using Kubernetes quickly.

---

## Why It Matters

Kubernetes became important because modern applications are made of many containers, and managing them manually is too difficult.

Kubernetes acts like an intelligent control system that keeps applications running, scales them when needed, and recovers them if something breaks.

That is why it has become one of the most valuable technologies in modern cloud computing.






# What are Containers?

## The Main Idea

Containers are a way to package an application together with everything it needs to run.

This includes:

* Application code
* Libraries and dependencies
* Configuration files
* Runtime environment

A container makes sure the **application behaves the same way everywhere**.

Docker played the biggest role in making containers popular.

---

## Why Containers Were Needed

Before containers, companies often used separate servers or virtual machines for each application.

This caused problems:

* Applications behaved differently on different machines
* More hardware was needed
* Deployments were slower
* Scaling applications took more time

Containers **solved this by packaging everything into one unit that can move easily between systems.**

You can t**hink of a container like a shipping box.
**
No matter where it goes, everything inside stays together and works the same way.

---

## Key Benefits of Containers

| Benefit        | What It Means                                                               |
| -------------- | --------------------------------------------------------------------------- |
| Portability    | Containers can run on Linux, Windows, or macOS if a container engine exists |
| Lightweight    | Containers use less CPU and memory than virtual machines                    |
| Faster Startup | Containers can start or stop in seconds                                     |
| Scalability    | You can quickly create many copies of a container                           |
| Consistency    | The application runs the same way in every environment                      |

---

## Containers vs Virtual Machines

| Feature           | Containers            | Virtual Machines     |
| ----------------- | --------------------- | -------------------- |
| Size              | Smaller               | Larger               |
| Startup Time      | Seconds               | Minutes              |
| Resource Usage    | Lower                 | Higher               |
| Includes Full OS  | Shares host OS kernel | Has full separate OS |
| Number Per Server | More containers fit   | Fewer VMs fit        |

Containers are lighter because they do not need a full operating system for every instance.

---

## Important Terms

### Container Image

A container image is the blueprint for a container.

It is a file that contains everything needed to run the application.

Once the image is launched, it becomes a running container.

You can think of it like this:

* Image = Recipe
* Container = Finished meal

---

### Container Registry

A container registry is a place where container images are stored.

Images can be:

* Public
* Private
* Restricted to specific users or services

Common registries include:

* Docker Hub
* Quay
* Google Container Registry

---

## How Kubernetes Uses Containers

Kubernetes does not usually build containers itself.

Instead, Kubernetes:

1. Pulls a container image from a registry/repository
2. Creates one or more running containers
3. Keeps the requested number of replicas running
4. Replaces failed containers automatically
5. Scales the number of containers up or down

For example, if you tell Kubernetes to run 5 copies of an application, Kubernetes will keep those 5 copies alive.

If one fails, Kubernetes creates a replacement automatically.

---

## Popular Container Technologies

Although Docker is the most famous, there are other container technologies too:

| Technology | Purpose                         |
| ---------- | ------------------------------- |
| Docker     | Most popular container platform |
| Podman     | Alternative to Docker           |
| containerd | Lightweight container runtime   |
| rkt        | Older container runtime         |
| LXD        | System container platform       |

---

## The Story Connection

Docker uses the idea of shipping containers.

Applications are packed into standardized boxes called containers.

Then **Kubernetes acts like the captain of a ship**, deciding:

* Which containers go where
* How many should run
* When more are needed
* What happens if one breaks

That is why Docker and Kubernetes work so well together.

Docker packages the applications.

Kubernetes manages them.






# 1.3 What is cloud native

## The Basic Idea

Cloud native is a modern way of building and running software.

Instead of manually deploying applications, waiting weeks for releases, and managing servers one by one, cloud native systems are designed to:

* Deploy quickly
* Scale automatically
* Recover from failures
* Work across cloud environments
* Support fast software updates

Cloud native technologies are especially built for:

* Public clouds
* Private clouds
* Hybrid clouds

---

## Official Meaning

According to the Cloud Native Computing Foundation, cloud native technologies help organizations build and run scalable applications in dynamic environments.

Some important cloud native technologies include:

* Containers
* Microservices
* Service meshes
* Immutable infrastructure
* Declarative APIs

These ideas work together to make applications more flexible and easier to manage.

---

## A Simpler Way to Think About It

Cloud native means building software in a way that takes full advantage of the cloud.

Instead of treating the cloud like a normal server room, cloud native systems are designed to use features like:

* Automatic scaling
* Fast deployments
* Self-healing systems
* Continuous updates
* Infrastructure automation

For example, if an application suddenly gets a lot of traffic, cloud native tools can automatically create more copies of the application.

If traffic drops, they can remove extra copies to save money.

---

## How Cloud Native Changed Software Development

In the 1990s and early 2000s, software teams often worked in silos.

| Team                     | Typical Responsibility        |
| ------------------------ | ----------------------------- |
| System Administrators    | Managed servers               |
| Infrastructure Engineers | Managed networks and hardware |
| Software Engineers       | Wrote application code        |

This often caused slow releases because every team worked separately.

Cloud native changed this approach.

The goal became to remove barriers between teams so code could move from development to testing to production much faster.

Instead of waiting until the end of the month or quarter for a release, teams can now release updates many times per day.

This idea is closely connected to DevOps.

---

## Role of the CNCF

The Cloud Native Computing Foundation is part of the Linux Foundation.

Its goal is to make cloud native computing common everywhere.

The CNCF supports cloud native projects by:

* Funding and organizing communities
* Supporting open-source development
* Creating documentation and training
* Running conferences
* Offering certifications
* Promoting successful projects

Some major conferences include:

* KubeCon
* Open Source Summit

---

## CNCF Project Stages

The CNCF classifies projects by maturity.

| Stage      | Meaning                               |
| ---------- | ------------------------------------- |
| Sandbox    | New and experimental                  |
| Incubating | Growing and used by some companies    |
| Graduated  | Mature and trusted for production use |

Kubernetes was the first graduated CNCF project.

That is one reason Kubernetes became so popular.

It had strong support, documentation, training, and a large community behind it.

---

## Important Cloud Native Projects

Kubernetes is not the only cloud native project.

As you continue learning, you may also see:

| Project    | Purpose                                          |
| ---------- | ------------------------------------------------ |
| Kubernetes | Manages containers                               |
| Helm       | Helps install and manage Kubernetes applications |
| Prometheus | Collects monitoring data                         |
| Linkerd    | Manages communication between services           |

---

## The Big Picture

Cloud native is not just one tool.

It is a whole way of thinking about software.

Applications are built to be:

* Fast to deploy
* Easy to scale
* Reliable
* Automated
* Cloud-friendly

Containers package the application.

Kubernetes manages the containers.

Cloud native provides the larger philosophy behind how everything works together.








# Install Minikube on Windows

## What is Minikube?

Minikube lets you run a local Kubernetes cluster directly on your computer.

It is mainly used for:

* Learning Kubernetes
* Practicing commands
* Testing applications locally

Minikube is free because it runs on your own machine instead of using cloud servers.

However, it is not meant for production because it does not provide the same security, networking, and scalability as cloud platforms.

---

## Requirements Before Installing

Before installing Minikube, you need:

| Requirement               | Purpose                                        |
| ------------------------- | ---------------------------------------------- |
| Terminal / Command Prompt | To run Minikube commands                       |
| Container Runtime         | Minikube needs something like Docker or Podman |
| Docker Desktop or Podman  | To run containers locally                      |

Most people use Docker Desktop with Minikube on Windows.

---

## Installation Steps

### 1. Go to the Minikube Website

Open the official Minikube website and go to the “Get Started” section.

Choose:

* Windows
* x86-64 architecture
* Stable release
* Installer / executable file

### 2. Download the Installer

Download the Minikube installer file.

Windows may show security warnings like:

* "This app is not commonly downloaded"
* "Make sure you trust this installer"

If that happens:

* Click "Keep"
* Then choose "Keep anyway"

### 3. Run the Installer

After downloading:

* Open the installer
* Windows may show another warning
* Click "Run anyway"
* Select language
* Accept the agreement
* Click Install
* Finish the installation wizard

---

## Verify the Installation

Open:

* Command Prompt
* PowerShell
* Windows Terminal

Run:

```bash
minikube
```

If the installation worked, Minikube will display a list of available commands.

That confirms Minikube is installed successfully.

---

## Story Version

Think of Minikube as your own small practice Kubernetes environment.

Instead of paying for cloud servers, you create a mini Kubernetes cluster on your laptop.

Docker provides the container engine underneath, and Minikube builds a local Kubernetes cluster on top of it.

So:

* Docker runs the containers
* Minikube runs Kubernetes locally
* Kubernetes manages the containers

That is the foundation for practicing Kubernetes on Windows.







# Install Minikube on Windows

## What is Minikube?

Minikube lets you run a local Kubernetes cluster directly on your computer.

It is mainly used for:

* Learning Kubernetes
* Practicing commands
* Testing applications locally

Minikube is free because it runs on your own machine instead of using cloud servers.

However, it is not meant for production because it does not provide the same security, networking, and scalability as cloud platforms.

---

## Requirements Before Installing

Before installing Minikube, you need:

| Requirement               | Purpose                                        |
| ------------------------- | ---------------------------------------------- |
| Terminal / Command Prompt | To run Minikube commands                       |
| Container Runtime         | Minikube needs something like Docker or Podman |
| Docker Desktop or Podman  | To run containers locally                      |

Most people use Docker Desktop with Minikube on Windows.

---

## Installation Steps

### 1. Go to the Minikube Website

Open the official Minikube website and go to the “Get Started” section.

Choose:

* Windows
* x86-64 architecture
* Stable release
* Installer / executable file

### 2. Download the Installer

Download the Minikube installer file.

Windows may show security warnings like:

* "This app is not commonly downloaded"
* "Make sure you trust this installer"

If that happens:

* Click "Keep"
* Then choose "Keep anyway"

### 3. Run the Installer

After downloading:

* Open the installer
* Windows may show another warning
* Click "Run anyway"
* Select language
* Accept the agreement
* Click Install
* Finish the installation wizard

---

## Verify the Installation

Open:

* Command Prompt
* PowerShell
* Windows Terminal

Run:

```bash
minikube
```

If the installation worked, Minikube will display a list of available commands.

That confirms Minikube is installed successfully.

---

## Story Version

Think of Minikube as your own small practice Kubernetes environment.

Instead of paying for cloud servers, you create a mini Kubernetes cluster on your laptop.

Docker provides the container engine underneath, and Minikube builds a local Kubernetes cluster on top of it.

So:

* Docker runs the containers
* Minikube runs Kubernetes locally
* Kubernetes manages the containers

That is the foundation for practicing Kubernetes on Windows.





# Spin Up and Explore a Minikube Cluster

## Before Starting

Before creating a cluster, make sure your container runtime is running.

Most people use Docker Desktop.

You can check by opening a terminal and running:

```bash id="4crk0u"
docker
```

If Docker is running, you will see a list of Docker commands.

If you get an error, open Docker Desktop first and wait until it fully starts.

---

## Start the Cluster

To create a local Kubernetes cluster using Minikube, run:

```bash id="e5p9jx"
minikube start
```

This command creates a small Kubernetes environment on your own computer.

Minikube will:

* Create a virtual Kubernetes node
* Configure the control plane
* Start important Kubernetes services
* Connect everything together

The process usually takes a few minutes.

Once complete, you will see a success message saying the cluster is ready.

---

## Minikube vs Kubectl

| Tool     | Purpose                                |
| -------- | -------------------------------------- |
| Minikube | Creates and manages the local cluster  |
| kubectl  | Interacts with and manages the cluster |

A simple way to think about it:

* Minikube builds the cluster
* Kubectl talks to the cluster

In cloud platforms like Amazon Web Services, Microsoft Azure, or Google Cloud, you usually create the cluster using their tools, but still manage it with kubectl.

---

## View Cluster Information

Run:

```bash id="f7y2nl"
kubectl cluster-info
```

This command shows important details about your cluster, such as:

* The control plane address
* The local IP and port
* Core Kubernetes services like DNS

Because Minikube runs locally, you will usually see an address like:

```text id="i1v8sq"
https://127.0.0.1:<port>
```

If you see an error saying:

```text id="w6n2bo"
The connection to the server was refused
```

it usually means your Minikube cluster is not running yet.

Start it again with:

```bash id="r9d4qt"
minikube start
```

---

## View Nodes

A node is a machine that runs Kubernetes workloads.

In Minikube, there is usually only one node because everything runs on your laptop.

Run:

```bash id="q2j5mx"
kubectl get nodes
```

You will normally see something like:

| Name     | Role          | Status |
| -------- | ------------- | ------ |
| minikube | control-plane | Ready  |

The node output may also show the Kubernetes version currently running.

---

## View Namespaces

Namespaces are used to organize and separate resources inside Kubernetes.

Run:

```bash id="p4c8zu"
kubectl get namespaces
```

You will usually see these default namespaces:

| Namespace       | Purpose                                |
| --------------- | -------------------------------------- |
| default         | Main place where your applications run |
| kube-system     | Internal Kubernetes components         |
| kube-public     | Public cluster information             |
| kube-node-lease | Tracks node health and heartbeats      |

Namespaces are useful because they help keep different applications, teams, or environments separate from each other.

---

## View Pods

Pods are the smallest deployable unit in Kubernetes.

A pod usually contains one or more containers running together.

Run:

```bash id="m8v3ks"
kubectl get pods -A
```

The `-A` flag means all namespaces.

This command shows every pod running in the cluster, including the system pods Kubernetes needs internally.

Examples include:

* DNS pods
* Networking pods
* Storage pods
* Kubernetes control plane components

---

## View Services

Services help expose pods and send traffic to them.

Run:

```bash id="n7x0fa"
kubectl get services -A
```

A service acts like an internal traffic manager or load balancer.

Instead of connecting directly to a pod, users or applications connect to a service, and the service forwards traffic to the correct pod.

This is useful because pods can stop, restart, or change IP addresses, while the service stays stable.

---

## Story Version

When you run `minikube start`, you create a small Kubernetes world on your laptop.

Inside that world:

* Nodes provide computing resources
* Namespaces organize resources
* Pods run applications
* Services direct traffic
* Kubectl lets you inspect and control everything

Even though it is small, it works the same way as a real Kubernetes cluster in the cloud.





# Reading and Writing YAML

## Why YAML Matters

When working with Kubernetes, you often do not create things manually one command at a time.

Instead, you write down what you want your cluster to look like inside a file.

For example, you may want:

* A namespace called `production`
* An application with 3 replicas
* A service that exposes port 80
* A pod running a specific container image

All of this can be written in a YAML file.

Kubernetes reads the YAML file and creates everything exactly the way you described.

This is why YAML is so important in Kubernetes.

---

## Infrastructure as Code and GitOps

YAML is heavily connected to two important ideas:

| Term                   | Meaning                                                            |
| ---------------------- | ------------------------------------------------------------------ |
| Infrastructure as Code | Managing infrastructure using files instead of manual clicks       |
| GitOps                 | Storing infrastructure files in Git and deploying changes from Git |

With Infrastructure as Code, your servers, applications, namespaces, and networking rules are all stored in code files.

With GitOps, these files are saved in Git repositories so you can:

* Track changes
* Roll back mistakes
* Collaborate with teams
* Keep a history of what changed

That means your Kubernetes cluster can be recreated anytime just by using the YAML files again.

---

## What is YAML?

YAML is a data serialization language.

That sounds complicated, but it simply means YAML is a standard way to organize and store information.

It is mainly used for configuration files.

YAML helps different systems exchange information in a format that is easy for humans to read.

Other common data formats are:

* JSON
* XML

YAML is usually easier to read because it uses spaces and indentation instead of lots of brackets and commas.

The full name is:

**YAML Ain’t Markup Language**

It was designed to be simple and human-friendly.

---

## Basic Structure of YAML

YAML mainly uses:

* Key-value pairs
* Lists
* Nested values
* Comments
* Indentation

These few ideas are enough to understand most Kubernetes YAML files.

---

## Key-Value Pairs

The most basic thing in YAML is a key-value pair.

A key is the name of something.

A value is the information stored under that name.

They are separated by a colon.

Example:

```yaml id="4x7vjl"
name: Ahmed
role: Data Analyst
city: Karachi
```

| Key  | Value        |
| ---- | ------------ |
| name | Ahmed        |
| role | Data Analyst |
| city | Karachi      |

Here:

* `name` is the key
* `Ahmed` is the value

This is very similar to a dictionary in programming.

---

## Lists in YAML

Lists are used when you want multiple values under one key.

In YAML, a list is created using dashes.

Example:

```yaml id="w3g0ne"
courses:
  - Docker Essentials
  - Kubernetes Basics
  - SQL for Data Analysis
```

This means the key `courses` contains three items.

| Key     | Values                                                      |
| ------- | ----------------------------------------------------------- |
| courses | Docker Essentials, Kubernetes Basics, SQL for Data Analysis |

Every item in the list starts with a dash.

---

## Nested Data

Sometimes you want to store information inside other information.

That is where indentation becomes important.

Example:

```yaml id="0k3zup"
person:
  name: Ahmed
  role: Data Analyst
  company:
    name: IRD
    department: Analytics
```

This structure means:

* There is a `person`
* Inside person there is a `name`
* There is also a `company`
* Inside company there is a `name` and `department`

You can think of indentation as showing parent-child relationships.

---

## YAML Symbols You Should Know

| Symbol | Meaning                      |
| ------ | ---------------------------- |
| `---`  | Start of a new YAML document |
| `#`    | Comment                      |
| `:`    | Separates key and value      |
| `-`    | Represents a list item       |

Example:

```yaml id="10s7ji"
---
# Instructor information
name: Kim
courses:
  - Kubernetes
  - Docker
```

Here:

* `---` starts the document
* `# Instructor information` is a comment
* `courses` contains a list

Comments are ignored by the computer and only help humans understand the file.

---

## Multiple YAML Documents in One File

A single YAML file can contain more than one document.

Each document starts with:

```yaml id="go7x9f"
---
```

This is useful in Kubernetes because one file may contain multiple resources.

For example:

* One namespace
* One deployment
* One service

all inside the same file.

---

## File Extensions

YAML files usually end with:

* `.yaml`
* `.yml`

Both are correct.

Many teams prefer `.yaml` because it is easier to read.

---

## The Most Common YAML Problem: Indentation

Indentation is one of the hardest parts of YAML for beginners.

YAML depends on spaces to understand structure.

Even one missing space can create an error.

Wrong example:

```yaml id="z9w2cr"
person:
name: Ahmed
role: Analyst
```

This is wrong because `name` and `role` should be indented.

Correct example:

```yaml id="m4y8ka"
person:
  name: Ahmed
  role: Analyst
```

The spaces tell YAML that `name` and `role` belong inside `person`.

Usually, people use 2 spaces for indentation.

Do not use tabs because YAML may break.

---

## YAML Validation

Because indentation mistakes are common, many people use YAML validators.

A YAML validator checks whether the file structure is correct.

One example is:

YAML Checker

You can paste your YAML into a validator and it will point to the exact line causing the problem.

---

## Why YAML is Important in Kubernetes

Almost every Kubernetes object is created using YAML.

For example, you can create:

* Pods
* Deployments
* Services
* Namespaces
* ConfigMaps
* Secrets

Instead of running many commands every time, you write the configuration once in YAML and reuse it whenever needed.

This makes Kubernetes easier to manage, especially for large projects.

---

## Story Version

Think of YAML like a blueprint or instruction sheet for Kubernetes.

Instead of telling Kubernetes step by step:

* Create this pod
* Open this port
* Run 3 copies
* Put it in this namespace

you write all the instructions in one YAML file.

Then Kubernetes reads the file and builds everything exactly the way you described.






# Create a Namespace

## What is a Namespace?

In Kubernetes, namespaces are used to organize and isolate resources inside a cluster.

They help keep applications separated from each other.

For example, you may have:

* A development environment
* A production environment
* Different teams
* Different microservices

all running inside the same cluster.

Instead of mixing everything together, Kubernetes lets you place resources into different namespaces.

---

## Why Namespaces are Useful

Suppose you have the same application in two versions:

| Environment | Purpose                       |
| ----------- | ----------------------------- |
| Development | Used for testing and building |
| Production  | Used by real users            |

If both run in the same cluster, namespaces help separate them.

For example:

* Development resources go into a `development` namespace
* Production resources go into a `production` namespace

This makes the cluster cleaner and easier to manage.

---

## Default Namespaces in Kubernetes

Before creating your own namespaces, you can see the ones Kubernetes already creates by default.

Run:

```bash id="b8m2xq"
kubectl get namespaces
```

You will usually see something like:

| Namespace       | Purpose                                                                 |
| --------------- | ----------------------------------------------------------------------- |
| default         | Main namespace where resources are created if no namespace is specified |
| kube-system     | Contains internal Kubernetes system components                          |
| kube-public     | Stores publicly accessible cluster information                          |
| kube-node-lease | Stores node heartbeat and lease information                             |

These namespaces are created automatically when the cluster starts.

---

## Namespace YAML Manifest

Namespaces are usually created using YAML manifests.

A simple namespace YAML file looks like this:

```yaml id="7p3kws"
apiVersion: v1
kind: Namespace
metadata:
  name: development
```

### Understanding Each Line

| Field               | Meaning                                       |
| ------------------- | --------------------------------------------- |
| `apiVersion: v1`    | Uses version 1 of the Kubernetes API          |
| `kind: Namespace`   | Tells Kubernetes you are creating a namespace |
| `metadata`          | Contains information about the object         |
| `name: development` | The actual name of the namespace              |

The most important field here is the namespace name.

In this example, the namespace will be called `development`.

---

## Create the Namespace

Save the file as something like:

```text id="p0d8yu"
namespace.yaml
```

Then run:

```bash id="h4w7ln"
kubectl apply -f namespace.yaml
```

### What This Command Means

| Part             | Meaning                      |
| ---------------- | ---------------------------- |
| `kubectl`        | Kubernetes command line tool |
| `apply`          | Create or update a resource  |
| `-f`             | Means "from file"            |
| `namespace.yaml` | Name of the YAML file        |

After running the command, Kubernetes reads the YAML file and creates the namespace.

---

## Verify the Namespace

Run:

```bash id="m6n2ta"
kubectl get namespaces
```

Now you should see `development` in the list.

---

## Multiple Resources in One YAML File

YAML allows you to place multiple resources in one file.

To separate resources, use:

```yaml id="g7y1sb"
---
```

The three dashes mean “start a new YAML document”.

This is useful because one file can contain multiple Kubernetes objects.

For example, you can create both `development` and `production` namespaces in the same file.

Example:

```yaml id="z4t9cv"
apiVersion: v1
kind: Namespace
metadata:
  name: development
---
apiVersion: v1
kind: Namespace
metadata:
  name: production
```

Now the same file creates two namespaces instead of one.

---

## Apply the Updated File

Run the same command again:

```bash id="s1k4mr"
kubectl apply -f namespace.yaml
```

Kubernetes will:

* Keep the existing `development` namespace
* Create the new `production` namespace

Then verify again:

```bash id="d2u8fq"
kubectl get namespaces
```

You should now see both:

* `development`
* `production`

---

## Delete the Namespaces

If you want to remove the namespaces, run:

```bash id="n9v3ha"
kubectl delete -f namespace.yaml
```

Kubernetes will read the same file and delete the resources defined inside it.

This is one of the benefits of Infrastructure as Code.

The same file used to create resources can also be used to delete them.

---

## Important YAML Concepts Used Here

| YAML Feature       | Example                 | Purpose                           |
| ------------------ | ----------------------- | --------------------------------- |
| Key-value pair     | `kind: Namespace`       | Defines information               |
| Indentation        | `name` under `metadata` | Shows hierarchy                   |
| Multiple documents | `---`                   | Separates resources               |
| File extension     | `.yaml`                 | Standard Kubernetes manifest file |

---

## Story Version

Think of a Kubernetes cluster like a large office building.

Namespaces are like different departments inside that building.

For example:

* One department for development
* One for production
* One for testing

Even though everyone is in the same building, each department stays organized and separate.

That is exactly what namespaces do inside Kubernetes.






# Deploy an Application

## Why Deployments Matter

In Kubernetes, applications usually run inside pods.

However, if you create only one pod and it crashes, your application becomes unavailable.

To avoid this, Kubernetes uses a resource called a Deployment.

A deployment helps ensure:

* Multiple copies of the application are running
* Failed pods are recreated automatically
* Updates can be managed more easily
* Applications remain highly available

High availability means there is always more than one copy of the application available to handle traffic.

For example, if you run 3 replicas and one pod fails, the other 2 continue serving users while Kubernetes creates a replacement.

---

## Deployment YAML Manifest

A deployment is usually created using a YAML file.

Example:

```yaml id="k8u1de"
apiVersion: apps/v1
kind: Deployment
metadata:
  name: pod-info-deployment
  namespace: development
spec:
  replicas: 3
  selector:
    matchLabels:
      app: pod-info
  template:
    metadata:
      labels:
        app: pod-info
    spec:
      containers:
        - name: pod-info-container
          image: schlesinger/pod-info:latest
          ports:
            - containerPort: 3000
          env:
            - name: POD_NAME
              valueFrom:
                fieldRef:
                  fieldPath: metadata.name
            - name: POD_NAMESPACE
              valueFrom:
                fieldRef:
                  fieldPath: metadata.namespace
            - name: POD_IP
              valueFrom:
                fieldRef:
                  fieldPath: status.podIP
```

---

## Understanding the Deployment YAML

### Top-Level Fields

| Field                 | Meaning                                        |
| --------------------- | ---------------------------------------------- |
| `apiVersion: apps/v1` | Uses the apps API group version 1              |
| `kind: Deployment`    | Tells Kubernetes to create a deployment        |
| `metadata`            | Contains identifying information               |
| `name`                | Name of the deployment                         |
| `namespace`           | Namespace where the deployment will be created |

In this example:

* Deployment name = `pod-info-deployment`
* Namespace = `development`

---

### Replicas

```yaml id="z0p2te"
replicas: 3
```

This tells Kubernetes to always keep 3 copies of the application running.

If one pod fails or is deleted, Kubernetes automatically creates another one.

---

### Labels and Selectors

```yaml id="m4j8vn"
selector:
  matchLabels:
    app: pod-info
```

```yaml id="t9q3lc"
labels:
  app: pod-info
```

Labels are small tags attached to Kubernetes resources.

The deployment uses selectors to find and manage pods with the matching label.

In this case:

* Label = `app: pod-info`
* The deployment controls all pods with that label

---

### Container Section

```yaml id="d2r7kp"
containers:
  - name: pod-info-container
    image: schlesinger/pod-info:latest
```

This defines the actual container to run.

| Field    | Meaning                              |
| -------- | ------------------------------------ |
| `name`   | Name of the container                |
| `image`  | Container image to use               |
| `latest` | Pull the latest version of the image |

The image comes from Docker Hub.

---

### Container Port

```yaml id="n5f0sm"
ports:
  - containerPort: 3000
```

This tells Kubernetes that the application inside the container listens on port 3000.

---

### Environment Variables

The deployment also creates environment variables inside each pod:

```yaml id="g8u2xa"
env:
  - name: POD_NAME
  - name: POD_NAMESPACE
  - name: POD_IP
```

These variables store useful information about the pod itself.

| Variable        | Meaning                            |
| --------------- | ---------------------------------- |
| `POD_NAME`      | Name of the pod                    |
| `POD_NAMESPACE` | Namespace where the pod is running |
| `POD_IP`        | IP address of the pod              |

These values are automatically filled using `fieldRef`.

---

## Make Sure the Namespace Exists

Before creating the deployment, verify the namespace exists:

```bash id="w6j4zt"
kubectl get ns
```

If `development` is missing, create it using:

```bash id="p9x3rn"
kubectl apply -f namespace.yaml
```

---

## Create the Deployment

Save the YAML into a file such as:

```text id="f3n1qd"
deployment.yaml
```

Then run:

```bash id="c8k7lp"
kubectl apply -f deployment.yaml
```

Kubernetes will read the file and create the deployment.

---

## View the Deployment

To see deployments inside the `development` namespace, run:

```bash id="h2m8vc"
kubectl get deployments -n development
```

Example output:

| Name                | Ready | Up-to-date | Available |
| ------------------- | ----- | ---------- | --------- |
| pod-info-deployment | 3/3   | 3          | 3         |

This means:

* 3 pods are expected
* 3 pods are running
* 3 pods are available

---

## View the Pods

To see the pods created by the deployment:

```bash id="r5v9ua"
kubectl get pods -n development
```

You should see 3 pods.

Each pod name will be slightly different because Kubernetes generates unique names automatically.

Example:

```text id="b7t1ew"
pod-info-deployment-abc12
pod-info-deployment-def34
pod-info-deployment-ghi56
```

---

## Test Self-Healing

One of the biggest benefits of deployments is self-healing.

Delete one pod:

```bash id="x4k2po"
kubectl delete pod <pod-name> -n development
```

Example:

```bash id="y1m7nr"
kubectl delete pod pod-info-deployment-abc12 -n development
```

Now run:

```bash id="q6u0fd"
kubectl get pods -n development
```

You will notice:

* One pod is terminating
* A new pod is being created automatically

This happens because the deployment is trying to maintain exactly 3 replicas.

If one disappears, Kubernetes replaces it.

---

## Important Commands Used

| Command                                        | Purpose                                   |
| ---------------------------------------------- | ----------------------------------------- |
| `kubectl get ns`                               | List namespaces                           |
| `kubectl apply -f namespace.yaml`              | Create namespace from YAML                |
| `kubectl apply -f deployment.yaml`             | Create deployment from YAML               |
| `kubectl get deployments -n development`       | View deployments in development namespace |
| `kubectl get pods -n development`              | View pods in development namespace        |
| `kubectl delete pod <pod-name> -n development` | Delete a pod                              |

---

## Story Version

Think of a deployment like a manager supervising workers.

You tell the manager:

> I always want 3 workers doing this job.

If one worker leaves, the manager immediately hires another one.

In Kubernetes:

* Pods are the workers
* The deployment is the manager
* Replicas define how many workers should always exist

That is why deployments are one of the most important resources in Kubernetes.
