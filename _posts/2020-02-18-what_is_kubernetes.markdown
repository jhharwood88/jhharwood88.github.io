---
layout: post
title:      "What is Kubernetes?"
date:       2020-02-18 21:00:53 +0000
permalink:  what_is_kubernetes
---


Im sure by now you have heard of the popular container based architecture, but may be wondering to yourself what even is a container? Containers help modernize applications, making it easier to scale and deploy them. While they have great power, they also have introduced new challenges in the form of complexity and adding a new infrastructure to your project. With containers, its possible to deploy large amounts of instances of a project or projects on a daily basis allowing for greater development potential. 

Originally developed by Google, Kubernetes is an open-source container organization platform built to allow the automation of container based applications, including their deployment and scaling. Kubernetes has become the standard go to for container organization. Kubernetes allows for easy deployment of applications, it does this by making a seperate layer, so that teams can create their applications and let the Kubetnetes manage the other aspects of deployment such as managing the load of applications across a group of developers, automatically managing resources and even stopping applications from consuming too many resources across a development team. It can also help to manage resources of a particular host, even moving applications to another host if extra resources are made available.

Kubernetes allows a team to develop faster, allowing a team to get the resources they require without having to physically procure them because the resources are all shared across a central infrastucture. This reduces or flat out removes the requiremnt to request additional resources to run an application, allowing for much quicker up time in deployment and testing. With containers, it also takes far less resources to run than the tradtional virtual machines, meaning less CPU and memory are required to get the job done. 

The way Kubernetes works is with its central component, a cluster. Clusters are made up of many virtual or phyiscal machines, allowing each to serve either as a master or a node. Nodes will host a group of one or more containers, which contain the applications within them. The master then can talk with each of these nodes, choosing when to create or destroy the containers within. This allows the master to route traffic to the containers based on how they are set up within the nodes.

The master access point works in the same way a control pannel would for administrators, allowing them and other users to work within the cluster to manage their own containers. Clusters will always have at least one master, but its possible to have more than one. The master will store the configuration data for clusters and pass it down to their nodes, which allow the nodes to maintain configuration for the containers theyre responsible for. The masters communicate with the cluster with an api server, making sure the containers match the configuration of the rest of the nodes in the cluster.

Nodes in a Kubernetes cluster are all configured by the same container setup, a typical setup would be Docker. This helps to manage the containers when they are deployed to the nodes. All of the applications will run inside of these containers and adopt the same configurations as their parent node. A process called a kubelet is in charge of managing the node, starting or stopping an application based on the instructions from the master. It will report its statistical information of its containers back to the master, making it easier to help decide on which containers to prioritize or remove.

While Kubernetes is a powerfull tool in the developers hands, it also can be a confusiong and intimidating thing to impliment. Given its recent development, its a growing but not quite common place use for developers especially in smaller application development where large scale resources arent as common. Despite its learning curve, its a worth while tool and I hope this blog provides some insight into the strengths to be gained by learning and implimenting Kubernetes in a real world development situation.



