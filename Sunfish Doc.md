

![img](https://www.openfabrics.org/wp-content/uploads/sunfish-logo-954x614-on-white-300x193_c.jpg)

# Sunfish OpenFabrics Management Framework for Composable Disaggregated Infrastructures

Version 0.0.1

**ABSTRACT:** Sunfish is designed for managing composable disaggregated resources over multiple fabrics using a central repository and an open-source API and toolset. Sunfish is designed for manipulating connected hardware resources using client-friendly RESTful abstractions and configuring fabric interconnects so that datacenter and AI workloads can be linked with available resources over dynamic fabric infrastructures. 

The Sunfish OpenFabrics Management Framework API defines a RESTful interface and a standardized data model to provide data structures to help simplify the development of composable distributed, disaggregated, computer architectures. Sunfish contains abstract data structures that represent computer system resources, available network fabric components and management, current resource operational conditions, and abstracted representations of composed disaggregated computing systems.

*Last Updated  01/08/2024*

**USAGE**

Copyright (c) 2024 OpenFabrics Alliance (OFA). All rights reserved. All other trademarks or registered trademarks are the property of their respective owners.

The OpenFabrics Alliance hereby grants permission for individuals to use this document for personal use only, and for corporations and other business entities to use this document for internal use only (including internal copying, distribution, and display) provided that:

1. Any text, diagram, chart, table or definition reproduced must be reproduced in its entirety with no alteration, and,
2. Any document, printed or electronic, in which material from this document (or any portion hereof) is reproduced must acknowledge the OFA copyright on that material, and must credit the OFA for granting permission for its reuse.

Other than as explicitly provided above, you may not make any commercial use of this document, or any portion thereof, or distribute this document to third parties. All rights not explicitly granted are expressly reserved to the OFA.

Permission to use this document for purposes other than those enumerated above may be requested by emailing TBD. Please include the the requesting individual and/or company and a brief description of the purpose, nature, and scope of the requested use.

All code fragments, scripts, data tables, and sample code in this OFA document are made available under the following license: BSD 3-Clause Software License.

- Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:

  1. Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
     
  2. Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
     
  3. Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.

> THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
> DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR
> SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
> OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

**DISCLAIMER**

Publication of this document for review and comment has been approved by the OpenFabrics Alliance (OFA) OpenFabrics Management Framework (OFMF) Working Group. This document may be updated, replaced, or made obsolete at any time and as such should not be used as reference material or cited as other than a ‘work in progress.’ Suggestions for revision should be directed to TBD. The information contained in this publication is subject to change without notice. The OFA makes no warranty of any kind with regard to this publication, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose. The OFA shall not be liable for errors contained herein or for incidental or consequential damages in connection with the furnishing, performance, or use. Suggestions for revisions should be directed to TBD.

**Current Revision**

The OFA is actively engaged in expanding and refining the Sunfish documentation. 

The most current revision can be found on the OFA web site at TBD

**Contact the OpenFabrics Alliance (OFA)**

Current OFA practice is to make updates and other information available through TBD.

Requests for interpretation, suggestions for improvement, additions, or defect reports are very welcome. They should be sent via TBD.

**INTENDED AUDIENCE**

TBD

**VERSIONING POLICY**

This document is versioned material. Versioned material shall have a three-level revision identifier, comprised of:

1. Version Number: Version numbered material shall be backwards compatible with all of previous revisions of that material that have the same version number. There is no assurance of interoperability or backward compatibility between revisions of a versioned material with different version numbers.
2. Release Number: A release represented by a minor revision number represents a technical change to existing content or an adjustment to the scope of the versioned material. Each minor revision causes the release number to be increased by one. The OFA will make every effort to ensure, but not guarantee, that versioned numbered and release numbered material shall be backwards compatible with previous revisions of the material with the same version number and release number. 
3. Errata Number: Contents of an errata revision of versioned material are limited to minor corrections or clarifications of existing versioned material. An errata revision may be backwards incompatible if the incompatibility is deemed necessary for correct operation of implementation(s) of the versioned material.  

Future publications of this document are subject to specific constraints on the scope of change that is permissible from one revision to the next and the degree of interoperability and backward compatibility that should be assumed between products designed to this standard. This versioning policy applies to all OFA Sunfish versioned materials.

**Revision History**

The evolution of this document is summarized in Table 1 <TBD: Insert hyperlink to Table 1>

Table 1: Revision history

| Date | Revision | Notes |
| ---- | -------- | ----- |
|      |          |       |
|      |          |       |
|      |          |       |



**About the OpenFabrics Alliance**

The mission of the OpenFabrics Alliance (OFA) is to accelerate the development and adoption of advanced fabrics for the benefit of the advanced networks ecosystem. The mission is accomplished by; creating opportunities for collaboration among those who develop and deploy such fabrics, incubating and evolving vendor independent open source software for fabrics, and supporting and promoting the use of such fabric technology software.

**Acknowledgements**

The OFA OFMF Working Group, which developed and reviewed this work in progress, would like to recognize the significant contributions made by the following members listed in <TBD: Insert hyperlink to Table 2>.

Table 2: Contributors

| Member Entity                    | Representative     |
| -------------------------------- | ------------------ |
| Intel                            | Phil Cayton        |
| Sandia National Lab              | Mike Aguilar       |
| IBM Research                     | Christian Pinto    |
| HPE                              | Russ Herrell       |
| Redhat                           | Doug Ledford       |
| Intel                            | Richelle Ahlvers   |
| IBM Research                     | Michele Gazzetti   |
| HPE                              | Jeff Hilland       |
| HPE                              | John Mayfield      |
| IntelliProp                      | Jim Hull           |
| IntelliProp                      | Tracy Spitler      |
| Lawrence Livermore National Labs | Chris Morrone      |
| Cornelis                         | Eugene Novak       |
| Cornelis                         | Dennis Dallesandro |
| HPE                              | Kurt Bowman        |
| Sandia National Labs             | Catherine Appleby  |
| Los Alamos National Labs         | Alex Lovell-Troy   |

# Table of Contents

[TOC]



# 1. Abstract

Sunfish is designed for System Administrators, Application Programmers and users, HPC and Cloud Architecture Designers, and other stakeholders that are involved in the design, deployment, and use of stable and high-speed network based computing systems.

Sunfish provides a universal set of RESTful interfaces and tools and services to manage fabric attached resources, such as, CPUs, Accelerators, and Memory Devices. Sunfish uses the Redfish Scalable Platforms Management API Specification  to allow clients to gather telemetry information on fabrics and components, request information about fabric attachments, allocate components, and compose disaggregated systems. Each vendor specific fabric can be controlled and manipulated through the use of a custom agent that is designed to provide its services and functions to Sunfish via the Redfish API. Redfish currently has an object called a ‘zone’ that contains a list of the fabric endpoints which may be connected to each other. Zones can be used to enumerate the members of a vLAN, or the resources of a virtual platform. Sunfish is designed to be versatile and allow clients to connect and interact with underlying high-speed fabrics.

Sunfish provides computing system clients with a common set of tools, to interact with disaggregated fabrics and resources. Clients may include, but are not limited to, Message Passing Interface applications, Fabric Attached Memory (FAM), Workload, Resource, and Cloud managers, IO systems, storage configuration managers, and CPU and accelerator resources. Client embodiments may include, but are not limited to, physical machines, virtual machines, appliances, embedded computational engines, and containers. Any entity (SW tool, admin GUI, shell script via CLI) may create a virtual platform, pod, cluster, partition, vLan, job queue, or subnet to enable some workload(s) to execute. 

# 2. Document Organization



## 2.1. Document Scope

TBD



## 2.2. Audience Assumptions

As Sunfish is designed as an extension of the Redfish Scalable Platforms Management API Specification, this document is written with the presumption that the reader has a detailed understanding of the Redfish Specification. This document cannot be fully understood without that context.

## 2.3. Normative References

The documents referenced in <TBD: Insert hyperlink to Table 3> are indispensable for the application of this document. For dated references, only the edition cited applies. For undated references, the latest edition of the referenced document (including any amendments) applies.

The approved references that contribute to this document are summarized in <TBD: Insert hyperlink to Table 3>

Table 3: Approved normative references

| Title (Version)                  | Authoring entity | Reference URL |
| -------------------------------- | ---------------- | ------------- |
| Redfish Specification            | DMTF             |               |
| Redfish Data Model Specification | DMTF             |               |
| Swordfish Specification          | SNIA             |               |
| NVMe Family of Specifications    | NVMe Consortium  |               |
| CXL Specification                | CXL Consortium   |               |
|                                  |                  |               |

## 2.4. Terms and Definitions

In this document, some terms have a specific meaning beyond the normal English meaning. Those terms are defined in this clause including new terms, frequently used Composable Disaggregated Resource Management terms, Sunfish Terms, Redfish terms, etc.

### 2.4.1 Sunfish-specific Terms

The terms listed in <TBD: Insert hyperlink to Table 5> are used in this document.

Table 5: Sunfish terms

| Term                   | Definition |
| ---------------------- | ---------- |
| Fabric Specific Agent  |            |
| Sunfish Agent Services |            |
| Sunfish Service        |            |
|                        |            |
|                        |            |
|                        |            |
|                        |            |



### 2.4.2 Redfish terms

Many terms in this document were originally defined in the Redfish Specification. Some of the more common terms and definitions are reproduced in <TBD: Insert hyperlink to Table 6>, as an aid to the reader.

Table 6: Redfish terms

| Term                   | Definition                                                   |
| ---------------------- | ------------------------------------------------------------ |
| OData                  | The Open Data Protocol, as defined in <TBD: Insert hyperlink to external OData-Protocol document> |
| OData Service Document | Resource that provides information about the service root for generic OData clients. |
| Redfish Schema         | Defines Redfish Resources according to OData schema representation. You can directly translate a Redfish Schema to a JSON Schema representation. |
| Redfish service        | Implementation of the protocols, resources, and functions that deliver the interface that this specification defines and its associated behaviors for one or more managed systems. |
| Request                | A message from a client to a service.                        |
| Service Root           | Resource that serves as the starting point for locating and accessing the other resources and associated metadata that together make up an instance of a Redfish Service. |

## 2.5 Keywords (normative language terms)

This document conforms to ISO/IEC Directives, Part 2 for keyword usage. The most common terms and their intended meanings are summarized <TBD: Insert hyperlink to Table 7>.

Table 7: Normative language terms

| Term(s)             | Meaning                                                      |
| ------------------- | ------------------------------------------------------------ |
| shall / shall not   | Used to identify objectively verifiable criteria to be fulfilled and from which no deviation is permitted if compliance with the document is to be claimed |
| should / should not | Used to identify a suggested possible choice or course of action deemed to be particularly suitable without necessarily mentioning or excluding others |
| may / need not      | Used to convey consent or liberty (or opportunity) to do something |
| can / cannot        | Expected or conceivable material, physical or causal outcome |
| must                | Identifies a constraint or obligation on the user of the document, typically due to one or more legal requirements or laws of nature, that is not stated as a provision of the standard *NB:* “must” is not an alternative for “shall”, and should only be used for constraints that arise from outside this standard |

# 3. Sunfish Framework

## 3.1. Introduction

TBD: Describe the general purpose of Sunfish. Explain how this chapter is organized (purpose of Sunfish, define CDI, value proposition of CDI, value proposition of Sunfish relative to CDI / Justify Sunfish.  Go into Composable Network/fabric Infrastructure)

### 3.1.1 Overview of Composable Disaggregated Infrastructure

Traditional HPC compute clusters are created by combining separate compute servers over a shared network fabric. Each individual compute server in the cluster is statically provisioned with its own CPUs, memory devices, accelerator cards, and storage devices to accommodate as many different application runtime requirements as possible. This need to incorporate “all of the options that may be required to support a given workload” often results in resource overprovisioning, makes traditional HPC architectures less flexible and less efficient, and can lead to situations where application jobs are more prone to run-time failure. Resources overprovisioning and inefficient use of hardware are common issues to any large scale computing facility.

For example, design considerations that lead to an under estimation of compute server memory resources can cause out-of-memory conditions. In another example, IO server memory oversubscription can result in filesystem failure and can occur due to virtual memory page swap thrashing, and lead to eventually application failure. The above issues could be mitigated with the dynamic addition of memory.

Another issue with the architectural inflexibility of current, siloed, HPC architecture is that it frequently results in overprovisioned or stranded resources. Stranded resources are those that are either are on a compute server that, due to a lack of other resources (e.g., CPU), is unavailable to a workload, or that have been assigned to a workload that isn’t making use of them. Overprovisioned resources are those that are either underused, or unused and idle for the current workloads but still draw energy and cooling.

The facility costs of large scale HPC systems including cooling and energy usage is becoming more of an issue. The overall scale might not seem worrying but looking at single countries, data centres can account for a significant portion of the overall yearly consumption. 

A solution to addressing the overprovisioning and computational efficiency limitations, as well as hardware and operating costs, of integrated, siloed, systems is the use of Composable Disaggregated Infrastructures.

With Composable Disaggregated Infrastructures, computational resources are not statically provisioned in servers, but instead are physically disaggregated in shared pools and connected through high-speed/low-latency network fabrics. These resources may be dynamically provisioned and re-provisioned to client applications, as needed, and are thus not only more efficient to manage by removing unnecessary hardware, but help reduce energy consumption and datacenter cooling costs.

CDI enables assigning pools of resources to consumers.  Remote resource disaggregation is already common for storage devices (e.g., NVMe-oF); current trends are pushing this paradigm further, extending it to assigning private or shared resources such as computational engines, disaggregated memory elements, disaggregated accelerators, and eventually to all forms of compute resources required by modern HPC applications. 

### 3.1.2 Managing composable Disaggregated Infrastructures

The larger the HPC system, the greater the potential impact of dynamic composability of disaggregated components to energy efficiency and computational stability. Composability managers are needed to efficiently connect workloads with resources in a dynamic ecosystem, at scale, without concern for the management model of the underlying hardware technology; in addition, centralized composabilty management must be scalable to be able to handle massive amounts of hardware telemetry, device states, device capabilities, and subscription information from large numbers of resources.

Disaggregated resource types are increasingly being accessed over a variety of fabric types and technologies; and being able to fully orchestrate these resources in a dynamic, heterogeneous environment requires managing those fabrics and the hardware resources that may be accessed thereon. 

The management and optimization of such a diverse set of fabrics and fabric technologies to realize the benefits of Composable Disaggregated Infrastructures is quickly becoming a complex issue to solve for infrastructure managers, especially in heterogeneous multi-vendor environments, with multiple vendor-sourced hardware and the ever-expanding collection of proprietary APIs and tools.

### 3.1.3 Sunfish/CDI  Value Propositions

#### 3.1.3.1  Software Defined Node Architecture

TBD

#### 3.1.3.2  More Efficient Sharing of Resources Through Resource Pools

In current HPC systems, hardware resources that are necessary to provide every type of computation must be installed into the compute nodes. This type of architectural design leads to wasted resources and limitations on the resources that are available to user jobs. For instance, if a user job requires six GPUs, 1 TB of on-board memory, and eight CPU cores in each node to complete a batch job, then the job cannot be run on a cluster with four GPUs and four CPU cores. In addition, if a batch job needs two GPUs and two CPU cores, two GPUs and two CPU cores are wasted resources that can't be allocated to other 'needy' batch jobs.

In a new composable HPC system <TBD: Insert hyperlink reference to the appropriate figure>, resource pools can allocate CPU cores, NVMe memory devices, GPUs, and FPGAs from available hardware pools, through aggregated RDMA and CXL fabrics. Hardware resources that are combined in such a manner provide versatility to batch jobs and mitigation of wasted resources. In addition, if a compute node is using only a single CPU core and a GPU is not being utilized, the GPU can be allocated to another compute node that needs the GPU to fulfill the requirements of its own batch job.

![img](https://www.openfabrics.org/wp-content/uploads/ofmfwg/2022-12-updates/Slide7.jpeg)

TBD: Needs discussion on scale and how to deal with conflicting requests and configuration.

TBD: Needs discussion on recovery of a system-wide configuration on restart of components, managers, agents, ...

#### 3.1.3.2 Sharing of Memory resources

Using Sunfish to manage and allocate memory and switches and NVMe memory that are based upon the CXL-3.0 specification, both remote memory and compute node memory can be shared. The figure below shows a simple example of memory sharing. On the left side, the orange node is connected to the orange NVMe memory through a CXL switch. On the right side, Sunfish has allowed the orange node to take a smaller portion of a shared NVMe memory. The blue node, needing more memory resources, has a portion of the shared memory and another NVMe memory, again connected via a CXL fabric switch.

![image-20231222105329458](C:\Users\pccayton\AppData\Roaming\Typora\typora-user-images\image-20231222105329458.png)

#### 3.1.3.3 Sharing of Storage Resources

##### 3.1.3.3.1 On-Demand Node-Local Parallel Filesystem

Node-local parallel filesystems (e.g., BeeGFS, Lustre) provide ephemeral scratch space to keep inter-node IO traffic localized. In many cases, the best way to implement the back-end block devices for these node-local parallel filesystems is with RAM disks. On-demand parallel filesystems are implemented with Management, Metadata Targets, and Object Storage (see the figure below). The amount of allocated RAM disk storage must provide enough space to accomodate growth of Metadata and Object Storage stripes. Communication between the parallel filesystem components can be performed via Ethernet but is more commonly performed with RDMA to reduce communication latency and improve bandwidth. In current HPC and Cloud architectures, the RAM disk block devices are reducing the available RAM for running processes.

In a composable parallel computing system, a better option is to deploy requested RAM disk storage from available NVMe memory blocks, using Machine Learning trained datasets to find the memory that is going to provide the highest IO transaction bandwidth and lowest latency. As shown in the figure, CPU cores are matched to NVMe memories through CXL-3.0 spec peer-to-peer network switches. Included in the diagram, are block storage devices that are available through the CXL switches for another option. IO block transactions are very good candidates for dynamically attached memories blocks, because processes and threads can be placed into an IO wait queue by the OS until the transactions are completed and an interrupt is generated.![img](https://www.openfabrics.org/wp-content/uploads/ofmfwg/2022-12-updates/Slide5-4.jpeg)

##### 3.1.3.3.2 DAOS Composable Management

Figure TBD <TBD: Insert hyperlink to the appropriate figure> shows a composable implementation of Distributed Asynchronous Object Storage ([DAOS](https://docs.daos.io/v2.2/overview/architecture/)) utilizing CXL peer-to-peer switches and NVMe memories providing Pool Shard blocks of storage for DAOS targets.  Each of the nodes can be configured as a DAOS container. Connections to the Object Storage are through an NDR RDMA switch.

![img](https://www.openfabrics.org/wp-content/uploads/ofmfwg/2022-12-updates/Slide21.jpeg)

3.1.3.4 Composable Accelerators

##### 3.1.3.4.1 Composable GPU Management

## 3.2 Sunfish Framework Overview

### 3.2.1 Introduction to the Sunfish Framework

Sunfish is designed to configure fabric interconnects and manage composable disaggregated resources in dynamic High Performance Computing (HPC) infrastructures using client-friendly abstractions. Sunfish provides a framework for abstraction of, and communication with, the multitude of independent management tools behind a single, consistent, standards-based API; it does this through a universal set of RESTful interaces and tools and services to manage fabric attached resources, such as, CPUs, Accelerators, and Memory Devices. Sunfish uses the common languages of [Redfish ](https://www.dmtf.org/standards/redfish)and [Swordfish](https://www.youtube.com/watch?v=zU1ZCYMgCQQ&t=8s), to allow clients to gather telemetry information on fabrics and components, request information about fabric attachments, allocate components, and compose disaggregated systems. Each vendor specific fabric can be controlled and manipulated through the use of a custom agent that is designed to provide its services and functions to Sunfish via the Redfish API. 

![image-20231222141429647](C:\Users\pccayton\AppData\Roaming\Typora\typora-user-images\image-20231222141429647.png)

On the right are disaggregated resources with potentially many different management entities in direct control using vendor and device specific means.  An Agent layer to aggregate the inventory from technology-specific hardware managers and convert the hardware specific device and resource descriptions into a standardized and commonly interpreted Redfish model. Agents are resource aggregators that present Sunfish with a Redfish / Swordfish model of all resources which they manage and/or model.  Agents communicate the whole model of the disaggregated resources they communicate with to the Sunfish Services which masks much of the hardware specific details from the clients. 

The Sunfish services aggregates and manage the Redfish Models of all resources from the library of active hardware agents.

Clients of Sunfish Services see the Redfish models of resources and manipulate these models to establish or alter the state of individual resources or their assignments (bindings) to consumers (e.g., hosts).

As it is critical that Agents and Clients have the same interpretation of a Redfish object found in the Sunfish database, the Sunfish framework also has policies and requirements to be followed when creating or interpreting the Redfish models.

Managing CDI requires some modest amount of scale, which in turn requires a Redfish representation of many different resource types residing on different interconnects, all supplied by different vendors. Disaggregated resources and interconnect fabrics may or may not support a Redfish API suitable for directly plugging into the Sunfish management framework, so the presence of an API translating Agent entity is used in all cases, though the complexity of any given Agent obviously depends upon the actual fabric management APIs and policies in use in the hardware managers’ realm. Sunfish not only collects and manages the Redfish object models for disaggregated resources, the fabrics that connects them, but also serves up control points for many common management tasks, such as Events and Logs, Access Control settings and policies, and authentication needs.

![image-20231222145436179](C:\Users\pccayton\AppData\Roaming\Typora\typora-user-images\image-20231222145436179.png)

### 3.2.2 Agents and Hardware Managers

As stated in TBD, Agents are resource aggregators that present Sunfish with a Redfish / Swordfish model of all resources which they manage and/or model.  Sunfish / Agent communications are event-driven.  This section provides a high-level overview of Sunfish Agent concepts and functionality; section TBD contains details of technology specific Agents.

Agents send Events to Sunfish to: 

- start the Sunfish/Agent interface; Sunfish creates the appropriate objects in its resource tree and acknowledges the event,
- alert Sunfish of the presence of new resources (e.g., a new fabric); Sunfish responds with a recursive Fetch of all subordinate and linked resources under the newly created resource (TBD: Insert and reference a hyperlink to the appropriate image),
- alert Sunfish of health and status changes in existing resources, or
- inform Sunfish of Events received from resources the Agent manages

![image-20231222144900019](C:\Users\pccayton\AppData\Roaming\Typora\typora-user-images\image-20231222144900019.png)

Sunfish registers for Events associated with resources and sends Redfish and Swordfish API calls to Agents to:

- query the latest status, health, or configuration of the Agents’ resources,
- request changes in state or configuration of Agents’ resources, or
- create or destroy logical Redfish and Swordfish objects which impact Agents’ resources

The Goal is to  maintain current Sunfish resource models without ‘polling’.

#### 3.2.2.1 Agent Failover / Failure-recovery

### 3.2.3 Client Layer

TBD

![image-20231222145919195](C:\Users\pccayton\AppData\Roaming\Typora\typora-user-images\image-20231222145919195.png)

### 3.2.4 Sunfish Core Services 

TBD - This requires text to describe the Management Layer responsibilities and components; I put in some example images that we can use to describe the Management Layer - these may not be the correct images to use... in any event, more images are probably necessary to explain the full picture.

![image-20231222145722443](C:\Users\pccayton\AppData\Roaming\Typora\typora-user-images\image-20231222145722443.png)

#### 3.2.4.1 Resource Control Operations

TBD - This would involve a subsection for each of the operations detailing the scope of the operation and the sequence of operations for each task - including task synchroneity. 

![image-20231222150108860](C:\Users\pccayton\AppData\Roaming\Typora\typora-user-images\image-20231222150108860.png)

#### 3.2.4.2 Resource Events

TBD - This would involve an overarching description of 'Events' from a Sunfish PoV and a subsection for each of the event operations detailing the scope of the operation and the sequence of operations for each task.

![image-20231222150436566](C:\Users\pccayton\AppData\Roaming\Typora\typora-user-images\image-20231222150436566.png)

### 3.3 Sunfish Interpretation of the Redfish Fabric Model

An abstract model in the ‘Redfish/Swordfish domain’ can be modeled as a group of endpoints, resources, zones, and zones-of-zones. An endpoint can be considered to be a destination, such as a server connected by a network card or a switch port.  A resource can be considered as a component that provides services to a fabric. A zone can be considered to be a set of endpoints and resources that provide an integrated unit, such as a collection  of remote memory. Finally, a zone-of-zones can be considered to be a unit or collection, of zones.

In the Redfish model there is no notion of physical separation. Thus, a zone of memory, for instance, could be made up of 2 separate memory chunks that are routable to each other, yet are not located in the same endpoint. The model above depicts only the logical resources, not the physical connections. Redfish models the physical fabric topology by associating actual fabric ports and fabric links.

The fabric itself (i.e., the connectivity) is modeled as ports and endpoints. Physical fabric connections (e.g., cables) are always shown as between 'ports'. Ports are traced back to the fabric devices that drive the ports. Fabric devices trace back to physical or logical infrasctructure which controlls the fabric device and to the 'Endpoint' object associated with the fabric device.

Discovery of physical and logical resources accessible via the fabric is necessarilly a fabric-specfic operation.

Non-fabric resources (i.e., resources not directly visible to the fabric) associated with the fabric devices (i.e., endpoints) may or may not have detailed Redfish models and schema that can be accessed via the same Service Root; for example, if the Service Root is maintained by the 'Fabric Manager', the fabric manager may not have visibility to details about systems or resources behind the fabric adapter, however the fabric manager must know sufficient details about the fabric adapter to correctly enable clints to access endpoints on the fabric that it is allowed to reach.

The example in Figure TBD (Insert hyperlink reference to figure TBD) shows a basic fabric model example with disaggregated memory components. The memory components can be allocated over fabrics to multiple composed systems. Sunfish provides tools and constructs to keep track of both allocation of memory resources, pathways from CPUs and Accelerators to the memory, and current running compute states.  



![img](https://www.openfabrics.org/wp-content/uploads/ofmfwg/redfish-ofmf-model-example.jpg)

### 3.4 Sunfish Access Rights and Permissions

TBD

# 4. Sunfish  Agents

TBD: Recap of Sunfish Agents as Fabric/Technology Specific Agents and how they map to management capabilities, APIs, ...

## 4.1 Compute Express Link (CXL)

### 4.1.1 CXL Overview

Compute Express Link (CXL) is an open industry standard that defines a family of interconnect protocols to support connections between CPUs and memory expansion devices and accelerators.

### 4.1.2 RESTful Agent API for CXL

### 4.1.3 Resource URL

### 4.1.4 Error Messages

### 4.1.5 Authorization

## 4.2 Compute Express Link (CXL)  Fabric Attached Memory

### 4.2.1 CXL Fabric Attached Memory (FAM) Overview

<TBD>

### 4.2.2 Sunfish Architecture for Fabric Attached Memory 

This section defines the policies and requirements the Sunfish Architecture imposes on Clients and Agents when interpreting or creating Redfish models of Fabric Attached Memory (FAM) managed via the Sunfish Architecture.  

### 4.2.3 Important taxonomy used herein, within the context of discussions around FAM

Producer, Memory source, Memory resource, Memory target, Memory funder: The physical entity attached to the fabric that supplies memory resources to satisfy fabric requests for memory reads and writes. This physical entity will store or recall the data being written or read.

Consumer, Host, Compute Entity, Data Mover, Requester, Initiator: The physical entity attached to the fabric that launches a fabric request for a memory read or write transaction to the target device. This physical entity will source or sink the data contained in the fabric memory read or write transaction.

Homogeneous (wrt memory resource) memory: The first requirement for FAM capacity to be considered homogeneous is such Memory capacity shall have the same persistence or volatile property across the entire range of data locations serviced by said memory sources.  A secondary consideration is not a requirement, but a strong recommendation.  Homogeneous memory capacity should have a similar access latency from similar access points such that multiple threads accessing the same addresses within the capacity have consistent performance.

Fabric Attached Memory is memory capacity that can be accessed across the fabric where the:

·    The source of FAM is the Producer. 

·    The Consumer is the initiator of a memory request; for example a Host or a data move engine.

### 4.2.4 Sunfish Policies on Modelling FAM with Redfish Objects

All fabric Agents are expected to comply with the following Sunfish interpretations and requirements when creating Redfish models of a FAM resource on any fabric. The following discussion introduces the critical Redfish objects that are intended to model FAM resources, and declares several general required policies that fabric Agents shall follow when creating these objects. FAM is memory capacity that can be accessed across a fabric. To have a presence on a fabric, the FAM shall have at least one Endpoint on the fabric.

A physical Endpoint shall have an associated unique fabric address that appears in the fabric transport-layer packets. This unique fabric address does not have to be visible in the Redfish Endpoint object JSON description. However, the FM/Agent stack must have the ability to translate a Redfish request targeted to a unique Redfish Endpoint object into one or more fabric-specific requests targeted at the unique fabric hardware entities.

An Endpoint presenting physical FAM to the fabric shall have a Connected Entity linked to a single Fabric Adapter. The Fabric Adapter shall represent the physical device that fields the fabric memory requests from the fabric and produces the response packets to return to the requester. A Fabric Adapter may have multiple ports which link into the fabric. Different fabrics may have different associations of these multiple ports to fabric IDs.  A single Fabric Adapter may present more than one Endpoint on the fabric, but any given physical Endpoint object shall not have more than one associated Fabric Adapter. A Fabric Adapter may present multiple logical devices to the fabric as multiple logical Endpoints. Each logical device shall be modelled as one and only one logical Endpoint, as allowing multiple physical or logical devices to be modelled as only one Endpoint can corrupt the Redfish concept of Zones.)

 The Fabric Adapter device may or may not make known to the FM any details about its associated chassis / enclosure, FRU, containing assembly, or other managers of such related entities. If the FM cannot discern a specific Chassis object housing the FAM’s Fabric Adapter, the FM/Agent stack shall create a generic FAM Chassis instance and attach the Fabric Adapter to the FAM Chassis’ subordinate Fabric Adapters collection. If the Fabric Adapter’s chassis details are supplied to Sunfish by a different Agent (for example, the chassis manager’s Agent), the only clear indicator that the generic FAM Chassis instance created by the fabric Agent and the chassis described by the chassis manager’s Agent are one and the same chassis is for both Agents to fill in the same Redfish Object UUID (or its equivalent) for the Fabric Adapter they each modeled. Therefore, all fabric component instances shall posses a globally unique, vendor defined UUID that can be read by each manager that may become involved. 

The FM shall create the subordinate PORTS collection and instantiate an appropriate Fabric Adapter Port object for each physical PORT discovered on the Fabric Adapter. The Fabric Adapter, by definition must have at least one physical port connected to the fabric which claims this Endpoint. The Fabric Adapter may have additional PORTs that are connected to devices not currently modelled as Redfish Switches or Redfish Endpoints on this same fabric. For example, if the Fabric Adapter represents a multi-headed FAM module. 

 The FM shall discover the entirety of the FAM resources accessible through the Fabric Adapter, and shall create appropriate homogeneous Redfish Memory resource objects to describe the available memory capacity. When the FM discovers the FAM device, the FM/Agent stack is responsible for breaking up all the Memory resources the adapter presents to the fabric into homogeneous memory resource pools. Some FAM devices may declare their memory resources as specific commercially available memory devices (for example: DDR5 DIMM devices, Optane NVDIMMs).  Some FAM devices may declare their memory resources as different quantities of generic memory media types (for example: volatile RAM, persistent RAM, persistent block-mode storage). Homogeneous Memory resources may be modelled using any applicable Redfish Memory object. See example for CXL Type 3 device with homogeneous memory resources in Section TBD. Non-homogeneous Memory resources shall be modelled as an appropriate number of homogeneous Memory resources. See example for CXL Type 3 device with hybrid (volatile and non-volatile) memory resources in Section TBD.

 After creating the appropriate homogeneous Memory resource objects for a Fabric Adapter, the FM/Agent stack shall create one or more homogeneous Memory Domains linked to appropriate collections of the Fabric Adapter’s Memory resource objects. 

Any Fabric Adapter which acts as a producer of FAM resources to the fabric thus shall have navigation links to one or more \*homogeneous\* Memory Domain objects.

 If the FM/Agent stack has an a priori plan that dictates how one or more of a FAM module Fabric Adapter’s Memory Domains are to be split up into individual Memory Chunks, the FM/Agent stack shall create the desired Memory Chunks. If there are no a priori plans that dictate allocation of Memory Chunks from the various MemoryDomains, the FM/Agent stack should not create the Memory Chunks collection or any default Memory Chunk instances. Their existence at the first appearance (creation time) of a FAM module will imply such memory allocations are reserved and not available to Clients of the Sunfish Redfish Service. The Redfish bubble diagram of Figure 1 depicts the Redfish object hierarchy of a FAM object as described by the above Fabric Adapter, Memory Domains, Memory sources, and an existing Memory Chunk. Note that requirement that Memory Domains be homogeneous coupled with the definition that a Memory Chunk is a subordinate of a single Memory Domain implicitly defines a Memory Chunk to consist of homogeneous media locations from within one physical device.

### 4.2.5 RESTful Agent API for CXL FAM

### 4.2.6 Resource URL

### 4.2.7 Error Messages

### 4.2.8 Authorization

## 4.3 NVMe

### 4.3.1 NVMe Overview

NVM Express (NVMe) is a standard interface and protocol library developed to fully realize the benefits of Non-Volatile Memory (NVM) by accelerating access to Non-Volatile Memory Devices (e.g., SSDs).  The NVMe specification family defines how hosts communicate with non-volatile memory either directly via e.g., the PCIe interface, or indirectly, through the supported NVMe fabric gransports (e.g., RDMA, Fibre Channel, TCP).  Indirectly accessing NVMe devices over fabrics extends the low-latency, efficient, NVMe storage protocol to provide scale-out access to, and sharing of, storage from remote storage systems (e.g., storage servers, storage appliances).  NVMe maintains the same architecture and software of the NVMe protocol, providing the benefits of NVMe regardless of the fabric type or the type of non-volatile memory used in the storage target or appliance.  

### 4.3.2 RESTful Agent API for NVMe

### 4.3.3 Resource URL

### 4.3.4 Error Messages

### 4.3.5 Authorization

## 4.4 Infiniband Fabric

### 4.4.1 Infiniband Overview

### 4.4.2 RESTful Agent API for Infiniband

### 4.4.3 Resource URL

### 4.4.4 Error Messages

### 4.4.5 Authorization

## 4.5 OmniPath Fabric

TBD: This may be the redundant if this is the same as IB...

### 4.5.1 OmniPath Overview

### 4.5.2 RESTful Agent API for OmniPath

### 4.5.3 Resource URL

### 4.5.4 Error Messages

### 4.5.5 Authorization

## 4.6 Gen-Z Fabric

TBD

### 4.6.1 OmniPath Overview

### 4.6.2 RESTful Agent API for OmniPath

### 4.6.3 Resource URL

### 4.6.4 Error Messages

### 4.6.5 Authorization

## 4.7 Slingshot Fabric

TBD

### 4.7.1 OmniPath Overview

### 4.7.2 RESTful Agent API for OmniPath

### 4.7.3 Resource URL

### 4.7.4 Error Messages

### 4.7.5 Authorization

# 5. Client and Composition {Layer} Requirements



## 5.1. Security

TBD (however we should state, at a minimum, that this document generally adheres to the security requirements defined in the Redfish Specification.) 

## 5.2. General constraints

### 5.2.1. Redfish elements

The Sunfish interface uses and extends the Redfish service interface. As such, all required elements of the Redfish model shall be present in Sunfish, therefore Sunfish functionality shall not conflict with any previously defined Redfish functionality but it may add to or extend it. Any functionality desired in a Sunfish implementation that is specified in Redfish shall follow the requirements as specified in the Redfish specification.

## 5.2.2. Events

### 5.2.2.1. Overview

### 5.2.2.2. Message Registry Selection and Management

### 5.2.2.3. Required Usage

### 5.2.2.4. Recommended Usage

- Standard Messages should be used, wherever possible.
- OEM messages should be avoided. Suggestions for clarification or expansion of the existing registries are encouraged. (submissions should be sent to TBD)

## 5.3. Discovering resources via Sunfish

## 5.4. Class Of Service requirements

## 7.5. HTTP status codes5

### 7.5.1. Create

### 7.5.2. Update, Replace, Delete

### 7.5.3. Actions

# 6. Annex A: Bibliography

## 6.1. A.1 Overview

The following referenced documents provide important support for the application of this document. For dated references, only the edition cited applies. For undated references, the latest edition of the referenced document (including any amendments) applies.

## 6.2. A.2 Informational references

The informational references are summarized in Table A.1.

| Tag  | Title (Version) | Author | URL  |
| ---- | --------------- | ------ | ---- |
|      |                 |        |      |
|      |                 |        |      |
|      |                 |        |      |
|      |                 |        |      |
|      |                 |        |      |
|      |                 |        |      |
|      |                 |        |      |
|      |                 |        |      |
|      |                 |        |      |
|      |                 |        |      |

Table A.1: Informational References