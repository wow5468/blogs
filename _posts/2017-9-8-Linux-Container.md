---
layout: post
title: Linux Container
---

**What's a container?**

A container (Linux Container) at its core is an allocation, portioning, and assignment of host (compute) resources such as CPU Shares, Network I/O, Bandwidth, Block I/O, and Memory (RAM) so that kernel level constructs may jail-off, isolate or “contain” these protected resources so that specific running services (processes) and namespaces may solely utilize them without interfering with the rest of the system. These processes could be lightweight Linux hosts based on a Linux image, multiple web severs and applications, a single subsystem like a database backend, to a single process such as ‘echo “Hello”’ with little to no overhead.

**Hypervisor-based**

![_config.yml]({{ site.baseurl }}/images/screen-shot-2014-06-13-at-9-18-11-am.png)
- Ability to easily run and accommodate legacy applications
- Performance benefits of running on bare-metal, no overhead of hypervisor
- Higher density and utilization for resources in the datacenter
- Adoption for new technologies is accelerated, put in isolated secure containers
- Reduce “shipping” pains; code is easily streamlined to customers, fast. 

**Container-based**

![_config.yml]({{ site.baseurl }}/images/3.png)

**Speed difference**

![_config.yml]({{ site.baseurl }}/images/4.png)


On a typical physical server(bare metal), with average compute resources:
- 10 - 100 virtual machines
- 100 - 1000 containers

On disk, containers can be very light:
- A few MB - even without fancy storage.

**Solutions and products**
- LxC ( Linux Containers )
    - 0.1.0 releases in 2008
    - Works with general vanilla Linux kernels off the shelf.
    - GNU GPLv2 License
    - Used as a “container engine” in Docker
    - Google App Engine utilizes an LXC-like technology
    - Parellels Virtouzzo utilizes LXC
    - Rackspace Cloud Databases utilize LXC
    - Heroku (Application Deployment Platform) utilize LXC
- Docker
    - Developed by (formally dotCloud) Docker Inc.
    - Apache 2.0 License
    - Docker is really an orchestration solution built on top of the linux kernel, namespaces, cgroups, chroot, and file system constructs. Docker originally chose LXC as the “engine” but recently developed their own solution called “libcontainer”
    - Solutions:
        - “Decker” – Modified version of the engine works with Cloud Foundry to deploy application workloads
        - Openshift
        - AWS Elastic Beanstalk Containers
        - Openstack Solum
        - Openstack Nova
        
**References**

[Linux Containers: Parallels, LXC, OpenVZ, Docker and More](https://aucouranton.com/2014/06/13/linux-containers-parallels-lxc-openvz-docker-and-more/)