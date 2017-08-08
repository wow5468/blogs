---
layout: post
title: What is Kubernetes?
---

What is Kubernetes
-------------------------

Kubernetes is an `open-source platform designed to automate deploying, scaling, and operating application containers.`

With Kubernetes, you can quickly and efficiently respond to customer demand:
- Deploy your applications quickly and predictably.
- Scale your application on the fly.
- Roll out new features seamlessly.
- Limit hardware usage to required resources only.

**Kubernetes is**
- **Portable**: public, private, hybrid, multi-cloud
- **Extensible**: modular, pluggable, hookable, composable
- **Self-healing**: auto-placement, auto-restart, auto-replication, auto-scaling

Why Containers? 
-------------------------------
Looking for reasons why we should be using [containers](http://blog.maden.kr/Linux-Container/)?

![_config.yml]({{ site.baseurl }}/images/arc.png)

The old way:
- The disadvantage of entangling the applications’ executables, configuration, libraries, and lifecycles with each other and with the host OS.
- Needs to build immutable VM images in order to achieve predictable rollouts and rollbacks.
- Heavyweight and non-portable.

The new way:
- Agile application creation and deployment: Increased ease and efficiency of container image creation compared to VM image use.
- Continuous development, integration, and deployment: Provides for reliable and frequent container image build and deployment with quick and easy rollbacks (due to image immutability).
- Dev and Ops separation of concerns: Create application container images at build/release time rather than deployment time, thereby decoupling applications from infrastructure.
- Environmental consistency across development, testing, and production: Runs the same on a laptop as it does in the cloud.
- Cloud and OS distribution portability: Runs on Ubuntu, RHEL, CoreOS, on-prem, Google Container Engine, and anywhere else.
- Application-centric management: Raises the level of abstraction from running an OS on virtual hardware to run an application on an OS using logical resources.
- Loosely coupled, distributed, elastic, liberated micro-services: Applications are broken into smaller, independent pieces and can be deployed and managed dynamically – not a fat monolithic stack running on one big single-purpose machine.
- Resource isolation: Predictable application performance.
- Resource utilization: High efficiency and density

Why do I need Kubernetes and what can it do?
-------------------------------------
At a minimum, Kubernetes can schedule and run application containers on clusters of physical or virtual machines. However, Kubernetes also allows developers to ‘cut the cord’ to physical and virtual machines, moving from a host-centric infrastructure to a container-centric infrastructure, which provides the full advantages and benefits inherent to containers. Kubernetes provides the infrastructure to build a truly container-centric development environment.

Kubernetes satisfies in production, such as:
- Co-locating helper processes, facilitating composite applications and preserving the one-application-per-container model
- Mounting storage systems
- Distributing secrets
- Checking application health
- Replicating application instances
- Using Horizontal Pod Autoscaling
- Naming and discovering
- Balancing loads
- Rolling updates
- Monitoring resources
- Accessing and ingesting logs
- Debugging applications
- Providing authentication and authorization

How is Kubernetes a platform?
-----------------------------
 Kubernetes was designed to serve as a platform for building an ecosystem of components and tools to make it easier to deploy, scale, and manage applications.
 
 Labels empower users to organize their resources however they please. Annotations enable users to decorate resources with custom information to facilitate their workflows and provide an easy way for management tools to checkpoint state.
 
 Additionally, the Kubernetes control plane is built upon the same APIs that are available to developers and users. Users can write their own controllers, such as schedulers, with their own APIs that can be targeted by a general-purpose command-line tool.
 
 What Kubernetes is not
---------------------------------------
Kubernetes:
- Does not limit the types of applications supported. It does not dictate application frameworks (e.g., Wildfly), restrict the set of supported language runtimes (for example, Java, Python, Ruby), cater to only 12-factor applications, nor distinguish apps from services. Kubernetes aims to support an extremely diverse variety of workloads, including stateless, stateful, and data-processing workloads. If an application can run in a container, it should run great on Kubernetes.
- Does not provide middleware (e.g., message buses), data-processing frameworks (for example, Spark), databases (e.g., mysql), nor cluster storage systems (e.g., Ceph) as built-in services. Such applications run on Kubernetes.
- Does not have a click-to-deploy service marketplace.
- Does not deploy source code and does not build your application. Continuous Integration (CI) workflow is an area where different users and projects have their own requirements and preferences, so it supports layering CI workflows on Kubernetes but doesn’t dictate how layering should work.
- Allows users to choose their logging, monitoring, and alerting systems. (It provides some integrations as proof of concept.)
- Does not provide nor mandate a comprehensive application configuration language/system (for example, jsonnet).
- Does not provide nor adopt any comprehensive machine configuration, maintenance, management, or self-healing systems.

What does Kubernetes mean?
---------------------------------
**Kubernetes** is that meaning helmsman or pilot, and is the root of governor and cybernetic