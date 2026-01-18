✨ Software Architecture & Deployment Models

🏛️ Monolithic Architecture

Monolithic architecture is a single-tier, tightly coupled software design paradigm in which an 
application is developed, compiled, packaged, deployed, and executed as one cohesive and indivisible
executable unit.

🔬 Technical Characteristics

Single deployment artifact (JAR/WAR/EXE)

In-process method invocation

Centralized configuration and logging

Shared database schema

⚠️ Architectural Impact

Any modification necessitates full system redeployment

Limited horizontal scalability

Low fault tolerance due to tight coupling

🧩 Microservices Architecture

Microservices architecture is a distributed, service-oriented architectural style in which an application is decomposed into fine-grained, autonomous, and independently deployable services, each representing a specific business capability.

🔹 Technical Definition

A microservices-based system consists of loosely coupled services communicating over lightweight network protocols (REST, gRPC, AMQP), with decentralized data management and independent lifecycle control.

🔬 Technical Characteristics

Independent deployment pipelines

Service-level data ownership

Polyglot programming and persistence

Resilience through isolation

⚠️ Architectural Impact

Increased operational complexity

Network latency and observability challenges

Requires mature DevOps practices

⚖️ Monolithic vs Microservices (Conceptual View)
Dimension	Monolithic	Microservices
Coupling	Tight	Loose
Deployment	Atomic	Independent
Scalability	Coarse-grained	Fine-grained
Fault Isolation	Minimal	High
System Evolution	Rigid	Agile
🌐 Traditional vs Virtualization vs Containerization
🧱 Traditional Deployment (Bare-Metal Architecture)

Traditional deployment refers to executing applications directly on physical hardware without any abstraction layer between the application and the operating system.

🔹 Technical Definition

Each application is bound to a dedicated physical server with a single operating system, leading to static resource allocation and hardware dependency.

Drawbacks: Resource underutilization, poor scalability, inflexible infrastructure.

🖥️ Virtualization

Virtualization is a hardware abstraction technique that enables multiple virtual machines (VMs) to run concurrently on a single physical host using a hypervisor.

🔹 Technical Definition

A hypervisor emulates hardware resources, allowing each VM to operate with its own guest operating system, kernel, and binaries, providing strong isolation at the cost of overhead.

Trade-off: Enhanced isolation vs increased resource consumption.

📦 Containerization

Containerization is an operating system–level virtualization mechanism that encapsulates applications into isolated user-space instances called containers, sharing the host OS kernel.

🔹 Technical Definition

Containers utilize Linux kernel primitives such as namespaces for isolation, cgroups for resource governance, and union file systems for layered images, enabling lightweight and portable execution.

Advantage: High density, rapid startup, cloud-native scalability.

📊 Comparative Summary
Attribute	Traditional	Virtualization	Containerization
Abstraction Level	None	Hardware	OS Kernel
OS Overhead	High	Very High	Minimal
Startup Time	Minutes	Minutes	Seconds
Portability	Poor	Moderate	Excellent
Resource Efficiency	Low	Medium	High
🐳 What is Docker?

Docker is an open-source containerization and application delivery platform that standardizes software execution by packaging applications and their dependencies into immutable, portable container images.

🔹 Technical Definition

Docker provides a client–server architecture that leverages OS-level virtualization, enabling consistent application behavior across heterogeneous environments by isolating processes and controlling resource utilization.

🔧 Core Components

Docker Engine – Container runtime daemon

Docker Image – Read-only, layered filesystem template

Docker Container – Active runtime instance

Dockerfile – Declarative build specification

Docker Registry – Distributed image repository

Docker transforms infrastructure into code and deployment into an automated, repeatable discipline.

⚙️ Installation of Docker
🐧 Docker Installation on Linux (Ubuntu)
sudo apt update
sudo apt install docker.io -y
sudo systemctl start docker
sudo systemctl enable docker
docker --version✨ Docker ✨

Docker is an open-source containerization platform that enables developers to build, package, 
ship, and run applications as lightweight, portable, and self-sufficient containers. Each container
bundles the application code with its runtime, system libraries, dependencies, and configuration,
ensuring environment consistency across development, testing, and production.

## Monolithic vs Microservices
Monolithic
A monolithic system is a single-tier application architecture where the UI layer, business logic, and data access layer are combined into one executable artifact and deployed together on a single runtime environment.

## Traditional vs Vertualization vs Containerization

## What is Docker?

## Installation of Docker

## Docker Commands

```shell
docker run [ContainerImage]     # to run a container
docker run -d [ContainerImage]  # to run a container in detached mode
docker ps               # to list running containers
docker ps -a             # to list all containers
docker create [ContainerImage]  # to create a container
docker start [ContainerID]     # to start a container
docker stop [ContainerID]      # to stop a container
docker rm [ContainerID]        # to remove a container]
docker rm -f [ContainerID]     # to force remove a container
docker run -p [HostPort]:[ContainerPort] [ContainerImage]  # to expose a port
docker exec -it [ContainerID] bash  # to attach / access to a container
docker run -P [ContainerImage]  # to expose all ports on random ports from 32768 to 61000
docker logs [ContainerID]   # to check container logs
docker stats [ContainerID]  # to check container resources
```
